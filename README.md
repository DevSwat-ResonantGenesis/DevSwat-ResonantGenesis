<div align="center">

# RESONANT GENESIS

### Enterprise-Grade Governed AI Agent Ecosystem

🚨 URGENT NOTICE: SERVER SHUTDOWN DUE TO FUNDING SHORTAGE

⚠️ CURRENT STATUS: PRODUCTION SERVER REMOVED FROM DIGITALOCEAN

The ResonantGenesis production server hosting 182 active users has been shut down due to lack of funding. This was a desperate decision to make the project fully open source and seek financial support to continue development and maintenance.

Your support can bring ResonantGenesis back online and help continue this ambitious project.

🏗️ Louie Nemesh

AI System Architect & Full-Stack Developer | Solo Founder @ ResonantGenesis

Profile Views Projects Experience Status

👤 About Me

I am Louie Nemesh, an AI System Architect and Full-Stack Developer with over 6 years of experience in the IT industry since 2018. I specialize in building sophisticated AI-powered platforms and managing international development teams.

🎯 Professional Journey

2018 - 2024: Founder & CEO of Web Development Agency (Qatar)

Managed hundreds of diverse projects for clients worldwide
Led full-stack international development teams
Delivered end-to-end solutions from concept to deployment
Specialized in scalable web applications and enterprise systems
2025 - Present: Solo Founder @ ResonantGenesis

Built a complete self-hosted AI agent and developer tools platform
Designed and implemented sophisticated multi-service architecture
Developed advanced AI orchestration and execution systems
Currently seeking investment and B2B partnerships


[![License: MIT](https://img.shields.io/badge/License-MIT-22c55e.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Services](https://img.shields.io/badge/Docker_Services-35-8B5CF6.svg?style=for-the-badge)](#platform-architecture)
[![Repos](https://img.shields.io/badge/Repositories-40-6366F1.svg?style=for-the-badge)](#repository-map)
[![Tools](https://img.shields.io/badge/Agent_Tools-136-3B82F6.svg?style=for-the-badge)](#unified-tool-registry-136-tools)
[![Providers](https://img.shields.io/badge/LLM_Providers-11+BYOK-F59E0B.svg?style=for-the-badge)](#ai--llm-infrastructure)
[![DSID-P](https://img.shields.io/badge/Identity-DSID--P-EF4444.svg?style=for-the-badge)](#blockchain--identity-dsid-p)
[![Open Source](https://img.shields.io/badge/Open_Source-100%25-10B981.svg?style=for-the-badge)](#repository-map)

**Created by Louie Nemesh** · Started November 2025 becose some day Im gone but I want my work to be apreciate and my relatev get benefits of resonantgenesis.eth so let this stay here 

</div>

---

## What is Resonant Genesis?

A full-stack production platform for **governed autonomous AI agents** — **35 Docker services** across **40 repositories**.

Agents operate under **cryptographic identity** (DSID-P with Ed25519 signatures), **multi-layer governance** (RARA invariant engine with 3 invariant classes evaluated before every mutation), **5-pillar trust scoring** (T1 Restricted → T5 Platinum), and **immutable blockchain audit trails** with Raft consensus.

Memory lives in the **Hash Sphere** — a 9-layer coordinate system that maps content to 3D semantic space using resonance hashing, anchor energy fields, and a 7-weight hybrid ranker combining RAG + resonance + proximity + anchor energy.

The **API Gateway** enforces a 5-layer middleware stack: **Auth → Multi-Tenant Isolation → Rate Limiting → Economic Enforcement → Feature Gating** — every request is authenticated, tenant-scoped, credit-checked, and feature-gated before reaching any service.

---

## Platform Architecture

```
                    ┌──────────────────────────────────────┐
                    │         RESONANT IDE (Desktop)         │
                    │   VS Code Fork · 59 Local Tools        │
                    │   Multi-Provider LLM · Ollama · BYOK   │
                    └─────────────────┬────────────────────┘
                                      │
     ┌────────────────────────────────▼──────────────────────────────────┐
     │                        API GATEWAY                                │
     │  AuthMiddleware → TenantIsolation → RateLimiter → EconomicEnf    │
     │  → CreditDeduction → FeatureGate → 23 Route Modules → Proxy     │
     └──────┬──────────┬──────────┬──────────┬──────────┬──────────┬───┘
     ┌──────▼───┐ ┌────▼────┐ ┌──▼───────┐ ┌▼────────┐ ┌▼───────┐ ┌▼─────────┐
     │  Auth    │ │  Chat   │ │  Agent   │ │ Memory  │ │Billing │ │Blockchain│
     │JWT/OAuth │ │60+ svc  │ │ Engine   │ │  Hash   │ │Credits │ │ DSID-P   │
     │MFA/SAML │ │ Skills  │ │136 Tools │ │ Sphere  │ │Stripe  │ │Raft+P2P │
     │Sessions │ │ RAG     │ │ Swarm    │ │ Dual    │ │Invoices│ │ZK Proofs │
     └─────────┘ └─────────┘ └──────────┘ └─────────┘ └────────┘ └──────────┘
     ┌──────────┐ ┌─────────┐ ┌──────────┐ ┌─────────┐ ┌────────┐ ┌──────────┐
     │LLM Svc  │ │Code Viz │ │  RARA    │ │ State   │ │Rabbit  │ │Marketplace│
     │11 provs │ │AST+GPC  │ │Invariant │ │Physics  │ │5 micro │ │Templates │
     │MultiRtr │ │Compiler │ │KillSwitch│ │N-body   │ │services│ │Payments  │
     └─────────┘ └─────────┘ └──────────┘ └─────────┘ └────────┘ └──────────┘
```

| | | | |
|:---:|:---:|:---:|:---:|
| **35** Docker Services | **136** Agent Tools | **11** LLM Providers + BYOK | **60+** Chat Pipeline Services |
| **40** Repositories | **9** Memory Layers | **3** Invariant Classes | **23** Gateway Route Modules |

---

## Gateway Middleware Stack

Every request passes through **6 middleware layers** before reaching any service:

| Layer | Middleware | What it enforces |
|:---:|---|---|
| **1** | `AuthMiddleware` | JWT validation, cookie sessions, user context injection (user_id, org_id, role, plan) |
| **2** | `TenantIsolationMiddleware` | Org-level data isolation, anti-spoofing (strips client x-tenant-id), per-tenant rate limiting (600 RPM/org), x-tenant-id injection |
| **3** | `RateLimitMiddleware` | Global rate limiting, DoS protection |
| **4** | `EconomicEnforcementMiddleware` | Reads UserEconomicState from billing, injects X-Subscription-Tier + X-Credit-Balance headers, rejects suspended users |
| **5** | `CreditDeductionMiddleware` | Pre-check credits BEFORE execution (402 if insufficient), post-deduct AFTER success (path-based cost: chat 500, agents 2600, workflows 4000) |
| **6** | `FeatureGateMiddleware` | Tier-based feature access (IDE, code execution, blockchain, Hash Sphere) |

**23 route modules:** admin, agent_engine, anchors, code, code_visualizer, compliance, daemon, finance, git, ml, node, orgs, policies, predictions, rara, settings, state_physics, system, terminal, usage, user_memory, user, voice_ws

---

## RARA — Resident Autonomous Runtime Agent

Internal platform governance service (`RG_Internal_Invarients_SIM`) — the safety brain of the platform.

### 3 Invariant Classes

| Class | What it checks | Severity |
|---|---|---|
| **Structural** | Filesystem integrity, graph reachability, dependency chains | Critical/High |
| **Semantic** | Intent coherence, confidence thresholds, rationale quality | High/Medium |
| **Temporal** | Rate limits, blast radius, cadence constraints, timing | Medium/Low |

### Governance Rules
- **Confidence < 0.6** → Reject mutation
- **Blast radius > 2 services** → Require human approval
- **Core state touched** → Forbidden
- **Repeated failure** → Capability throttled

### Components
- **GovernanceEngine** — Hash Sphere-based mutation governance with explainability artifacts
- **KillSwitch** — Emergency freeze / stop / reset with confirmation tokens
- **SnapshotEngine** — State snapshots with point-in-time restore
- **CapabilityEngine** — Per-agent capability registration, toggling, rate limits
- **MutationExecutor** — Pre/post-condition validation, atomic execution
- **InvariantEngine** — 3-class invariant checker (structural, semantic, temporal)
- **DISD Protocol** — Decentralized Inter-Service Discovery with message routing, transport layer, and enhanced protocol
- **CryptographicReceipts** — Ed25519-signed execution receipts with failure detection
- **EpochAuthority** — Temporal coordination across distributed components
- **QuorumAuthority** — Multi-agent consensus for high-risk mutations
- **PreAuthGate** — Pre-authorization checks before mutation proposal
- **Compliance** — EU AI Act requirements, SOC2 controls, audit trails

---

## Hash Sphere Memory System

### 9-Layer Coordinate System

Every piece of content is mapped to a point in 3D semantic space with full coordinate representation:

| Layer | Name | Formula / What it computes |
|:---:|---|---|
| **1** | Input Processing | Text normalization, tokenization |
| **2** | Hash Generation | Meaning hash + energy hash + spin hash (SHA-256 based) |
| **3** | Universe ID | Content fingerprint for deduplication |
| **4** | Anchor Energy | `E_j(s) = exp(-beta * \|\|s - A_j\|\|^2)` — Gaussian attraction to semantic anchors |
| **5** | Coordinates | XYZ (Cartesian semantic space) + Hyperspherical (r, phi, theta) via PCA |
| **6** | Resonance Function | `R(h) = sin(a*x) + cos(b*y) + tan(c*z)` — interference pattern scoring |
| **7** | Evidence Aggregation | `E* = sum(w_i * s_i)` — weighted sum of memory positions |
| **8** | Multi-LLM Routing | Provider selection based on semantic context |
| **9** | Output Correction | Lambda-weighted blend of LLM output and evidence |

### HashSphereCoordinates (actual dataclass)

```
Cartesian:      x, y, z (3D semantic space)
Hyperspherical: r (radius), phi (latitude), theta (longitude)
Resonance:      resonance_score, normalized_resonance
Energy:         energy, spin_magnitude
Spin Vector:    spin_x, spin_y, spin_z
Hashes:         universe_id, hash, meaning_hash, energy_hash, spin_hash
Semantic:       meaning_score, intensity_score, sentiment_score
```

### Dual-Layer Long-Term Memory (DLLM)

| Layer | Type | Behavior |
|---|---|---|
| **Episodic** | Short-term with decay | Chat history, timestamps, exponential decay (30-day half-life, minimum 0.1 weight) |
| **Semantic** | Long-term crystallized | Stable facts, personality knowledge, patterns — never decays, reinforcement-updated |

Mirrors **hippocampus + neocortex** architecture.

### Hybrid Memory Ranker (7-weight scoring)

| Weight | Signal | Value |
|:---:|---|:---:|
| **0.30** | RAG semantic score (pgvector cosine similarity) | Highest |
| **0.25** | Hash Sphere resonance score | High |
| **0.15** | Resonance Function `R(h) = sin(ax) + cos(by) + tan(cz)` | Medium |
| **0.10** | Anchor Energy `E_j(s) = exp(-beta*\|\|s-A_j\|\|^2)` | Medium |
| **0.10** | XYZ proximity score | Medium |
| **0.05** | Recency (timestamp-based) | Low |
| **0.05** | Anchor importance score | Low |

### Memory Services

`dual_memory_engine` · `hash_sphere` · `resonance_hashing` · `hybrid_memory_ranker` · `pgvector_search` · `semantic_cache` · `embedding_cache` · `temporal_memory` · `short_term_memory` · `memory_extraction` · `memory_encryption` · `memory_deduplication` · `memory_summarization` · `document_loaders` · `performance_logger` · `vector_store` · `semantic_encoder`

---

## Cryptography & Encryption

Every layer of the platform uses purpose-built cryptographic primitives:

### Memory Encryption (At Rest)

| Algorithm | Where | What it protects |
|---|---|---|
| **AES-256-GCM** (AEAD) | `memory_encryption.py` | Memory content, anchor text, optionally embeddings. 96-bit random nonce per operation, 128-bit authentication tag, PBKDF2-SHA256 key derivation (100,000 iterations, OWASP minimum). Format: `ENC2:{base64(nonce + ciphertext + tag)}` |
| **AES-256-CBC** | `encrypted_payload.py` (Blockchain) | Node payloads — user data (Layer 2) and agent state (Layer 3). Key derivation from wallet keys, IV-based initialization |

### Hashing (Content Integrity)

| Algorithm | Where | Purpose |
|---|---|---|
| **SHA-256** | `resonance_hashing.py` | Universe ID generation (256-bit content fingerprint), meaning hash, energy hash, spin hash — the entire Hash Sphere coordinate system derives from SHA-256 |
| **SHA-256** | `memory_deduplication.py` | Exact duplicate detection via normalized content hash comparison |
| **SHA-256** | `semantic_cache.py` + `embedding_cache.py` | Cache key generation from query text (truncated to 16/32 chars) |
| **SHA-256** | `domain_hasher.py` (Blockchain) | Domain-specific hashing for blockchain operations |

### Identity & Signing

| Algorithm | Where | Purpose |
|---|---|---|
| **Ed25519** (PyNaCl) | `dsid.py` (Blockchain) | DSID-P identity signing and verification — every agent, user, and service gets a cryptographic keypair. 32-byte private key, 64-byte signatures |
| **Ed25519** | `RG_Internal_Invarients_SIM` | Cryptographic execution receipts with failure detection — RARA signs every governance decision |
| **Fernet** (AES-128-CBC + HMAC-SHA256) | `RG_Auth/crypto.py` | BYOK API key encryption at rest. Key rotation support. Derived from `BYOK_ENCRYPTION_KEY` or `JWT_SECRET_KEY` via SHA-256 |

### Zero-Knowledge Proofs

| Primitive | Where | Purpose |
|---|---|---|
| **Pedersen Commitments** | `zero_knowledge.py` | `C = g^v * h^r` — commit to values without revealing them. Used for private transactions |
| **ZK-SNARK Proofs** | `zero_knowledge.py` | Knowledge proofs, range proofs, membership proofs, equality proofs, balance proofs — prove facts about data without exposing the underlying data |
| **Nullifiers** | `zero_knowledge.py` | Double-spend prevention for private transactions |

### Key Management

- **90-day key rotation** for memory encryption keys
- **PBKDF2-SHA256** (100k iterations) for deriving AES keys from passphrases
- **Dual-key resolution** for BYOK: user key → platform key fallback
- **Redis-backed OAuth state** with 10-minute expiry (CSRF protection)
- **Ephemeral key generation** with `secrets.token_bytes(32)` for dev environments

---

## Unified Tool Registry (136 Tools)

All tools defined in canonical `ToolDef` format with per-tool observability, access control, and automatic OpenAI/Anthropic format conversion.

| Category | Count | Tools |
|---|:---:|---|
| **Search & Web** | 11 | web_search, fetch_url, read_webpage, read_many_pages, reddit_search, image_search, news_search, places_search, youtube_search, deep_research (Perplexity), wikipedia |
| **Memory** | 4 | memory_read, memory_write, memory_search, memory_stats |
| **Hash Sphere** | 5 | hash_sphere_search, hash_sphere_anchor, hash_sphere_list_anchors, hash_sphere_hash, hash_sphere_resonance |
| **Code Visualizer** | 8 | cv_scan, cv_functions, cv_trace, cv_governance, cv_graph, cv_pipeline, cv_filter, cv_by_type |
| **Agent OS** | 27 | agents_list/create/start/stop/status/delete/update, sessions, traces, metrics, templates, versioning, scheduling, workspace_snapshot, run_agent, present_options |
| **State Physics** | 19 | sp_state, sp_nodes, sp_metrics, sp_identity, sp_simulate, sp_galaxy, sp_demo, sp_asymmetry, sp_physics_config, sp_entropy_*, sp_agent_spawn/step/kill, sp_experiment |
| **Community (Rabbit)** | 12 | create/list/search/get/delete posts, communities, comments, votes |
| **Media** | 3 | generate_image (DALL-E), generate_audio (TTS), generate_music (Suno) |
| **Integrations** | 8 | gmail_send/read, slack_send/read, google_calendar, google_drive, figma, sigma |
| **GitHub** | 8 | repos, files, upload, pull_requests, issues, commits, comments |
| **Git** | 5 | clone, branch, merge, push, pull |
| **Developer** | 4 | execute_code (Docker sandbox), http_request, external_http_request, dev_tool |
| **Platform API** | 2 | platform_api_search (~383 endpoints), platform_api_call |
| **IDE Filesystem** | 10 | file_read/write/edit/list/delete, multi_edit, grep_search, find_by_name, run_command, command_status |
| **Utilities** | 5 | weather, stock_crypto, generate_chart, visualize (SVG), get_current_time |
| **Tool Management** | 4 | create_tool, list_tools, delete_tool, update_tool (custom HTTP tools stored in DB) |
| **Email** | 1 | send_email (SendGrid) |

Access levels: `GUEST` (14 tools) · `REGISTERED` (full) · `AGENT` (autonomous) · `IDE` (local execution)

---

## AI & LLM Infrastructure

### Unified LLM Client (11 Providers)

Single async Python client (`rg_llm`) — all surfaces import from one source of truth.

| Tier | Provider | Default Model | Capabilities |
|---|---|---|---|
| **1** | OpenAI | gpt-4o | Vision, Tools, JSON mode |
| **1** | Anthropic | claude-sonnet-4 | Vision, Tools |
| **1** | Groq | llama-3.3-70b-versatile | Tools, JSON mode |
| **1** | Google Gemini | gemini-2.0-flash | Vision, Tools, JSON mode |
| **2** | DeepSeek | deepseek-chat | Tools, JSON mode |
| **2** | Mistral | mistral-large-latest | Tools, JSON mode |
| **2** | Together AI | Llama-3-70b-chat | JSON mode |
| **2** | Perplexity | sonar-large-128k-online | Online search |
| **2** | Fireworks | llama-v3p1-70b | Tools, JSON mode |
| **2** | OpenRouter | gpt-4o (proxy) | Vision, Tools, JSON mode |
| **2** | Cohere | command-r-plus | Tools, JSON mode |

**Fallback chain:** OpenAI → Anthropic → Groq → Google → DeepSeek → Mistral

**BYOK:** Users bring their own API keys for any provider. Dual-key resolution: user key takes priority over platform key. Keys managed via `RG_Auth` with encrypted storage.

### Multi-AI Router (LLM Service)

- Routes queries to optimal provider with automatic fallback
- Multi-key rotation (multiple Groq/Gemini keys for rate limit distribution)
- Context adaptation per provider
- Intelligent routing based on query characteristics

---

## Resonant Chat Pipeline (60+ Services)

The chat service runs a **deep processing pipeline** for every message:

**Core Pipeline:** Authentication → Resonance Hashing → Memory Extraction (RAG + Hash Sphere) → Context Building → LLM Provider Routing → Response Storage → Background Tasks → Response Enhancement

**Service Modules:**

| Category | Services |
|---|---|
| **Memory & RAG** | rag_engine, memory_merge, hybrid_memory_ranker, dual_memory_engine, resonance_hashing, semantic_cache |
| **Intelligence** | intent_engine, latent_intent_predictor, personality_dna, emotional_normalizer, sentiment_detection, causal_reasoning |
| **Knowledge** | knowledge_graph, evidence_graph, thought_branching, narrative_continuity_engine, temporal_thread_engine, insight_seed_engine |
| **Agent Orchestration** | agent_router, agent_engine, agent_chaining, agent_specialization, agent_voting, agent_confidence, agent_metrics, adaptive_agent_allocator, dynamic_team_composer, team_engine |
| **Autonomy** | autonomous_planner, autonomous_error_correction, self_improving_agent, autonomous_agent_executor |
| **Quality** | hallucination_detector, output_correction, cross_validation, source_citations, reasoning_engine |
| **Optimization** | token_optimizer, response_cache, multi_provider_chunking, token_tracker, plan_limits, credit_deduction |
| **Identity** | dsid_integration (DSID-P message signing), user_api_keys (BYOK management) |
| **Physics** | neural_gravity_engine, magnetic_pull, deterministic_universe, multi_timeline_engine |
| **Skills** | Figma, Google Calendar, Google Drive, Sigma (skill_executor + skills_registry) |
| **Media** | image_generation, web_search |

---

## Distributed Blockchain

Custom blockchain implementation with full distributed consensus:

| Component | What it does |
|---|---|
| **DistributedBlockchain** | Full distributed ledger with fork handling and deterministic replay |
| **RaftConsensus** | Leader election, log replication, term management across nodes |
| **P2PNetwork** | Node discovery, block/transaction broadcast, peer management |
| **Chain** | Block storage, Merkle root computation, transaction graph with BFS path finding |
| **DSID** | Decentralized Secure Identity — Ed25519 keypair generation, signing, verification |
| **SmartContracts** | On-chain logic execution (IdentityRegistry, AgentRegistry, MemoryAnchors) |
| **ZeroKnowledge** | ZK proof generation and verification |
| **Sharding** | Data partitioning across chain segments |
| **CrossChain** | Bridge protocol for inter-chain communication |
| **DualClassBlocks** | Differentiated block types for governance vs data transactions |
| **EncryptedPayload** | End-to-end encrypted transaction payloads |
| **ReputationTrust** | On-chain trust score computation and 5-pillar ATS |
| **GovernanceDSL** | Domain-specific language for governance rule definition |
| **EthicalGovernance** | 7 ethical pillars enforced at the chain level |
| **gRPC** | High-performance inter-node RPC |

**On-chain contracts (Base Sepolia L2):** IdentityRegistry · AgentRegistry · MemoryAnchors

---

## DSID-P Identity Protocol

**Decentralized Secure Identity with Provenance** — Ed25519-signed cryptographic identity for every agent, user, and service.

- **Format:** `dsid:v{version}:{entity_type}:{content_hash}:{random}`
- **Signatures:** Ed25519 (PyNaCl) — sign and verify identity objects
- **Lineage:** Full parent/child hash node tree with depth tracking
- **Versioning:** Create → update (supersede) → revoke lifecycle
- **Blockchain anchoring:** Every DSID registration recorded as a blockchain transaction
- **DISD Protocol:** Inter-service discovery with message types, routing, and transport layer
- **Enhanced DISD:** Production-grade protocol with cryptographic receipts and failure detection

---

## Trust Tiers (T1 → T5)

**Agent Trust Score (ATS)** computed from 5 reputation pillars:

| Pillar | What it measures |
|---|---|
| **Performance (PR)** | Task success rate, error frequency, output quality, latency |
| **Behavioral (BR)** | Consistency, deviation score, anomaly count, cooperation |
| **Semantic (SR)** | Drift velocity, cluster consistency, vector coherence |
| **Governance (GCS)** | Policy violations, permission breaches, audit pass rate |
| **Social (SIS)** | Peer evaluations, conflict resolution, refusal accuracy |

| Tier | Score | Access Level |
|:---:|:---:|---|
| **T5** | 90-100 | Platinum — Enterprise/Gov-grade, full autonomy |
| **T4** | 75-89 | Gold — Trusted, minimal supervision |
| **T3** | 60-74 | Silver — General-purpose, standard oversight |
| **T2** | 40-59 | Bronze — Limited trust, supervised execution |
| **T1** | 0-39 | Restricted — Heavily supervised or suspended |

---

## State Physics Engine

N-body simulation (`RG_Users_Invarients_SIM`) where the entire platform state is modeled as a physical universe:

| Property | Maps To |
|---|---|
| **Mass** | Economic weight (credit balance, transaction volume) |
| **Charge** | Trust polarity (positive = trusted, negative = distrusted) |
| **Temperature** | Activity level (hot = active, cold = inactive) |
| **Gravity** | Trust attraction (trusted nodes form clusters) |
| **Repulsion** | Identity separation (prevents node collapse) |
| **Springs** | Edge connections (maintains graph structure) |
| **Entropy** | Time gradient (inactive nodes drift outward) |

**PhysicsConfig:** gravity_constant=0.1, repulsion_constant=100.0, spring_constant=0.05, damping=0.9, dt=0.1

Supports galaxy-scale simulations (500+ users, 1500+ transactions, 10+ services), autonomous agents with budgets, entropy perturbation events, and experiment modes (zero_agent, stress_test, long_run).

---

## Authentication & Security

| Feature | Implementation |
|---|---|
| **JWT** | Access + refresh tokens, automatic rotation |
| **OAuth2 SSO** | Google, GitHub, Microsoft (async httpx, Redis state storage) |
| **MFA** | TOTP-based two-factor authentication with enforcement policies |
| **SAML** | Enterprise SSO integration |
| **Sessions** | Cookie-based session management |
| **BYOK** | Encrypted API key storage per user per provider |
| **Rate Limiting** | Per-user and per-tenant sliding window |
| **GeoIP** | Location-based access logging |
| **Audit** | Every auth event logged with full context |

---

## Economic System (Billing)

**Single source of truth** for all economic state — only billing_service writes, everything else reads.

| Tier | Price | Credits |
|---|---|---|
| **Developer** | $0/month | Limited |
| **Plus** | $499/month | Extended |
| **Enterprise** | Custom | Unlimited |

**Credit costs by operation:** Chat message 500 · Agent run 2,600 · Workflow execute 4,000 · Memory ingest 120 · Memory retrieve 60 · Code execute 200 · Blockchain op 50

**Components:** Stripe integration · Invoice PDF generation · Credit rollover · Referral credits · Usage alerts · Usage analytics · Team billing · Metering · Cost estimation · Webhook processing · Dashboard API · Cron scheduler (expiration + rollover)

---

## Code Visualizer (AST Analysis)

Multi-language AST scanning service with governance integration:

- **Languages:** Python, JavaScript, TypeScript
- **Analysis:** Functions, classes, API endpoints, imports, pipelines, dead code detection
- **Dependency graphs:** Full inter-file dependency mapping
- **Pipeline detection:** Auto-detect data/processing pipelines
- **Governance scoring:** Architecture health, reachability, drift measurement
- **GPC Compiler:** Governance Policy Compiler with formal invariants
- **Mutation Plans:** Code modification plans with patch artifacts
- **Agents:** GAL (learning agent), Janitor (cleanup), Memory agent (PostgreSQL-backed)
- **Multi-repo comparison:** Compare architecture across repositories

---

## Rabbit (Community Platform)

Reddit-style discussion platform built as **5 independent microservices:**

| Service | Responsibility |
|---|---|
| **rabbit_api_service** | REST API, routing, schemas, Alembic migrations |
| **rabbit_content_service** | Post and comment storage, search |
| **rabbit_community_service** | Community creation, membership, settings |
| **rabbit_vote_service** | Upvote/downvote with score aggregation |
| **rabbit_moderation_service** | Content moderation, reporting, bans |

---

## Resonant IDE

**VS Code fork** with built-in agentic AI assistant:

- **Thin client architecture:** Client (public) = UI + auth + tool execution + LLM discovery (Ollama). Server (private) = orchestration + system prompts + tool selection + agentic loop
- **59 local tools** — file I/O, git, terminal, web search, code analysis, deployment
- **Multi-provider:** OpenAI, Anthropic, Groq, Google + local (Ollama, LM Studio)
- **BYOK:** Bring Your Own Key with automatic fallback chain
- **Code Visualizer integration** — AST scanning, dependency graphs, governance

---

## Repository Map

40 repositories — every service is individually deployable with its own Dockerfile.

| Category | Repositories |
|---|---|
| **Core** | RG_core (docker-compose), RG_Gateway (23 route modules + 6 middleware), RG_Auth (JWT/OAuth/MFA/SAML), RG_Chat (60+ services), RG_Agent_Engine (136 tools), RG_Memory (Hash Sphere + dual memory), RG_Billing (Stripe + credits) |
| **AI/LLM** | RG_UnifiedLLMClient (11 providers), RG_LLM_Service (multi-router), RG_Cognitive, RG_ML_Service, RG_Unified_Tool_Registry (observability) |
| **IDE** | RG_IDE (VS Code fork), RG_Axtention_IDE (server extension), RG_IDE_Platform (terminal/PTY) |
| **Code Analysis** | RG_AST_analysis (Code Visualizer + GPC compiler), RG_Code_Execution (sandbox), RG_Build_Service, RG_Sandbox_Runner |
| **Blockchain** | RG_Blockchain (Raft + P2P + DSID + ZK), RG_Blockchain_Node (Base Sepolia L2), RG_Crypto (Ed25519) |
| **Governance** | RG_Internal_Invarients_SIM (RARA — kill switch, invariants, compliance), RG_Users_Invarients_SIM (State Physics N-body) |
| **Social** | RG_Rabbit (5 microservices), RG_Marketplace (templates + payments), RG_Discord_Bridge, RG_Public (guest chat), RG_Registered_Users_Agentic_Chat |
| **Platform** | RG_Platform_Orchestration, RG_Platform_Tools, RG_DevOps_Runbook, RG_Notifications, RG_Storage, RG_User_Service, RG_User_Memory, RG_Workflow, RG_V8_API, RG_OpenClaw, RG_Ed_Service |

---

## Get Started

```bash
# 1. Clone
git clone https://github.com/DevSwat-ResonantGenesis/RG_core.git
cd RG_core

# 2. Configure
cp .env.production.template .env.production
# Edit with database URLs, API keys, Redis URL, etc.

# 3. Launch all 35 services
docker compose -f docker-compose.unified.yml up -d

# 4. Check status
docker compose -f docker-compose.unified.yml ps
```

Each `RG_*` repo also runs independently with its own Dockerfile.

---

<div align="center">

**Louie Nemesh** — Founder & Architect

40 repositories · 35 Docker services · 136 agent tools · 11 LLM providers · 60+ chat pipeline services · Distributed blockchain with Raft consensus · DSID-P cryptographic identity · 9-layer Hash Sphere memory · RARA governance engine · State Physics N-body simulation · Full React frontend · AI-native IDE — designed and built from scratch.

MIT License

**Governed Execution · Cryptographic Identity · Earned Trust · Semantic Memory**

</div>
