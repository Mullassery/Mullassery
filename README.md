# 👋 Hi, I'm Georgi Mullassery

**MarTech Solutions Architect** | Customer Data Platforms • Data Engineering • AI Engineering | Bengaluru, India

[![Email](https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white)](mailto:mullassery@gmail.com)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/georgi-mullassery/)
[![Product Hunt](https://img.shields.io/badge/Product%20Hunt-DA552F?style=for-the-badge&logo=producthunt&logoColor=white)](https://www.producthunt.com/@georgi_mullassery/forums)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Mullassery)

## 🚀 About Me

Solutions Architect with 10+ years of experience designing and delivering enterprise-scale customer data, marketing technology, analytics, and AI-enabled solutions. Expertise in Customer Data Platforms (Adobe RT-CDP, Braze, mParticle, Segment CDP), event-driven architectures, cloud data platforms, customer journey orchestration, identity resolution, real-time activation, and data engineering on Google Cloud and Azure.

Outside of MarTech, I build systems-level software for fun — an AI-native operating system kernel and display stack written in Rust (the SHER OS family), plus a growing set of open-source Python and Rust developer tools.

- 🔭 **Current focus**: Customer Data Platforms, agentic AI systems, and Rust systems programming
- 🤖 **Exploring**: Autonomous code generation, RAG architectures, MCP-based agent tooling
- 🎓 **Background**: MBA, Jansons School of Business · B.Com, Mar Ivanios College

## 🔧 Technologies & Tools

**AI — Autonomous Code Generation**
Claude Code, Cursor, Replit, Codex, Hermes Agent, OpenCode, Loveable, OpenRouter

**AI — Agent Automation**
Temporal, Langflow, n8n + Node.js, FastAPI, Firecrawl, Tavily, SerpAPI, Twilio, Claude Agent SDK, OpenAI Agent SDK, Google Agent SDK, Ollama, Scheduled & Background Agents

**AI — RAG & Application Development**
LangChain, LangGraph, LlamaIndex, Chainlit / OpenWebUI, LangSmith, DSPy, BM25 + vector similarity + reranking, Context Engineering, Ragas + DeepEval, Pinecone, Weaviate, ChromaDB, pgvector, Qdrant, Milvus

**MCP & Model Platforms**
Model Context Protocol, Hugging Face, AWS Bedrock, Azure AI Foundry, GCP Vertex AI (Model Garden)

**Cloud & Data Platforms**
GCP, Azure, AWS · Google Cloud Storage, Azure Blob Storage / ADLS, Amazon S3, MinIO

**Data Warehousing & Engineering**
BigQuery, Snowflake, Databricks (PySpark), Microsoft Fabric, Azure Data Factory, Airbyte / Fivetran, dbt, Apache Airflow, Apache Kafka, Apache Flink (PyFlink), Hightouch / Reverse ETL, InfluxDB, Telegraf, Datadog

**Infrastructure as Code & Containers**
Terraform, Docker, Docker Compose, Azure Kubernetes Service (AKS), NGINX Ingress

**IoT, Messaging & Robotics**
Raspberry Pi 5, ESP32, MQTT (Eclipse / RabbitMQ), Node-RED, AWS IoT Core, AWS IoT SiteWise, CoAP, Edge Processing, Industrial IoT

**Identity & Security**
Entra ID / Azure AD, Azure Key Vault, Azure AI Search, incoming/outgoing guardrails

## 🌟 Featured Projects

### 🧠 [SHER OS](https://github.com/Mullassery/SHER-KERNEL) — AI-native operating system
An alternative to the Linux kernel: zero-trust security, isolated driver runtime, Linux kernel interface. Phases 0–5 complete, 21K+ lines of production Rust. Companion subsystems: [SHER-Graphics](https://github.com/Mullassery/SHER-Graphics) (software GPU + Vulkan/MoltenVK backend), [SHER-Display](https://github.com/Mullassery/SHER-Display) (compositor & window manager), [SHER-INPUT](https://github.com/Mullassery/SHER-INPUT) (input subsystem), [SHER-Aurora](https://github.com/Mullassery/SHER-Aurora) (GNOME-style design system).

### 🌉 [TinyBridge](https://github.com/Mullassery/TinyBridge) — macOS-native Linux VM runtime
Built on Apple's Virtualization.framework. Boots a real Ubuntu guest to a working login via a genuine Rust → C ABI → Swift call chain, with cloud-init-provisioned credentials.

### 🐍 Python & Rust developer tools
A growing suite of focused, single-purpose tools spanning robotics data ([PyRoboFrames](https://github.com/Mullassery/PyRoboFrames), [PyRoboSimulator](https://github.com/Mullassery/PyRoboSimulator)), dependency auditing ([PyDependencyCheck](https://github.com/Mullassery/PyDependencyCheck), [PyAPICheck](https://github.com/Mullassery/PyAPICheck)), and runtime state tagging ([PyTagManager](https://github.com/Mullassery/PyTagManager)).

## 📂 All Repositories

<details>
<summary>SHER OS platform (AI-native operating system, Rust)</summary>

| Repo | Description |
|---|---|
| [SHER-KERNEL](https://github.com/Mullassery/SHER-KERNEL) | AI-native OS kernel — zero-trust security, isolated driver runtime, Linux kernel interface |
| [SHER-Graphics](https://github.com/Mullassery/SHER-Graphics) | Software GPU simulation + real Vulkan/MoltenVK backend |
| [SHER-Display](https://github.com/Mullassery/SHER-Display) | Display server, compositor, and window manager |
| [SHER-INPUT](https://github.com/Mullassery/SHER-INPUT) | Input subsystem — canonical event stream for Display and Aurora |
| [SHER-Aurora](https://github.com/Mullassery/SHER-Aurora) | GNOME-style design system: tokens, typography, motion, accessibility |
| [SHER-Process-Explorer](https://github.com/Mullassery/SHER-Process-Explorer) | Evidence-based Linux process explorer — /proc telemetry, eBPF sampling, daemon + CLI + desktop UI |

</details>

<details>
<summary>Systems & runtimes</summary>

| Repo | Description |
|---|---|
| [TinyBridge](https://github.com/Mullassery/TinyBridge) | macOS-native Linux VM runtime on Apple's Virtualization.framework |
| [PrismNote](https://github.com/Mullassery/PrismNote) | Jupyter-compatible data-science notebook with built-in AI |
| [homebrew-tinybridge](https://github.com/Mullassery/homebrew-tinybridge) | Homebrew tap for TinyBridge |
| [homebrew-prismnote](https://github.com/Mullassery/homebrew-prismnote) | Homebrew tap for PrismNote |

</details>

<details>
<summary>LLM & AI tooling</summary>

| Repo | Description |
|---|---|
| [PyTokenCalc](https://github.com/Mullassery/PyTokenCalc) | Token counting & cost estimation across 20+ LLM providers |
| [PyInferenceManager](https://github.com/Mullassery/PyInferenceManager) | Multi-provider LLM inference executor — 11+ providers, batching, load testing |
| [PyStreamMCP](https://github.com/Mullassery/PyStreamMCP) | Query planning & context discovery for AI agents — 60–75% token reduction |
| [PyVectorHound](https://github.com/Mullassery/PyVectorHound) | Diagnostic engine for RAG retrieval failures |
| [PyStreamPDF](https://github.com/Mullassery/PyStreamPDF) | Selective PDF extraction to cut RAG costs 50–70% |
| [OpenAnchor](https://github.com/Mullassery/OpenAnchor) | Token intelligence middleware for multi-provider LLM usage |

</details>

<details>
<summary>Data engineering & quality</summary>

| Repo | Description |
|---|---|
| [PyDependencyCheck](https://github.com/Mullassery/PyDependencyCheck) | Dependency intelligence for Python — supply chain integrity |
| [PyAirflowTester](https://github.com/Mullassery/PyAirflowTester) | Airflow & dbt reliability and quality-assurance platform |
| [StatGuardian](https://github.com/Mullassery/StatGuardian) | Declarative data quality framework (Rust) — 13x faster than pandera |
| [PyReverseETL](https://github.com/Mullassery/PyReverseETL) | Quality-validated reverse ETL with lineage tracking |
| [PyBeamGuard](https://github.com/Mullassery/PyBeamGuard) | Apache Beam & Dataflow pipeline analysis and cost forecasting |
| [PyStreamXL](https://github.com/Mullassery/PyStreamXL) | Stream large Excel files with constant memory — 46x faster than openpyxl |
| [PySynthData](https://github.com/Mullassery/PySynthData) | Synthetic data generation for ML training |
| [PyWeatherEnriched](https://github.com/Mullassery/PyWeatherEnriched) | Weather data enrichment for ML pipelines |
| [PyNetworkIntel](https://github.com/Mullassery/PyNetworkIntel) | Network discovery, topology mapping, anomaly detection |

</details>

<details>
<summary>Robotics & simulation</summary>

| Repo | Description |
|---|---|
| [PyRoboFrames](https://github.com/Mullassery/PyRoboFrames) | High-performance ML dataloader for robotics (LeRobot format, Apple Silicon) |
| [PyRoboReplay](https://github.com/Mullassery/PyRoboReplay) | Robotics perception and replay engine — sensor fusion, trajectory analysis |
| [PyRoboSimulator](https://github.com/Mullassery/PyRoboSimulator) | World simulator for autonomous systems — 100K+ agents, REST API |
| [PyRoboVision](https://github.com/Mullassery/PyRoboVision) | Perception stack for autonomous robots & vehicles |
| [PyTerrainMap](https://github.com/Mullassery/PyTerrainMap) | Unified terrain intelligence for multi-robot fleets |

</details>

<details>
<summary>Analytics, MarTech & security</summary>

| Repo | Description |
|---|---|
| [PyTagManager](https://github.com/Mullassery/PyTagManager) | AI-native analytics implementation — semantic DOM graph to GTM/GA4/Segment/etc. |
| [ClusterAudienceKit](https://github.com/Mullassery/ClusterAudienceKit) | Enterprise audience intelligence — RFM, clustering, CLV, churn detection |
| [PyAPICheck](https://github.com/Mullassery/PyAPICheck) | Transparent API security discovery and policy generation |

</details>

## 📫 Reach Me

- 📧 [mullassery@gmail.com](mailto:mullassery@gmail.com)
- 📍 Bengaluru, India
- 💼 [LinkedIn](https://www.linkedin.com/in/georgi-mullassery/)
- 🚀 [Product Hunt](https://www.producthunt.com/@georgi_mullassery/forums)
- 🔗 [github.com/Mullassery](https://tinyurl.com/georgi-github)

**Thanks for stopping by — always happy to talk CDPs, data platforms, agentic AI, or Rust systems programming.**
