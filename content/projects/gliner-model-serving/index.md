---
title: "GLiNER model serving"
description: "Serve GLiNER extraction, classification and decision models with vLLM, with companion Haystack pipeline components."
summary: "Serve GLiNER extraction, classification and decision models on CPUs or GPUs, with structured decision APIs and Haystack integration."
weight: 20
featureimage: "project-logos/gliner.svg"
showBreadcrumbs: true
---

{{< lead >}}
Taking GLiNER extraction, classification and decision models from local inference to reusable APIs and Haystack pipelines.
{{< /lead >}}

{{< keywordList >}}
{{< keyword icon="skill-python" >}}Python{{< /keyword >}}
{{< keyword icon="skill-vllm" >}}vLLM{{< /keyword >}}
{{< keyword icon="skill-haystack" >}}Haystack{{< /keyword >}}
{{< keyword icon="docker" >}}Docker{{< /keyword >}}
{{< /keywordList >}}

I built **vllm-gliner** to serve GLiNER2 and GLiNER2.5 extraction and classification models, including the **GLiNER2.5 Decide decision model**, through vLLM. It adds DeBERTa model, pooling and request-processing plugins, with Docker images for NVIDIA GPUs and x86-64 CPUs.

{{< button href="https://github.com/maxdswain/vllm-gliner" >}}GitHub repository{{< /button >}}

## Model serving

- **Entity extraction over HTTP:** expose schema-based extraction through `/pooling`, including character spans, confidence scores and token usage.
- **Efficient inference:** integrate DeBERTa attention kernels, model pooling and IO processing with vLLM's serving infrastructure.
- **CPU and GPU deployments:** provide model-preparation tooling and Docker Compose configurations for both environments.

These serving capabilities are supplied by the project's vLLM plugins.

## Decision models

**GLiNER2.5 Decide** turns text into structured decisions rather than generated prose. I added an opt-in endpoint plugin for the OpenAI-compatible `/v1/decisions` API and vLLM's `/v1/systemone` API, answering multiple classification questions in a single model pass.

The Decisions API supports choices, predicate probabilities and scores—for example, identifying a support request's intent, whether it asks for cancellation, and its urgency together. Decide uses a closed-set classification head, not an autoregressive language-model vocabulary, and also remains accessible through `/pooling`.

## Companion project: gliner-haystack

[**gliner-haystack**](https://github.com/maxdswain/gliner-haystack) connects the inference server to Haystack pipelines. Its text and document extractors accept labels at runtime, return entity spans and confidence scores, and enrich new documents without changing their existing text or metadata.

For example, a Haystack indexing pipeline can tag entities before it writes documents to a store:

{{< mermaid >}}
sequenceDiagram
    accTitle: Entity extraction in a Haystack pipeline
    accDescr: The document extractor sends text and entity labels to a separate GLiNER server, then returns copies of the documents with entity metadata.
    participant P as Pipeline
    participant H as Document extractor
    participant V as gliner via vLLM
    P->>H: Documents + labels
    H->>V: POST /pooling
    V-->>H: Spans + scores
    H-->>P: Enriched documents
{{< /mermaid >}}

`GLiNERDocumentExtractor` enriches documents; `GLiNERTextExtractor` returns entities for a text input without creating a document. Both are clients of the inference server. Document processing can also run asynchronously with bounded concurrency while preserving input order.

- [Serving code and deployment examples](https://github.com/maxdswain/vllm-gliner#readme)
- [Haystack components and pipeline examples](https://github.com/maxdswain/gliner-haystack#readme)
