# 👋 Hi, I'm Georgi Mullassery

**MarTech Solutions Architect** | Customer Data Platforms • Data Engineering • AI Engineering | Bengaluru, India

[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mullassery@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/georgi-mullassery/)
[![Product Hunt](https://img.shields.io/badge/Product%20Hunt-DA552F?style=for-the-badge&logo=producthunt&logoColor=white)](https://www.producthunt.com/@georgi_mullassery/forums)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Mullassery)

## 🚀 About Me

Solutions Architect with more than a decade of work experience across IBM, Wipro, IPG Mediabrands, and others, designing and delivering enterprise-scale customer data, marketing technology, analytics, and AI-enabled solutions. Expertise in Customer Data Platforms (Adobe RT-CDP, Braze, mParticle, Segment CDP), event-driven architectures, cloud data platforms, customer journey orchestration, identity resolution, real-time activation, and data engineering on Google Cloud and Azure.

I build open-source tools that solve practical problems around running a Customer Data Platform in production — tag/analytics implementation, audience intelligence, reverse ETL, and the data-pipeline reliability that CDPs depend on. Outside of MarTech, I also build systems-level software in Rust for fun, including an from-scratch AI-native OS kernel (the SHER OS family).

- 🔭 **Current focus**: Customer Data Platforms, marketing data pipelines, and the tooling that keeps them reliable
- 🤖 **Exploring**: Agentic AI for MarTech workflows, RAG architectures, MCP-based agent tooling
- 🎓 **Background**: MBA, Jansons School of Business · B.Com, Mar Ivanios College

## 🔧 Technologies & Tools

**MarTech & Customer Data Platforms**
Adobe RT-CDP, Braze, mParticle, Segment CDP, customer journey orchestration, identity resolution, real-time activation, Hightouch / Reverse ETL

**Data Warehousing & Engineering**
BigQuery, Snowflake, Databricks (PySpark), Microsoft Fabric, Azure Data Factory, Airbyte / Fivetran, dbt, Apache Airflow, Apache Kafka, Apache Flink (PyFlink), InfluxDB, Telegraf, Datadog

**Cloud & Data Platforms**
GCP, Azure, AWS · Google Cloud Storage, Azure Blob Storage / ADLS, Amazon S3, MinIO

**AI — RAG & Application Development**
LangChain, LangGraph, LlamaIndex, Chainlit / OpenWebUI, LangSmith, DSPy, BM25 + vector similarity + reranking, Context Engineering, Ragas + DeepEval, Pinecone, Weaviate, ChromaDB, pgvector, Qdrant, Milvus

**AI — Agent Automation**
Temporal, Langflow, n8n + Node.js, FastAPI, Firecrawl, Tavily, SerpAPI, Twilio, Claude Agent SDK, OpenAI Agent SDK, Google Agent SDK, Ollama, Scheduled & Background Agents

**AI — Autonomous Code Generation**
Claude Code, Cursor, Replit, Codex, Hermes Agent, OpenCode, Loveable, OpenRouter

**MCP & Model Platforms**
Model Context Protocol, Hugging Face, AWS Bedrock, Azure AI Foundry, GCP Vertex AI (Model Garden)

**Infrastructure as Code & Containers**
Terraform, Docker, Docker Compose, Azure Kubernetes Service (AKS), NGINX Ingress

**Identity & Security**
Entra ID / Azure AD, Azure Key Vault, Azure AI Search, incoming/outgoing guardrails

**IoT, Messaging & Robotics**
Raspberry Pi 5, ESP32, MQTT (Eclipse / RabbitMQ), Node-RED, AWS IoT Core, AWS IoT SiteWise, CoAP, Edge Processing, Industrial IoT

## 📂 Open Source, by category

Every project below links straight to its **Use Cases** section — the fastest way to see whether it solves a problem you actually have. Status is described plainly: if something is early-stage or has known gaps, it says so.

### 🎯 MarTech & Customer Data (flagship)

| Repo | What it does |
|---|---|
| [PyTagManager](https://github.com/Mullassery/PyTagManager#use-cases) | Crawls a site, builds a semantic DOM graph, and generates/exports analytics-tracking configs (GTM, GA4, Segment, and others) — then drives a real headless browser to verify the tracking actually fires correctly at runtime, not just that the config looks right. |
| [ClusterAudienceKit](https://github.com/Mullassery/ClusterAudienceKit#use-cases) | Customer segmentation engine (Rust core + Python bindings): RFM analysis, multiple clustering algorithms, churn/CLV scoring, and streaming segmentation with drift detection. |
| [PyReverseETL](https://github.com/Mullassery/PyReverseETL#use-cases) | Moves data from warehouses/databases to CRM and marketing-automation destinations with real PII masking and a recorded lineage graph — the activation counterpart to CDP ingestion. |
| [MessageBirds](https://github.com/Mullassery/MessageBirds) | Customer data platform infrastructure: Kafka-based event streaming, Postgres storage, an edge ingest gateway, and SDKs across web, iOS, and Python. |

### ✅ Data Pipeline Reliability & Quality

| Repo | What it does |
|---|---|
| [PyAirflowTester](https://github.com/Mullassery/PyAirflowTester#use-cases) | Static analysis for Airflow DAGs and dbt manifests, plus dependency-intelligence (blast radius, risk scoring) and an optional web dashboard. |
| [StatGuardian](https://github.com/Mullassery/statguardian#real-world-use-cases) | Rust data-quality engine with a custom `.sg` validation DSL — schema validation, drift detection, anomaly detection. |
| [PyBeamGuard](https://github.com/Mullassery/PyBeamGuard#use-cases) | Static analysis for Apache Beam/Flink/Spark pipelines — flags hot keys, shuffle bottlenecks, and cost risks before deployment. |
| [PyDBTGuard](https://github.com/Mullassery/PyDBTGuard) | Scores dbt tests for reliability, cost, and blast radius from static manifest metadata — early-stage project. |
| [PyDependencyCheck](https://github.com/Mullassery/PyDependencyCheck#use-cases) | Python dependency vulnerability scanning, health scoring, and SBOM generation. |
| [PyNetworkIntel](https://github.com/Mullassery/PyNetworkIntel#use-cases) | Lightweight LAN network discovery, topology mapping, and vulnerability scanning — dependency-free by design. |
| [PyStreamXL](https://github.com/Mullassery/PyStreamXL#use-cases) | Streams large `.xlsx` files row-by-row in constant memory (Rust-backed), with streaming writes and formula/comment extraction. |
| [PySynthData](https://github.com/Mullassery/PySynthData#use-cases) | Generates synthetic relational datasets from a schema, with differential-privacy noise injection and referential-integrity-aware row generation. |
| [PyWeatherEnriched](https://github.com/Mullassery/PyWeatherEnriched#use-cases) | Geocodes a location and fetches real historical weather data, then engineers climate features (rolling stats, degree-days, anomaly z-scores) for ML pipelines. |

### 🤖 LLM & AI Tooling

| Repo | What it does |
|---|---|
| [PyTokenCalc](https://github.com/Mullassery/PyTokenCalc#real-world-use-cases) | Token counting and cost estimation across 10+ LLM provider tokenizers (OpenAI, Anthropic, Google, Cohere, Azure, HuggingFace, Ollama, and more). |
| [PyInferenceManager](https://github.com/Mullassery/PyInferenceManager#use-cases) | Multi-provider LLM inference orchestrator (Anthropic, OpenAI, Gemini, Ollama, vLLM) with cost tracking, retries, and circuit-breaking. |
| [PyStreamMCP](https://github.com/Mullassery/PyStreamMCP#use-cases) | Query planning and context discovery for AI agents — exposed as a Python SDK, REST API, and MCP tool server. |
| [PyVectorHound](https://github.com/Mullassery/PyVectorHound#use-cases) | Diagnostic layer for RAG/vector-search pipelines — computes retrieval-quality metrics and root-causes failures. |
| [PyStreamPDF](https://github.com/Mullassery/PyStreamPDF#real-world-use-cases) | PDFium-backed PDF library with token-budget-aware semantic chunking, aimed at reducing what gets sent to LLMs. |
| [PyAPICheck](https://github.com/Mullassery/PyAPICheck#use-cases) | Discovers API surface from OpenAPI/traffic, scores security risk with a named reason for every finding, and generates Cedar policy for enforcement. |
| [PyStreamAI](https://github.com/Mullassery/PyStreamAI) | ML deployment toolkit — canary/A-B routing, cost tracking, request scheduling, and ONNX Runtime inference. |
| [PyInterviewBot](https://github.com/Mullassery/PyInterviewBot) | Voice-AI interview platform: Rust gateway, Python AI service, JS client — early-stage, see its own README for current limitations. |
| [OpenAnchor](https://github.com/Mullassery/OpenAnchor) | Token intelligence middleware for multi-provider LLM usage. |
| [PyBlastRadius](https://github.com/Mullassery/PyBlastRadius) | Dependency-graph blast-radius analysis, criticality scoring, and failure-cascade simulation — Terraform discovery is real; Kubernetes/Airflow/OTLP sources are not yet wired up. |

### 🛠️ Systems & Runtimes

| Repo | What it does |
|---|---|
| [TinyBridge](https://github.com/Mullassery/TinyBridge#use-cases) | macOS-native Linux VM runtime on Apple's Virtualization.framework. macOS backend is real and working; Windows/Linux backends are unimplemented scaffolding. Installed via [Homebrew tap](https://github.com/Mullassery/homebrew-tinybridge), not PyPI. |
| [PrismNote](https://github.com/Mullassery/PrismNote#use-cases) | Jupyter-style data-science notebook: Rust/Axum backend, React frontend, real local SQL execution, and a Docker-sandboxed code executor. Installed via [Homebrew tap](https://github.com/Mullassery/homebrew-prismnote). |
| [MudFish](https://github.com/Mullassery/MudFish) | Async Rust web crawler (frontier, fetch, parser) with Python bindings via PyO3. |

### 🖥️ SHER OS — an AI-native operating system, built from scratch (Rust)

A multi-repo, in-development OS project outside the MarTech day job. Most subsystems are currently a deliberate **simulation layer** — real Rust code with real tests, but in-memory/userspace behavior rather than real hardware I/O or a bootable kernel. Each repo's own README states plainly what's real vs. simulated.

| Repo | What it does |
|---|---|
| [SHER-KERNEL](https://github.com/Mullassery/SHER-KERNEL#use-cases) | Core kernel scaffolding — object model, scheduling, memory, driver-lifecycle concepts, and a Linux Kernel Interface compatibility layer. |
| [SHER-Graphics](https://github.com/Mullassery/SHER-Graphics#use-cases) | GPU abstraction and rendering — software simulation plus a real, working Vulkan/MoltenVK backend. |
| [SHER-Display](https://github.com/Mullassery/SHER-Display#use-cases) | Display server, compositor, and window management. |
| [SHER-INPUT](https://github.com/Mullassery/SHER-INPUT#use-cases) | Canonical, backend-independent input event stream — real evdev backend on Linux, simulated backend for hardware-free testing. |
| [SHER-Aurora](https://github.com/Mullassery/aurora#use-cases) | GNOME-style design system — tokens, typography, motion, and an automated WCAG contrast audit. |
| [SHER-Process-Explorer](https://github.com/Mullassery/SHER-Process-Explorer#use-cases) | Evidence-based Linux process investigation tool — `/proc` telemetry, bpftrace integration, daemon + CLI + desktop UI. |

### 🦾 Robotics & Simulation

| Repo | What it does |
|---|---|
| [PyRoboFrames](https://github.com/Mullassery/PyRoboFrames#use-cases) | Rust-backed ML dataloader for robot-learning datasets — native LeRobot format support, Apple Silicon hardware video decode. |
| [PyRoboReplay](https://github.com/Mullassery/PyRoboReplay#real-world-use-cases) | Forensic-debugging and causal-analysis engine for autonomous robot mission replay. |
| [PyRoboSimulator](https://github.com/Mullassery/PyRoboSimulator) | World simulator for autonomous systems, with a FastAPI backend service — active development, see its own README for current test/CI status. |
| [PyRoboVision](https://github.com/Mullassery/PyRoboVision#use-cases) | Multi-object tracker (Kalman filter + Hungarian algorithm) and trajectory predictor for robot perception. |
| [PyTerrainMap](https://github.com/Mullassery/PyTerrainMap#use-cases) | Fuses multi-robot terrain observations into a spatial/temporal store, with H3 spatial indexing and SLAM. |

## 📫 Reach Me

- 📧 [mullassery@gmail.com](mailto:mullassery@gmail.com)
- 📍 Bengaluru, India
- 💼 [LinkedIn](https://www.linkedin.com/in/georgi-mullassery/)
- 🚀 [Product Hunt](https://www.producthunt.com/@georgi_mullassery/forums)
- 🔗 [github.com/Mullassery](https://tinyurl.com/georgi-github)

**Thanks for stopping by — always happy to talk CDPs, marketing data pipelines, or the tooling that makes them reliable.**
