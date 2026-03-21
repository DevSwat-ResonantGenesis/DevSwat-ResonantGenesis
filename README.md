<div align="center">

# RESONANT GENESIS

<h3>Enterprise-Grade Governed AI Agent Ecosystem &mdash; 40+ Microservices</h3>

<br>

[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Services](https://img.shields.io/badge/Services-42-8B5CF6.svg?style=for-the-badge)](#-platform-architecture)
[![Tools](https://img.shields.io/badge/Agent_Tools-130+-3B82F6.svg?style=for-the-badge)](#-key-numbers)
[![Providers](https://img.shields.io/badge/LLM_Providers-11-F59E0B.svg?style=for-the-badge)](#-ai--llm)
[![DSID-P](https://img.shields.io/badge/Identity-DSID--P-EF4444.svg?style=for-the-badge)](#-blockchain--identity)
[![Open Source](https://img.shields.io/badge/Open_Source-100%25-10B981.svg?style=for-the-badge)](#-get-started)

<br>

> **Created by [Louie Nemesh](#-the-creator).**
> **Started November 11, 2025.**

<br>

</div>

---

<br>

## What is Resonant Genesis?

**Resonant Genesis** is a full-stack production platform for governed autonomous AI agents. Not a chatbot wrapper. Not a prompt playground.

Agents operate under **cryptographic identity** (DSID-P with Ed25519 signatures), **multi-layer governance** (6-layer MAGM policy engine evaluated before every action), **5-pillar trust scoring** (T1 Restricted → T5 Platinum), and **immutable blockchain audit trails** with Raft consensus.

Memory is stored in the **Hash Sphere** — a 9-layer coordinate system that maps content to 3D semantic space using resonance hashing, anchor energy fields, and hybrid multi-method extraction.

The entire platform is **open source** — 41 repositories, 42 Docker services, every component individually deployable.

<br>

---

<br>

## &#x1F3D7; Platform Architecture

```
                        ┌─────────────────────────────────┐
                        │      RESONANT IDE (Desktop)      │
                        │  VS Code Fork · 59 Local Tools   │
                        └───────────────┬─────────────────┘
                                        │
                        ┌───────────────▼─────────────────┐
                        │          API GATEWAY             │
                        │  JWT Auth · Rate Limits · 30+    │
                        │  Service Routes · Blue/Green     │
                        └───────────────┬─────────────────┘
           ┌────────────────┬───────────┴──────────┬────────────────┐
     ┌─────▼──────┐  ┌─────▼──────┐  ┌────────────▼──┐  ┌─────────▼───┐
     │    Auth    │  │    Chat    │  │  Agent Engine  │  │   Memory    │
     │ JWT/OAuth  │  │  Skills    │  │ Plan-Execute   │  │ Hash Sphere │
     │ BYOK Keys  │  │  137 Tools │  │ 130+ Tools     │  │  9 Layers   │
     └────────────┘  └────────────┘  │ Multi-Agent    │  │ Semantic 3D │
     ┌────────────┐  ┌────────────┐  │ Orchestrator   │  └─────────────┘
     │ Blockchain │  │  Billing   │  └────────────────┘  ┌─────────────┐
     │  DSID-P    │  │  Stripe    │  ┌────────────────┐  │    Code     │
     │ Ed25519    │  │  Credits   │  │   LLM Service  │  │ Visualizer  │
     │ Raft Chain │  │  Metering  │  │  11 Providers  │  │ AST+Govern  │
     └────────────┘  └────────────┘  │  BYOK+Ollama   │  │ Dep Graphs  │
                                     └────────────────┘  └─────────────┘
     ┌────────────┐  ┌────────────┐  ┌────────────────┐  ┌─────────────┐
     │  Rabbit    │  │ Marketplace│  │    Workflow     │  │  Cognitive  │
     │  5 Svcs    │  │  Templates │  │  Orchestration  │  │    NLP      │
     └────────────┘  └────────────┘  └────────────────┘  └─────────────┘
```

<br>

---

<br>

## &#x1F4CA; Key Numbers

<div align="center">

| | | | |
|:---:|:---:|:---:|:---:|
| **42** | **30+** | **130+** | **59** |
| Docker Services | Gateway Routes | Agent Tools | IDE Tools |
| **11** | **5** | **9** | **6** |
| LLM Providers | Trust Tiers | Memory Layers | Governance Layers |

</div>

<br>

---

<br>

## &#x1F9E0; How It Works

<details>
<summary><b>&#x1F510; Multi-Layer Governance (MAGM)</b> — 6-layer policy engine enforced before every action</summary>
<br>

The **Multi-Agent Governance Model** enforces policies **before** agent actions execute — not after.

| Layer | Name | What it does |
|:---:|---|---|
| **L0** | Policy Management | Universal, class-specific, and cluster-specific policy rules |
| **L1** | Ownership & Identity | Owner/manager bindings, delegation rules, permission scoping |
| **L2** | Contract Governance | Allowed/forbidden action lists, resource budgets, escalation rules |
| **L3** | Semantic Governance | Cluster-based rules, supervision requirements, self-modification control |
| **L4** | Behavioral Governance | Causality rules, interaction patterns, coordination constraints, quotas |
| **L5** | Registry Enforcement | Runtime enforcement across the tool and agent registries |

Plus **7 Ethical Pillars** (human oversight, transparency, privacy, fairness, safety, governance, sovereignty) enforced at the execution boundary with sandbox validation and execution gates.

</details>

<details>
<summary><b>&#x26D3; DSID-P Identity Protocol</b> — Ed25519-signed cryptographic identity for every agent and user</summary>
<br>

**Decentralized Secure Identity with Provenance (DSID-P):**

- **Format:** `dsid:v{version}:{entity_type}:{content_hash}:{random}`
- **Signatures:** Ed25519 (PyNaCl) — sign and verify identity objects cryptographically
- **Lineage:** Full parent/child hash node tree with depth tracking
- **Versioning:** Create → update (supersede) → revoke lifecycle
- **Blockchain anchoring:** Every DSID registration is recorded as a blockchain transaction
- **Hash Nodes:** Merkle-tree-based content verification with proof paths

On-chain contracts on Base Sepolia L2:
- **IdentityRegistry** — User identity with public key binding
- **AgentRegistry** — Agent manifests with status tracking
- **MemoryAnchors** — Content hash timestamps for verifiable provenance

</details>

<details>
<summary><b>&#x1F4C8; Trust Tiers (T1 → T5)</b> — 5-pillar reputation system, autonomy is earned</summary>
<br>

**Agent Trust Score (ATS)** is computed from 5 reputation pillars with configurable weight profiles:

| Pillar | What it measures |
|---|---|
| **Performance Reputation (PR)** | Task success rate, error frequency, output quality, latency consistency |
| **Behavioral Reputation (BR)** | Behavior consistency, deviation score, anomaly count, cooperation quality |
| **Semantic Reliability (SR)** | Drift velocity, cluster consistency, vector coherence, domain alignment |
| **Governance Compliance (GCS)** | Policy violations, permission breaches, unauthorized writes, audit pass rate |
| **Social Interaction (SIS)** | Peer evaluations, enterprise ratings, conflict resolution, refusal accuracy |

| Tier | Score | Level |
|:---:|:---:|---|
| **T5** | 90–100 | Platinum — Enterprise/Gov-grade reliability |
| **T4** | 75–89 | Gold — High-performing, trusted |
| **T3** | 60–74 | Silver — Stable, general-purpose |
| **T2** | 40–59 | Bronze — Limited trust, supervised |
| **T1** | 0–39 | Restricted — Heavily supervised or suspended |

Includes **trust decay** (inactivity, drift, outdated behavior graphs), **trust recovery** mechanisms, and weight profiles for low-risk, medium-risk, high-risk, and supervisor contexts.

</details>

<details>
<summary><b>&#x1F9E0; Hash Sphere Memory</b> — 9-layer deterministic semantic coordinate system</summary>
<br>

The Hash Sphere maps every piece of content to a point in 3D semantic space with full coordinate representations:

| Layer | Name | What it computes |
|:---:|---|---|
| **1** | Input Processing | Text normalization |
| **2** | Hash Generation | Meaning hash + energy hash + spin hash |
| **3** | Universe ID | SHA-256 content fingerprint |
| **4** | Anchor Energy | `E_j(s) = exp(-β·‖s - A_j‖²)` — attraction to nearest anchor |
| **5** | Coordinates | XYZ (semantic clusters) + Hyperspherical (r, φ, θ) |
| **6** | Resonance Scoring | `R(h) = sin(a·x) + cos(b·y) + tan(c·z)` where a=π/4, b=e/3, c=φ/2 |
| **7** | Evidence Aggregation | `E* = Σ wᵢ · sᵢ` — weighted sum of memory positions |
| **8** | Multi-LLM Routing | Provider selection based on context |
| **9** | Output Correction | λ-weighted blend of LLM output and evidence |

**5-method extraction** (in priority order):
1. Anchor-based lookup (fast keyword matching)
2. Proximity search (3D XYZ distance)
3. Resonance filtering (hash similarity)
4. Cluster retrieval (context-based)
5. RAG semantic search (pgvector embeddings)

**Hybrid Ranker weights:** RAG 0.30 · Resonance 0.25 · Resonance Function 0.15 · Anchor Energy 0.10 · Proximity 0.10 · Recency 0.05 · Anchor 0.05

Plus **Magnetic Pull System** for non-linear amplification of strong memories and **Neural Gravity Engine** for gravitational clustering.

</details>

<details>
<summary><b>&#x1F916; Multi-Agent Orchestration</b> — swarm intelligence with blockchain audit trail</summary>
<br>

The **Multi-Agent Orchestrator** manages autonomous agent swarms:

- **Agent Roles:** Executor, Planner, Reviewer, Supervisor, Specialist
- **Goal Decomposition:** LLM breaks high-level goals into 3–10 concrete sub-tasks
- **Dependency DAG:** Tasks track dependencies; blocked tasks unlock automatically when prerequisites complete
- **Agent Scoring:** Capability matching + performance-weighted selection
- **Failure Recovery:** Automatic re-assignment to different agents on failure
- **Blockchain Recording:** Every goal submission, task assignment, completion, and failure is recorded on-chain

Real-time inter-agent messaging via the parallel agent runtime.

</details>

<details>
<summary><b>&#x1F4BB; Resonant IDE</b> — AI-native VS Code fork with 59 built-in tools</summary>
<br>

**Resonant IDE** — Electron-based VS Code fork with a built-in agentic AI assistant:

- **59 local tools** — file I/O, git, web search, terminal, code analysis, deployment
- **Thin client architecture** — client handles UI + tool execution; server handles orchestration + system prompts
- **Multi-provider:** OpenAI, Anthropic, Groq, Google + local (Ollama, LM Studio)
- **BYOK:** Bring Your Own Key for any provider with automatic fallback chain
- **Code Visualizer integration** — AST scanning, dependency graphs, governance analysis from within the editor

</details>

<details>
<summary><b>&#x1F4AC; Resonant Chat</b> — web AI assistant with 137 tools and skill detection</summary>
<br>

- **137 tools** across search, memory, Hash Sphere, code analysis, agents, utilities, media, and integrations
- **LLM-based skill detection** — intent classification routes to specialized handlers
- **Integration skills:** Figma, Google Calendar, Google Drive, Sigma
- **Orchestrator mode** with interactive options and agent creation via natural language
- **Native tool calling** across OpenAI, Anthropic, and Groq — no prompt-based JSON parsing

</details>

<details>
<summary><b>&#x26D3; Distributed Blockchain</b> — custom chain with Raft consensus</summary>
<br>

- **Raft Consensus** for leader election and log replication across nodes
- **P2P Network** for node communication and block/transaction announcements
- **Fork handling** and chain reorganization
- **Transaction Graph** with BFS path finding between transactions
- **Merkle proofs** for content verification
- Records: DSID registrations, agent orchestration events, memory anchors, trust score changes

</details>

<br>

---

<br>

## &#x1F4E6; All Repositories

> **41 repos** — every service is its own repo, individually deployable.

<br>

<details open>
<summary><h3>&#x1F680; Full-Stack Deployment</h3></summary>

| | Repository | What it does |
|:---:|---|---|
| &#x1F4E6; | [**ORG_Core**](https://github.com/DevSwat-ResonantGenesis/ORG_Core) | Production monolith — docker-compose for 42 services, gateway config, shared libs |
| &#x1F310; | [**ORG_Frontend**](https://github.com/DevSwat-ResonantGenesis/ORG_Frontend) | React 18 + TypeScript + Vite — AI chat, agent dashboard, Hash Sphere visualization |

</details>

<details open>
<summary><h3>&#x2699; Core Services</h3></summary>

| | Repository | What it does |
|:---:|---|---|
| &#x1F6E1; | [**ORG_Gateway**](https://github.com/DevSwat-ResonantGenesis/ORG_Gateway) | API Gateway — 30+ service routes, JWT auth middleware, rate limiting, blue/green deploy |
| &#x1F511; | [**ORG_Auth**](https://github.com/DevSwat-ResonantGenesis/ORG_Auth) | JWT, OAuth (Google/GitHub/Discord), BYOK API key management, 2FA |
| &#x1F4AC; | [**ORG_Chat**](https://github.com/DevSwat-ResonantGenesis/ORG_Chat) | Resonant Chat — 137 tools, LLM skill detection, IDE completions proxy |
| &#x1F916; | [**ORG_Agent_Engine**](https://github.com/DevSwat-ResonantGenesis/ORG_Agent_Engine) | Plan-execute loop, 130+ tools, multi-agent orchestrator, DSID-P trust enforcement |
| &#x1F9E0; | [**ORG_Memory**](https://github.com/DevSwat-ResonantGenesis/ORG_Memory) | Hash Sphere — 9-layer extraction, 5-method retrieval, hybrid ranking, pgvector embeddings |
| &#x1F4B3; | [**ORG_Billing**](https://github.com/DevSwat-ResonantGenesis/ORG_Billing) | Credit system, Stripe integration, execution metering |
| &#x1F464; | [**ORG_User_Service**](https://github.com/DevSwat-ResonantGenesis/ORG_User_Service) | Profiles, preferences, settings |
| &#x1F514; | [**ORG_Notifications**](https://github.com/DevSwat-ResonantGenesis/ORG_Notifications) | Email, push notifications, event-driven alerts |
| &#x1F504; | [**ORG_Workflow**](https://github.com/DevSwat-ResonantGenesis/ORG_Workflow) | Multi-step orchestration — sequential, parallel, branching |
| &#x1F4BE; | [**ORG_Storage**](https://github.com/DevSwat-ResonantGenesis/ORG_Storage) | S3/DigitalOcean Spaces compatible file storage |

</details>

<details>
<summary><h3>&#x1F4A1; AI & LLM</h3></summary>

| | Repository | What it does |
|:---:|---|---|
| &#x26A1; | [**ORG_UnifiedLLMClient**](https://github.com/DevSwat-ResonantGenesis/ORG_UnifiedLLMClient) | One async Python client for 11 providers — streaming, native tool calling, BYOK, fallback chain |
| &#x1F310; | [**ORG_LLM_Service**](https://github.com/DevSwat-ResonantGenesis/ORG_LLM_Service) | Multi-provider proxy (OpenAI, Anthropic, Groq, Gemini, +7 more) |
| &#x1F9EC; | [**ORG_Cognitive**](https://github.com/DevSwat-ResonantGenesis/ORG_Cognitive) | NLP analysis, text processing, semantic understanding |
| &#x1F52C; | [**ORG_ML_Service**](https://github.com/DevSwat-ResonantGenesis/ORG_ML_Service) | Model registry, inference endpoints |
| &#x1F6E0; | [**ORG_Unified_Tool_Registry-Observability_Module**](https://github.com/DevSwat-ResonantGenesis/ORG_Unified_Tool_Registry-Observability_Module) | Canonical ToolDef format, per-tool observability, OpenAI/Anthropic format conversion |
| &#x1F4AC; | [**ORG_Registered_Users_Agentic_Chat**](https://github.com/DevSwat-ResonantGenesis/ORG_Registered_Users_Agentic_Chat) | Full agentic chat with native tool calling and provider routing |

</details>

<details>
<summary><h3>&#x1F4BB; IDE & Code Analysis</h3></summary>

| | Repository | What it does |
|:---:|---|---|
| &#x1F5A5; | [**ORG_IDE**](https://github.com/DevSwat-ResonantGenesis/ORG_IDE) | Resonant IDE — AI-native VS Code fork, 59 built-in tools, thin client |
| &#x1F9E9; | [**ORG_Axtention_IDE**](https://github.com/DevSwat-ResonantGenesis/ORG_Axtention_IDE) | IDE Server Extension — agentic loop, system prompts, tool orchestration |
| &#x1F4DF; | [**ORG_IDE_Platform**](https://github.com/DevSwat-ResonantGenesis/ORG_IDE_Platform) | Terminal sessions, PTY management |
| &#x1F333; | [**ORG_AST_analysis**](https://github.com/DevSwat-ResonantGenesis/ORG_AST_analysis) | Code Visualizer — AST scanning, dependency graphs, pipeline detection, governance |
| &#x25B6; | [**ORG_Code_Execution**](https://github.com/DevSwat-ResonantGenesis/ORG_Code_Execution) | Secure sandboxed code execution |
| &#x1F3D7; | [**ORG_Build_Service**](https://github.com/DevSwat-ResonantGenesis/ORG_Build_Service) | Project builder, CI/CD pipeline |
| &#x1F512; | [**ORG_Sandbox_Runner**](https://github.com/DevSwat-ResonantGenesis/ORG_Sandbox_Runner) | Isolated execution for untrusted code |

</details>

<details>
<summary><h3>&#x26D3; Blockchain & Identity</h3></summary>

| | Repository | What it does |
|:---:|---|---|
| &#x1F517; | [**ORG_Blockchain**](https://github.com/DevSwat-ResonantGenesis/ORG_Blockchain) | DSID-P protocol, 5-pillar trust system, 6-layer MAGM governance engine, Raft distributed chain |
| &#x26CF; | [**ORG_Blockchain_Node**](https://github.com/DevSwat-ResonantGenesis/ORG_Blockchain_Node) | Base Sepolia L2 — IdentityRegistry, AgentRegistry, MemoryAnchors contracts |
| &#x1F510; | [**ORG_Crypto**](https://github.com/DevSwat-ResonantGenesis/ORG_Crypto) | Ed25519 signatures, key management, cryptographic operations |

</details>

<details>
<summary><h3>&#x1F30D; Marketplace & Social</h3></summary>

| | Repository | What it does |
|:---:|---|---|
| &#x1F6CD; | [**ORG_Marketplace**](https://github.com/DevSwat-ResonantGenesis/ORG_Marketplace) | Agent templates, one-click deploy, community contributions |
| &#x1F430; | [**ORG_Rabbit**](https://github.com/DevSwat-ResonantGenesis/ORG_Rabbit) | Reddit-like community (5 microservices — API, content, community, votes, moderation) |
| &#x1F4E8; | [**ORG_Discord_Bridge**](https://github.com/DevSwat-ResonantGenesis/ORG_Discord_Bridge) | Discord bot integration for notifications and commands |
| &#x1F310; | [**ORG_Public**](https://github.com/DevSwat-ResonantGenesis/ORG_Public) | Public guest chat service |

</details>

<details>
<summary><h3>&#x1F6E0; Platform & DevOps</h3></summary>

| | Repository | What it does |
|:---:|---|---|
| &#x1F3AD; | [**ORG_Platform_Orchestration**](https://github.com/DevSwat-ResonantGenesis/ORG_Platform_Orchestration) | Deployment scripts, docker-compose, infrastructure |
| &#x1F527; | [**ORG_Platform_Tools**](https://github.com/DevSwat-ResonantGenesis/ORG_Platform_Tools) | Shared utilities, CLI tools |
| &#x1F4D6; | [**ORG_DevOps_Runbook**](https://github.com/DevSwat-ResonantGenesis/ORG_DevOps_Runbook) | Deployment guides, troubleshooting docs |
| &#x1F680; | [**ORG_V8_API**](https://github.com/DevSwat-ResonantGenesis/ORG_V8_API) | V8 API service |
| &#x1F4DC; | [**ORG_OpenClaw**](https://github.com/DevSwat-ResonantGenesis/ORG_OpenClaw) | Legal document processing integration |
| &#x1F393; | [**ORG_Ed_Service**](https://github.com/DevSwat-ResonantGenesis/ORG_Ed_Service) | Learning modules, tutorials |
| &#x1F9EA; | [**ORG_Internal_Invarients_SIM**](https://github.com/DevSwat-ResonantGenesis/ORG_Internal_Invarients_SIM) | Platform safety invariants |
| &#x1F9EA; | [**ORG_Users_Invarients_SIM**](https://github.com/DevSwat-ResonantGenesis/ORG_Users_Invarients_SIM) | User safety invariants |
| &#x1F4DD; | [**ORG_User_Memory**](https://github.com/DevSwat-ResonantGenesis/ORG_User_Memory) | Per-user memory storage |

</details>

<br>

---

<br>

## &#x1F680; Get Started

```bash
# 1. Clone
git clone https://github.com/DevSwat-ResonantGenesis/ORG_Core.git
cd ORG_Core

# 2. Configure
cp .env.production.template .env.production
# Edit with your database URLs, API keys, etc.

# 3. Launch all services
docker compose -f docker-compose.unified.yml up -d

# 4. Check status
docker compose -f docker-compose.unified.yml ps
```

**Want just one service?** Each `ORG_*` repo runs independently with its own Dockerfile.

<br>

---

<br>

## &#x1F464; The Creator

<div align="center">

**Louie Nemesh** — Founder & Architect

*Started November 11, 2025. One person. One vision.*

*40+ microservices, blockchain identity protocol, AI-native IDE, full React frontend, agent marketplace, distributed ledger — designed and built from scratch.*

</div>

<br>

---

<br>

## &#x1F4DC; License

MIT License — free to use, modify, distribute, and build upon.

[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e.svg?style=flat-square)](https://opensource.org/licenses/MIT)

<br>

---

<div align="center">

<br>

**Governed Execution &nbsp;·&nbsp; Cryptographic Identity &nbsp;·&nbsp; Earned Trust &nbsp;·&nbsp; Semantic Memory**

<br>

*41 open source repos &nbsp;·&nbsp; 42 Docker services &nbsp;·&nbsp; 9-layer Hash Sphere &nbsp;·&nbsp; 5-tier trust system*

<br>

</div>
