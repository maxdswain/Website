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

Lead AI architecture and delivery across engineering teams, owning internal AI infrastructure and supporting services.

- Built a self-hosted GraphRAG chatbot for sensitive documents, with DeepEval regression tests and retrieval evaluation using Haystack NDCG.
- Built a Go AI gateway for self-hosted and Azure AI Foundry models with enterprise authentication, rate limits and tool permissions, adding **sub-millisecond overhead**.
- Serve language and embedding models using vLLM and TEI; built multi-agent systems and three multi-user MCP servers. Improved synthetic-data generation by approximately **30×** and signal-processing workflows by **15×**.
- Coordinate delivery across Azure and on-premises infrastructure using CloudBees, Kubernetes and Argo CD, with automated testing and zero-downtime updates. Provide technical and architectural guidance and mentor engineers.

{{< /timelineItem >}}

{{< timelineItem header="AI Engineer" subheader="Leonardo · Edinburgh" badge="Sep 2024 – Mar 2025" icon="leonardo" md=true >}}

- Led the rollout of AI applications to hundreds of internal engineers, serving tens of thousands of requests daily with no downtime during working hours.
- Built FastAPI services integrated with Elasticsearch, MongoDB and PostgreSQL; improved testing, performance, robustness and scalability.
- Built high-performance readers for proprietary engineering data and synthetic-data generators for AI training.
- Owned and administered the AI/ML team's Azure cloud infrastructure and developer workstations used across the business.

{{< /timelineItem >}}

{{< timelineItem header="Graduate Systems Engineer" subheader="Leonardo · Edinburgh" badge="Sep 2023 – Aug 2024" icon="leonardo" md=true >}}

Completed Leonardo’s accelerated 12-month graduate programme within the Global Combat Air Programme Data & AI/ML team.

- Led development of a system to query, process and serve engineering datasets, earning a nomination for the 2024 innovation award.
- Built readers, processors and ETL pipelines for legacy data in proprietary formats, combining optical, radar and GPS sources to support engineering analysis.
- Supported, maintained and upgraded AI/ML infrastructure.

{{< /timelineItem >}}

{{< timelineItem header="Mathematical Physics Research Intern" subheader="Lancaster University · Lancaster" badge="Jul 2022" icon="lancaster" md=true >}}

Worked in a team to build a new purely functional, symbolic programming language in Haskell.

- Implemented a parser that converts text into the language's Haskell data types.
- Added arithmetic on numbers and symbols—multiplication, addition, subtraction and exponentiation—alongside symbolic functions including `Type`, `Subs` and `Print`, and support for custom mathematical functions.
- Used Git for source control and Stack to build and test the language.

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
