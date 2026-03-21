<div align="center">

# RESONANT GENESIS

### Enterprise-Grade Governed AI Agent Ecosystem

[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Services](https://img.shields.io/badge/Services-42-8B5CF6.svg?style=for-the-badge)](#platform-architecture)
[![Tools](https://img.shields.io/badge/Agent_Tools-130+-3B82F6.svg?style=for-the-badge)](#agent-engine)
[![Providers](https://img.shields.io/badge/LLM_Providers-11-F59E0B.svg?style=for-the-badge)](#ai--llm-infrastructure)
[![DSID-P](https://img.shields.io/badge/Identity-DSID--P-EF4444.svg?style=for-the-badge)](#blockchain--identity)
[![Open Source](https://img.shields.io/badge/Open_Source-100%25-10B981.svg?style=for-the-badge)](#get-started)

**Created by Louie Nemesh** · Started November 11, 2025

</div>

---

## What is Resonant Genesis?

A full-stack production platform for **governed autonomous AI agents** — 42 Docker services across 41 repositories.

Agents operate under **cryptographic identity** (DSID-P with Ed25519 signatures), **multi-layer governance** (6-layer MAGM policy engine evaluated before every action), **5-pillar trust scoring** (T1 Restricted → T5 Platinum), and **immutable blockchain audit trails** with Raft consensus.

Memory is stored in the **Hash Sphere** — a 9-layer coordinate system that maps content to 3D semantic space using resonance hashing, anchor energy fields, and hybrid multi-method extraction.

---

## Platform Architecture

```
                    ┌──────────────────────────────────┐
                    │      RESONANT IDE (Desktop)       │
                    │   VS Code Fork · 59 Local Tools   │
                    └───────────────┬──────────────────┘
                                    │
                    ┌───────────────▼──────────────────┐
                    │          API GATEWAY              │
                    │  JWT Auth · Rate Limits · 30+     │
                    │  Service Routes · Blue/Green      │
                    └───────────────┬──────────────────┘
          ┌──────────────┬──────────┴─────────┬──────────────┐
    ┌─────▼─────┐  ┌─────▼─────┐  ┌──────────▼──┐  ┌────────▼────┐
    │   Auth    │  │   Chat    │  │ Agent Engine │  │   Memory    │
    │ JWT/OAuth │  │ 137 Tools │  │ 130+ Tools   │  │ Hash Sphere │
    │ BYOK Keys │  │  Skills   │  │ Multi-Agent  │  │  9 Layers   │
    └───────────┘  └───────────┘  └─────────────┘  └─────────────┘
    ┌───────────┐  ┌───────────┐  ┌─────────────┐  ┌─────────────┐
    │Blockchain │  │  Billing  │  │ LLM Service │  │    Code     │
    │  DSID-P   │  │  Stripe   │  │ 11 Providers│  │ Visualizer  │
    │ Ed25519   │  │  Credits  │  │ BYOK+Ollama │  │ AST+Govern  │
    └───────────┘  └───────────┘  └─────────────┘  └─────────────┘
```

| | | | |
|:---:|:---:|:---:|:---:|
| **42** Docker Services | **130+** Agent Tools | **11** LLM Providers | **59** IDE Tools |
| **5** Trust Tiers | **9** Memory Layers | **6** Governance Layers | **7** Ethical Pillars |

---

## Governance (MAGM)

The **Multi-Agent Governance Model** enforces policies **before** agent actions execute — not after.

| Layer | Name | What it does |
|:---:|---|---|
| **L0** | Policy Management | Universal, class-specific, and cluster-specific policy rules |
| **L1** | Ownership & Identity | Owner/manager bindings, delegation rules, permission scoping |
| **L2** | Contract Governance | Allowed/forbidden action lists, resource budgets, escalation rules |
| **L3** | Semantic Governance | Cluster-based rules, supervision requirements, self-modification control |
| **L4** | Behavioral Governance | Causality rules, interaction patterns, coordination constraints, quotas |
| **L5** | Registry Enforcement | Runtime enforcement across the tool and agent registries |

**7 Ethical Pillars:** human oversight, transparency, privacy, fairness, safety, governance, sovereignty — enforced at the execution boundary with sandbox validation and execution gates.

---

## DSID-P Identity Protocol

**Decentralized Secure Identity with Provenance** — Ed25519-signed cryptographic identity for every agent and user.

- **Format:** `dsid:v{version}:{entity_type}:{content_hash}:{random}`
- **Signatures:** Ed25519 (PyNaCl) — sign and verify identity objects cryptographically
- **Lineage:** Full parent/child hash node tree with depth tracking
- **Versioning:** Create → update (supersede) → revoke lifecycle
- **Blockchain anchoring:** Every DSID registration recorded as a blockchain transaction
- **Hash Nodes:** Merkle-tree-based content verification with proof paths

**On-chain contracts (Base Sepolia L2):** IdentityRegistry · AgentRegistry · MemoryAnchors

---

## Trust Tiers (T1 → T5)

**Agent Trust Score (ATS)** computed from 5 reputation pillars:

| Pillar | What it measures |
|---|---|
| **Performance Reputation (PR)** | Task success rate, error frequency, output quality, latency consistency |
| **Behavioral Reputation (BR)** | Behavior consistency, deviation score, anomaly count, cooperation quality |
| **Semantic Reliability (SR)** | Drift velocity, cluster consistency, vector coherence, domain alignment |
| **Governance Compliance (GCS)** | Policy violations, permission breaches, unauthorized writes, audit pass rate |
| **Social Interaction (SIS)** | Peer evaluations, enterprise ratings, conflict resolution, refusal accuracy |

| Tier | Score | Level |
|:---:|:---:|---|
| **T5** | 90-100 | Platinum — Enterprise/Gov-grade reliability |
| **T4** | 75-89 | Gold — High-performing, trusted |
| **T3** | 60-74 | Silver — Stable, general-purpose |
| **T2** | 40-59 | Bronze — Limited trust, supervised |
| **T1** | 0-39 | Restricted — Heavily supervised or suspended |

Includes **trust decay** (inactivity, drift, outdated behavior graphs), **trust recovery** mechanisms, and configurable weight profiles (low-risk, medium-risk, high-risk, supervisor).

---

## Hash Sphere Memory

9-layer deterministic semantic coordinate system. Every piece of content is mapped to a point in 3D semantic space.

| Layer | Name | What it computes |
|:---:|---|---|
| **1** | Input Processing | Text normalization |
| **2** | Hash Generation | Meaning hash + energy hash + spin hash |
| **3** | Universe ID | SHA-256 content fingerprint |
| **4** | Anchor Energy | E_j(s) = exp(-beta \|\|s - A_j\|\|^2) — attraction to nearest anchor |
| **5** | Coordinates | XYZ (semantic clusters) + Hyperspherical (r, phi, theta) |
| **6** | Resonance Scoring | R(h) = sin(ax) + cos(by) + tan(cz) where a=pi/4, b=e/3, c=phi/2 |
| **7** | Evidence Aggregation | E* = sum(w_i * s_i) — weighted sum of memory positions |
| **8** | Multi-LLM Routing | Provider selection based on context |
| **9** | Output Correction | lambda-weighted blend of LLM output and evidence |

**5-method extraction:** Anchor lookup → Proximity search → Resonance filtering → Cluster retrieval → RAG semantic search (pgvector)

**Hybrid Ranker weights:** RAG 0.30 · Resonance 0.25 · Resonance Function 0.15 · Anchor Energy 0.10 · Proximity 0.10 · Recency 0.05 · Anchor 0.05

---

## Agent Engine

- **Autonomous plan-execute loop** with iterative reasoning and tool execution
- **130+ tools** across search, memory, Hash Sphere, code analysis, agents, utilities
- **Multi-agent swarm orchestrator** — Agent roles: Executor, Planner, Reviewer, Supervisor, Specialist
- **Goal decomposition** via LLM into 3-10 concrete sub-tasks with dependency DAG
- **Agent scoring** — capability matching + performance-weighted selection
- **Failure recovery** — automatic re-assignment on failure
- **Blockchain recording** — every goal, task, completion, and failure recorded on-chain

---

## Resonant IDE

Electron-based **VS Code fork** with a built-in agentic AI assistant:

- **59 local tools** — file I/O, git, web search, terminal, code analysis, deployment
- **Thin client architecture** — client handles UI + tool execution; server handles orchestration
- **Multi-provider:** OpenAI, Anthropic, Groq, Google + local (Ollama, LM Studio)
- **BYOK:** Bring Your Own Key for any provider with automatic fallback chain
- **Code Visualizer** — AST scanning, dependency graphs, governance analysis

---

## Resonant Chat

Web AI assistant with **137 tools** and LLM-based skill detection:

- **Native tool calling** across OpenAI, Anthropic, and Groq
- **Integration skills:** Figma, Google Calendar, Google Drive, Sigma
- **Orchestrator mode** with interactive options and agent creation via natural language

---

## Distributed Blockchain

Custom chain with **Raft consensus:**

- **Leader election** and log replication across nodes
- **P2P network** for block/transaction announcements
- **Fork handling** and chain reorganization
- **Transaction graph** with BFS path finding
- **Merkle proofs** for content verification
- Records: DSID registrations, orchestration events, memory anchors, trust changes

---

## AI & LLM Infrastructure

- **Unified LLM Client** — single async Python client for 11 providers (OpenAI, Anthropic, Groq, Gemini, +7 more)
- **Native tool calling** with automatic format conversion (OpenAI/Anthropic)
- **BYOK** with dual-key resolution and automatic fallback chains
- **Streaming** SSE support across all providers

---

## All Repositories

41 repos — every service is its own repo, individually deployable.

### Core Services

| Repository | What it does |
|---|---|
| [**ORG_Core**](https://github.com/DevSwat-ResonantGenesis/ORG_Core) | Production monolith — docker-compose for 42 services, gateway config, shared libs |
| [**ORG_Frontend**](https://github.com/DevSwat-ResonantGenesis/ORG_Frontend) | React 18 + TypeScript + Vite — AI chat, agent dashboard, Hash Sphere visualization |
| [**ORG_Gateway**](https://github.com/DevSwat-ResonantGenesis/ORG_Gateway) | API Gateway — 30+ service routes, JWT auth middleware, rate limiting, blue/green deploy |
| [**ORG_Auth**](https://github.com/DevSwat-ResonantGenesis/ORG_Auth) | JWT, OAuth (Google/GitHub/Discord), BYOK API key management, 2FA |
| [**ORG_Chat**](https://github.com/DevSwat-ResonantGenesis/ORG_Chat) | Resonant Chat — 137 tools, LLM skill detection, IDE completions proxy |
| [**ORG_Agent_Engine**](https://github.com/DevSwat-ResonantGenesis/ORG_Agent_Engine) | Plan-execute loop, 130+ tools, multi-agent orchestrator, DSID-P trust enforcement |
| [**ORG_Memory**](https://github.com/DevSwat-ResonantGenesis/ORG_Memory) | Hash Sphere — 9-layer extraction, 5-method retrieval, hybrid ranking, pgvector embeddings |
| [**ORG_Billing**](https://github.com/DevSwat-ResonantGenesis/ORG_Billing) | Credit system, Stripe integration, execution metering |
| [**ORG_User_Service**](https://github.com/DevSwat-ResonantGenesis/ORG_User_Service) | Profiles, preferences, settings |
| [**ORG_Notifications**](https://github.com/DevSwat-ResonantGenesis/ORG_Notifications) | Email, push notifications, event-driven alerts |
| [**ORG_Workflow**](https://github.com/DevSwat-ResonantGenesis/ORG_Workflow) | Multi-step orchestration — sequential, parallel, branching |
| [**ORG_Storage**](https://github.com/DevSwat-ResonantGenesis/ORG_Storage) | S3/DigitalOcean Spaces compatible file storage |

### AI & LLM

| Repository | What it does |
|---|---|
| [**ORG_UnifiedLLMClient**](https://github.com/DevSwat-ResonantGenesis/ORG_UnifiedLLMClient) | Async Python client for 11 providers — streaming, native tool calling, BYOK, fallback chain |
| [**ORG_LLM_Service**](https://github.com/DevSwat-ResonantGenesis/ORG_LLM_Service) | Multi-provider proxy (OpenAI, Anthropic, Groq, Gemini, +7 more) |
| [**ORG_Cognitive**](https://github.com/DevSwat-ResonantGenesis/ORG_Cognitive) | NLP analysis, text processing, semantic understanding |
| [**ORG_ML_Service**](https://github.com/DevSwat-ResonantGenesis/ORG_ML_Service) | Model registry, inference endpoints |
| [**ORG_Unified_Tool_Registry-Observability_Module**](https://github.com/DevSwat-ResonantGenesis/ORG_Unified_Tool_Registry-Observability_Module) | Canonical ToolDef format, per-tool observability, OpenAI/Anthropic format conversion |
| [**ORG_Registered_Users_Agentic_Chat**](https://github.com/DevSwat-ResonantGenesis/ORG_Registered_Users_Agentic_Chat) | Full agentic chat with native tool calling and provider routing |

### IDE & Code Analysis

| Repository | What it does |
|---|---|
| [**ORG_IDE**](https://github.com/DevSwat-ResonantGenesis/ORG_IDE) | Resonant IDE — AI-native VS Code fork, 59 built-in tools, thin client |
| [**ORG_Axtention_IDE**](https://github.com/DevSwat-ResonantGenesis/ORG_Axtention_IDE) | IDE Server Extension — agentic loop, system prompts, tool orchestration |
| [**ORG_IDE_Platform**](https://github.com/DevSwat-ResonantGenesis/ORG_IDE_Platform) | Terminal sessions, PTY management |
| [**ORG_AST_analysis**](https://github.com/DevSwat-ResonantGenesis/ORG_AST_analysis) | Code Visualizer — AST scanning, dependency graphs, pipeline detection, governance |
| [**ORG_Code_Execution**](https://github.com/DevSwat-ResonantGenesis/ORG_Code_Execution) | Secure sandboxed code execution |
| [**ORG_Build_Service**](https://github.com/DevSwat-ResonantGenesis/ORG_Build_Service) | Project builder, CI/CD pipeline |
| [**ORG_Sandbox_Runner**](https://github.com/DevSwat-ResonantGenesis/ORG_Sandbox_Runner) | Isolated execution for untrusted code |

### Blockchain & Identity

| Repository | What it does |
|---|---|
| [**ORG_Blockchain**](https://github.com/DevSwat-ResonantGenesis/ORG_Blockchain) | DSID-P protocol, 5-pillar trust system, 6-layer MAGM governance, Raft distributed chain |
| [**ORG_Blockchain_Node**](https://github.com/DevSwat-ResonantGenesis/ORG_Blockchain_Node) | Base Sepolia L2 — IdentityRegistry, AgentRegistry, MemoryAnchors contracts |
| [**ORG_Crypto**](https://github.com/DevSwat-ResonantGenesis/ORG_Crypto) | Ed25519 signatures, key management, cryptographic operations |

### Marketplace & Social

| Repository | What it does |
|---|---|
| [**ORG_Marketplace**](https://github.com/DevSwat-ResonantGenesis/ORG_Marketplace) | Agent templates, one-click deploy, community contributions |
| [**ORG_Rabbit**](https://github.com/DevSwat-ResonantGenesis/ORG_Rabbit) | Reddit-like community (5 microservices — API, content, community, votes, moderation) |
| [**ORG_Discord_Bridge**](https://github.com/DevSwat-ResonantGenesis/ORG_Discord_Bridge) | Discord bot integration for notifications and commands |
| [**ORG_Public**](https://github.com/DevSwat-ResonantGenesis/ORG_Public) | Public guest chat service |

### Platform & DevOps

| Repository | What it does |
|---|---|
| [**ORG_Platform_Orchestration**](https://github.com/DevSwat-ResonantGenesis/ORG_Platform_Orchestration) | Deployment scripts, docker-compose, infrastructure |
| [**ORG_Platform_Tools**](https://github.com/DevSwat-ResonantGenesis/ORG_Platform_Tools) | Shared utilities, CLI tools |
| [**ORG_DevOps_Runbook**](https://github.com/DevSwat-ResonantGenesis/ORG_DevOps_Runbook) | Deployment guides, troubleshooting docs |
| [**ORG_V8_API**](https://github.com/DevSwat-ResonantGenesis/ORG_V8_API) | V8 API service |
| [**ORG_OpenClaw**](https://github.com/DevSwat-ResonantGenesis/ORG_OpenClaw) | Legal document processing integration |
| [**ORG_Ed_Service**](https://github.com/DevSwat-ResonantGenesis/ORG_Ed_Service) | Learning modules, tutorials |
| [**ORG_Internal_Invarients_SIM**](https://github.com/DevSwat-ResonantGenesis/ORG_Internal_Invarients_SIM) | Platform safety invariants |
| [**ORG_Users_Invarients_SIM**](https://github.com/DevSwat-ResonantGenesis/ORG_Users_Invarients_SIM) | User safety invariants |
| [**ORG_User_Memory**](https://github.com/DevSwat-ResonantGenesis/ORG_User_Memory) | Per-user memory storage |

---

## Get Started

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

Each `ORG_*` repo also runs independently with its own Dockerfile.

---

<div align="center">

**Louie Nemesh** — Founder & Architect

40+ microservices, blockchain identity protocol, AI-native IDE, full React frontend, agent marketplace, distributed ledger — designed and built from scratch.

MIT License

**Governed Execution · Cryptographic Identity · Earned Trust · Semantic Memory**

</div>
