<!-- ===================== HEADER ===================== -->
<div align="center">

<p>
  <a href="https://jayaremala.com"><img src="https://img.shields.io/badge/Portfolio-jayaremala.com-26d0ce?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Portfolio"/></a>
  <a href="https://linkedin.com/in/jayasabarishreddyr"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
  <a href="mailto:jr6421@nyu.edu"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>
  <img src="https://img.shields.io/badge/Qualcomm_Edge_AI-Hackathon_Winner-FF6F00?style=for-the-badge&logo=qualcomm&logoColor=white" alt="Qualcomm Edge AI Hackathon Winner"/>
</p>

<a href="https://github.com/sabarishreddy99?tab=followers"><img src="https://komarev.com/ghpvc/?username=sabarishreddy99&label=Profile%20views&color=26d0ce&style=flat" alt="profile views"/></a>

</div>

<!-- ===================== ABOUT ===================== -->
## About


I build AI systems that have to hold up when real traffic hits them.

I'm Jaya, a software engineer, AI/ML with 5+ years shipping production systems, the last two focused on LLM applications that hold up outside a notebook. At NYU I took a multi-agent research platform from prototype to daily cross-institutional use, serving self-hosted Llama 3.1 70B over millions of records. Just as much of that year went into the unglamorous half: grading answer quality against held-out query sets on NDCG@10, MAP, MRR and precision@k, tracing multi-hop tool-call chains to the failing span, and holding 99.9% uptime at 3,000+ RPS while cutting P99 latency 78%.


- Took a **multi-agent research platform** from prototype to daily cross-institutional use at NYU, serving self-hosted **Llama 3.1 70B** over millions of papers.
- Raised answer quality **40%** with hybrid retrieval (**BGE-M3** + BM25 fused by Reciprocal Rank Fusion), graded before and after against held-out query sets on NDCG@10 and precision@k.
- Held **99.9% uptime at 3,000+ RPS** through 3× load spikes, and cut **P99 latency 78%** (450ms → under 100ms).
- Spent two years in Bengaluru embedded as the external engineering partner to **Shell PLC**, moving **115GB/day** from 200+ offshore stations with **zero data loss** and exactly-once semantics.
- Pushed LLM inference to **15ms on a Snapdragon NPU**, 10× faster than the cloud baseline — **Qualcomm Edge AI Hackathon winner**.
- **M.S. Computer Science, NYU Tandon** (GPA 3.8) · TA for Machine Learning and Data Structures & Algorithms, 50+ students per course.

> My portfolio is itself an agent you can talk to — **Avocado AI**, running a public MCP server → **[jayaremala.com](https://jayaremala.com/)**

Four things I have taken from 0 to 1 as sole or founding engineer:
- gradeVITian, a consumer web app at 17,000+ MAU and 20,000+ accounts, #2 on Google, still in production six years later
- Avocado AI, a public Model Context Protocol server any Claude or Cursor client can consume, over a 4-stage hybrid retrieval pipeline
- Tailorbird, an agent orchestrator that cut inference cost per job from $1.23 to $0.92 by priming one session and forking prompt-cached children
- SnapLog, a QLoRA-fine-tuned Llama 3.2 3B served at 15ms on-device, 10x faster than the cloud baseline (Qualcomm Edge AI Hackathon winner)

<!-- ===================== FEATURED PROJECTS ===================== -->
## Featured Projects

### [Tailorbird](https://github.com/sabarishreddy99/tailorbird) — autonomous résumé tailoring
A deterministic Python orchestrator that turns a job URL into a tailored one-page résumé, driving a **coding agent headlessly**. Pluggable ATS adapters (Greenhouse, Ashby, Lever, Workday, Workable, Apple, Amazon, Oracle), a regex eligibility screen that costs **zero tokens**, `flock`-guarded concurrent commits, and a stdlib web tracker with live log streaming.

**Cut inference cost per job from $1.23 to $0.92 and fresh tokens from 77k to 42k** by loading the agent skill once into a primed session and forking a prompt-cached child per job.

`Python` `Claude Code CLI (headless)` `MCP` `AsyncIO` `FastAPI` `headless Chrome`

### [Avocado AI](https://github.com/sabarishreddy99/jayaremala) · [Live](https://jayaremala.com/chat) — agent-native platform with a public MCP server
A portfolio fronted by a streaming agentic assistant, over a **4-stage hybrid retrieval pipeline**: query expansion → dense vector search (ChromaDB) → BM25 → **Reciprocal Rank Fusion**. Every tool is exposed through a **public Model Context Protocol server** any Claude or Cursor client can consume — read-only, token-gated and rate-limited. Multi-provider routing (Gemini → Groq → OpenRouter) fails over on cost and availability.

`FastAPI` `MCP (FastMCP)` `ChromaDB` `BM25` `RRF` `HyDE` `Next.js` `Docker` `AWS`

### [CodeCollab](https://github.com/sabarishreddy99/CodeCollab) — real-time collaborative editor + code retrieval
Conflict-free multi-user editing with **Yjs CRDTs** over WebSockets and a Redis presence layer, horizontally scaled behind Nginx. Its retrieval half raised **code retrieval relevance 65%** over naive context windows by chunking source at **AST scope level** and embedding each scope with Voyage-Code-2, measured against a fixed baseline query set.

`Node.js` `Yjs CRDT` `WebSockets` `Redis` `Voyage-Code-2` `Docker`

### SnapLog — on-device LLM inference · *Qualcomm Edge AI Hackathon winner*
A **QLoRA**-fine-tuned Llama 3.2 3B served at **15ms on-device** through 4-bit **AWQ** quantization on **ONNX Runtime** — 10× faster than the cloud baseline it was benchmarked against. An offline-first SQLite buffer keeps ingestion lossless through network partitions.

`QLoRA` `AWQ` `ONNX Runtime` `Llama 3.2 3B` `Snapdragon NPU` `FastAPI`

### GeneCart — AI-assisted genomics discovery · *NYU CAS, in production use*
Search and discovery over large scientific corpora, owned end to end across the API, the agent layer, the data model and the AWS infrastructure. The agent is scoped to a fixed set of **least-privilege server-side tools**, so interpreted intent can never issue an unbounded write, with a human retaining final authority over sensitive genomic data.

`LangGraph` `FastAPI` `PostgreSQL` `pgvector` `React` `AWS` `Kubernetes` `Terraform`

### [gradeVITian](https://gradevitian.jayaremala.com) · [GitHub](https://github.com/sabarishreddy99/gv-official) — consumer web, six years live
Built from idea to production as sole engineer: **17,000+ monthly active users**, **20,000+ accounts**, **#2 on Google** through programmatic SEO, tuned against Core Web Vitals as a PWA with service workers. Still running six years later, since rebuilt on Next.js and FastAPI.

`Next.js` `FastAPI` `PHP` `MySQL` `PWA` `Technical SEO`

<!-- ===================== EXPERIENCE ===================== -->
## Experience

| Where | Role | What it produced |
|---|---|---|
| **NYU CAS — Genomics & Systems Biology** | Software Engineer · Jun 2025 – present | GeneCart: agent layer, API contracts, Terraform-provisioned AWS |
| **NYU IT — High-Speed Research Network** | Software Engineer, Research Infrastructure | +40% answer quality · P99 −78% · 99.9% @ 3,000+ RPS · deploy lead time −65% |
| **Wipro** *(client: Shell PLC)* | Software Engineer, embedded partner · Bengaluru | 115GB/day zero data loss · fault tolerance +39% · service requests −45% |
| **Vellore Institute of Technology** | Full Stack Developer | gradeVITian → 17K+ MAU, 20K+ accounts, #2 on Google |

<!-- ===================== STACK ===================== -->
## Stack

**Languages** Python · Java · TypeScript · JavaScript · SQL · Bash

**AI & agents** LangGraph · Model Context Protocol (MCP, FastMCP) · RAG · vector search (ChromaDB, FAISS, pgvector) · embeddings (BGE-M3, Voyage-Code-2) · hybrid search + Reciprocal Rank Fusion · prompt & context engineering · QLoRA fine-tuning · AWQ quantization · ONNX Runtime · Claude Code and Cursor daily

**Backend & data** FastAPI · Spring Boot · Django · Node.js · REST · gRPC · GraphQL · Apache Kafka (exactly-once, DLQ, schema-registry governance) · PostgreSQL · Redis · DynamoDB · Elasticsearch · Spark · Airflow · dbt · Snowflake

**Cloud & reliability** AWS (ECS, EKS, Lambda, S3, SQS) · Kubernetes · Docker · Terraform · Ansible · CI/CD · blue-green deploys · Datadog · Grafana · Prometheus · distributed tracing · on-call and incident RCA

<div align="center">

<img height="170" src="https://github-readme-stats.vercel.app/api?username=sabarishreddy99&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true" alt="GitHub Stats"/>
<img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=sabarishreddy99&layout=compact&theme=tokyonight&hide_border=true&langs_count=8" alt="Top Languages"/>

</div>

<!-- ===================== CONNECT ===================== -->
## Let's build something

Open to **AI engineering, applied AI, and backend** roles where the work is production rather than prototype and to forward-deployed work, which is what the two years embedded at Shell actually were.

<div align="center">

<a href="https://jayaremala.com/chat"><img src="https://img.shields.io/badge/Talk_to_my_AI-jayaremala.com-26d0ce?style=for-the-badge&logo=openai&logoColor=white" alt="Talk to my AI"/></a>
<a href="https://linkedin.com/in/jayasabarishreddyr"><img src="https://img.shields.io/badge/Connect-LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
<a href="mailto:jr6421@nyu.edu"><img src="https://img.shields.io/badge/Reach_out-Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>

</div>
