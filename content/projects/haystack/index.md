---
title: "Haystack contributions"
description: "Contributions to Haystack’s retrieval and document pipelines: read-only graph queries, sparse and multivector embeddings, and Gotenberg conversion."
summary: "Graph retrieval, embeddings and document conversion for Haystack, deepset’s open-source agent framework."
weight: 10
featureimage: "project-logos/haystack.svg"
showBreadcrumbs: true
---

{{< lead >}}
I contribute to Haystack, deepset’s open-source agent framework. My work focuses on how agents retrieve evidence from documents and knowledge graphs.
{{< /lead >}}

{{< keywordList >}}
{{< keyword icon="skill-python" >}}Python{{< /keyword >}}
{{< keyword icon="skill-haystack" >}}Haystack{{< /keyword >}}
{{< keyword icon="fork" >}}GraphRAG{{< /keyword >}}
{{< keyword icon="skill-grpc" >}}gRPC{{< /keyword >}}
{{< /keywordList >}}

<div class="mt-4 flex">
{{< button href="https://github.com/deepset-ai/haystack" >}}Haystack on GitHub{{< /button >}}
</div>

## Selected contributions

- **Graph retrieval.** I built a FalkorDB retriever that uses the graph schema to translate natural-language questions into read-only Cypher queries. I also extended the document store to write graph labels and relationships from document metadata at indexing time. Agents can then query those relationships without modifying the graph.
- **Embeddings.** I added SPLADE sparse embedders and gRPC support for Hugging Face Text Embeddings Inference, including streaming document batches. SPLADE represents text as weighted terms for search. For models that instead produce a vector per token, I built vLLM multivector embedders for both queries and documents, preserving fine-grained matches between a question and a passage.
- **Document processing.** I authored the Gotenberg integration so Haystack pipelines can convert source documents to PDF through a separate service before parsing and indexing them. I extended OpenDataLoader PDF to return embedded images as Haystack documents, so figures can be retrieved alongside text. I also added asynchronous metadata extraction and concurrent embedding requests for document pipelines.
