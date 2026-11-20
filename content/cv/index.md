---
title: "Curriculum vitae"
description: "Senior AI Engineer — experience, selected projects and technical skills."
draft: false
showDate: false
showDateUpdated: false
showAuthor: false
showAuthorBottom: false
showReadingTime: false
showReadingProgress: false
showWordCount: false
showPagination: false
showTableOfContents: false
showBreadcrumbs: false
showTaxonomies: false
showComments: false
showHero: false
sharingLinks: false
---

{{< lead >}}
Senior AI Engineer building secure, scalable AI platforms and tools that make complex engineering work simpler.
{{< /lead >}}

{{< icon "location-dot" >}} Edinburgh, UK · [{{< icon "github" >}} GitHub](https://github.com/maxdswain) · [{{< icon "linkedin" >}} LinkedIn](https://www.linkedin.com/in/maxdswain/)

## Experience

{{< timeline >}}

{{< timelineItem header="Senior AI Engineer" subheader="Leonardo · Edinburgh" badge="Apr 2025 – Present" icon="leonardo" md=true >}}

Own the internal AI platform and lead its delivery across engineering teams. Work alongside engineers to understand their workflows. Release early versions, then interview both frequent and infrequent users to understand what usage figures alone cannot explain. Guide architecture decisions and mentor engineers through deployment.

- **Model access and permissions.** Built a Go gateway that routes requests to self-hosted models and Azure AI Foundry. It authenticates users, enforces rate limits and controls which tools each user and agent may call, adding **less than a millisecond of gateway overhead**.
- **Agent tools.** Developed multi-agent systems and built tool-using agents with Pydantic AI, handling tool calls through the OpenAI Responses API. Wrote three multi-user Model Context Protocol (MCP) servers in Go and Python to connect agents to CloudBees and Bitbucket.
- **Retrieval and evaluation.** Led delivery of a self-hosted GraphRAG chatbot that combines semantic retrieval with graph context for sensitive documents. Measured how highly the retriever ranked relevant documents using Haystack’s NDCG metric. Used DeepEval regression tests and custom evaluations to check agent behaviour as prompts changed.
- **Inference.** Served language, vision-language, embedding, entity extraction and decision models using vLLM and Text Embeddings Inference (TEI). Extended vLLM and tuned serving configurations, including speculative decoding and parallel inference.
- **Production operations.** Instrumented the gateway and AI services with Prometheus and Grafana; used GlitchTip to trace requests and investigate application errors. Introduced fortnightly releases across Azure and on-premises Kubernetes, with automated checks in CloudBees and rolling, zero-downtime updates through Argo CD.
- **Engineering workflows.** Built pipelines to extract, clean and join data, increasing synthetic-data generation speed by approximately **30×**. Consolidated signal reading and processing into one installable tool that ran faster than real time and approximately **15×** faster than the previous workflow.

{{< /timelineItem >}}

{{< timelineItem header="AI Engineer" subheader="Leonardo · Edinburgh" badge="Sep 2024 – Mar 2025" icon="leonardo" md=true >}}

Led the rollout of AI applications to **hundreds of internal engineers**. The applications served tens of thousands of requests a day with no downtime during working hours.

- Served as technical lead for full-stack engineering applications. Built FastAPI services backed by Elasticsearch, MongoDB and PostgreSQL, and improved testing and performance as the applications scaled.
- Wrote high-performance readers for complex proprietary formats so engineers could process existing datasets. Developed synthetic-data generators for AI training.
- Owned and administered the AI/ML team’s Azure infrastructure and the developer workstations used by engineers across the business.

{{< /timelineItem >}}

{{< timelineItem header="Graduate Systems Engineer" subheader="Leonardo · Edinburgh" badge="Sep 2023 – Aug 2024" icon="leonardo" md=true >}}

Completed Leonardo’s accelerated 12-month graduate programme within the Global Combat Air Programme Data & AI/ML team.

- Led development of a system for querying, processing and serving large engineering datasets. This technical leadership earned a nomination for Leonardo’s 2024 innovation award.
- Wrote readers and processors for legacy formats and built extraction, transformation and loading (ETL) pipelines. Combined optical, radar and GPS records so engineers could analyse the sources together.
- Supported the team’s AI/ML infrastructure, maintaining and upgrading the systems used for engineering work.

{{< /timelineItem >}}

{{< timelineItem header="Mathematical Physics Research Intern" subheader="Lancaster University · Lancaster" badge="Jul 2022" icon="lancaster" md=true >}}

Co-developed a purely functional language for symbolic mathematics in Haskell, working on its parser and built-in functions.

- Implemented the parser that translated text into the Haskell data types used to represent expressions. Implemented arithmetic on both numbers and symbols, including exponentiation.
- Implemented built-in functions including `Type`, `Subs` and `Print`, and added support for user-defined mathematical functions. Used Git to collaborate on the language and Stack to automate builds and tests.

{{< /timelineItem >}}

{{< /timeline >}}

## Selected work

### [Haystack (deepset)](https://github.com/deepset-ai/haystack)

Contributed GraphRAG and FalkorDB text-to-Cypher retrieval, SPLADE sparse embedders and gRPC support for Hugging Face TEI. Built the Gotenberg document converter and improved asynchronous document-store operations and embedding throughput.

### [GLiNER model serving](https://github.com/maxdswain/vllm-gliner)

Built vLLM plugins to serve GLiNER on CPUs and GPUs, with a DeBERTa encoder and fused Triton attention. Added GLiNER2.5 Decide endpoints and Haystack components for entity extraction.

### [Code Executor MCP](https://github.com/maxdswain/code-executor-mcp)

Built a Go MCP server for stateful Python execution in isolated Docker sandboxes, with session-scoped packages, automatic cleanup and optional gVisor isolation.

### [splintr-go](https://github.com/maxdswain/splintr-go)

Created Go bindings for Splintr tokenisation, including parallel batch processing, bundled vocabularies and explicit native-resource cleanup.

## Technical skills

<div class="cv-skills">

### Languages

{{< keywordList >}}
{{< keyword icon="skill-python" >}}Python{{< /keyword >}}
{{< keyword icon="skill-go" >}}Go{{< /keyword >}}
{{< keyword icon="skill-typescript" >}}TypeScript{{< /keyword >}}
{{< keyword icon="skill-gnubash" >}}Bash{{< /keyword >}}
{{< keyword icon="skill-c" >}}C{{< /keyword >}}
{{< keyword icon="skill-haskell" >}}Haskell{{< /keyword >}}
{{< /keywordList >}}

### AI and retrieval

{{< keywordList >}}
{{< keyword icon="skill-vllm" >}}vLLM{{< /keyword >}}
{{< keyword icon="skill-sglang" >}}SGLang{{< /keyword >}}
{{< keyword icon="skill-pydantic" >}}Pydantic AI{{< /keyword >}}
{{< keyword icon="skill-docling" >}}Docling{{< /keyword >}}
{{< keyword icon="skill-haystack" >}}Haystack{{< /keyword >}}
{{< keyword icon="fork" >}}GraphRAG{{< /keyword >}}
{{< keyword icon="skill-deepeval" >}}DeepEval{{< /keyword >}}
{{< keyword icon="skill-azure" >}}Azure AI Foundry{{< /keyword >}}
{{< keyword icon="skill-modelcontextprotocol" >}}MCP{{< /keyword >}}
{{< /keywordList >}}

### Infrastructure

{{< keywordList >}}
{{< keyword icon="skill-azure" >}}Azure{{< /keyword >}}
{{< keyword icon="skill-linux" >}}Linux{{< /keyword >}}
{{< keyword icon="docker" >}}Docker{{< /keyword >}}
{{< keyword icon="skill-kubernetes" >}}Kubernetes{{< /keyword >}}
{{< keyword icon="skill-argo" >}}Argo CD{{< /keyword >}}
{{< keyword icon="list-check" >}}CI/CD{{< /keyword >}}
{{< keyword icon="skill-cloudbees" >}}CloudBees{{< /keyword >}}
{{< keyword icon="skill-jenkins" >}}Jenkins{{< /keyword >}}
{{< keyword icon="skill-githubactions" >}}GitHub Actions{{< /keyword >}}
{{< keyword icon="skill-prometheus" >}}Prometheus{{< /keyword >}}
{{< keyword icon="skill-grafana" >}}Grafana{{< /keyword >}}
{{< keyword icon="skill-sentry" >}}GlitchTip / Sentry{{< /keyword >}}
{{< /keywordList >}}

### Data and APIs

{{< keywordList >}}
{{< keyword icon="skill-fastapi" >}}FastAPI{{< /keyword >}}
{{< keyword icon="skill-grpc" >}}gRPC{{< /keyword >}}
{{< keyword icon="skill-postgresql" >}}PostgreSQL{{< /keyword >}}
{{< keyword icon="skill-mongodb" >}}MongoDB{{< /keyword >}}
{{< keyword icon="skill-elasticsearch" >}}Elasticsearch{{< /keyword >}}
{{< keyword icon="fork" >}}Graph databases{{< /keyword >}}
{{< /keywordList >}}

</div>

## Education

{{< timeline >}}

{{< timelineItem header="MPhys (Hons) — Theoretical Physics" subheader="Lancaster University · Lancaster" badge="Oct 2019 – Jul 2023" icon="lancaster" md=true >}}

**Grade:** First Class Honours.

**Master’s project:** Programmed a Metropolis–Hastings Markov chain Monte Carlo algorithm in C to sample the Boltzmann distribution, generating a classical distribution of hundreds of interacting dipolar atoms in a quadratic trapping potential. Combined this with CASINO variational and diffusion Monte Carlo algorithms to investigate supersolidity in dipolar atomic systems confined to traps.

**Modules included:**

- Advanced Electrodynamics and Gravity
- Advanced Relativity and Gravity
- Computer Modelling
- Gauge Theories
- Quantum information processing
- Semiconductor Device Physics

{{< /timelineItem >}}

{{< /timeline >}}
