<div align="center">
  <a href="https://agent-runtime-protocol.com/">
    <img src="./images/ARP_Long_Transparent.png" alt="ARP Logo" width="80%">
  </a>
  <a href="https://agent-runtime-protocol.com/" target="_blank">
    <img src="https://img.shields.io/website?url=https%3A%2F%2Fagent-runtime-protocol.com%2F&up_message=https%3A%2F%2Fagent-runtime-protocol.com%2F&up_color=31aab6&down_message=unavailable&labelColor=1d636a" alt="Website Link">
  </a>
  <a href="https://agent-runtime-protocol.com/public_docs/" target="_blank">
    <img src="https://img.shields.io/website?url=https%3A%2F%2Fagent-runtime-protocol.com%2Fpublic_docs%2F&up_message=https%3A%2F%2Fagent-runtime-protocol.com%2Fpublic_docs%2F&up_color=31aab6&down_message=unavailable&label=documentation&labelColor=1d636a" alt="Docs Website Link">
  </a>
  <a href="https://www.reddit.com/r/AgentRuntimeProtocol/" target="_blank">
    <img src="https://img.shields.io/badge/reddit-r%2FAgentRuntimeProtocol-ff6314?logo=reddit" alt="Reddit">
  </a>
</div>

<div align="center">
  <h3>Capability-oriented infrastructure for reliable agentic systems.</h3>
  <h4>Open standard + runnable reference stack for capability-centric, bounded, auditable execution.</h4>
</div>

<div align="center">
  <a href="https://opensource.org/licenses/MIT" target="_blank"><img src="https://img.shields.io/pypi/l/arp-standard-model" alt="ARP Python Data Model License"></a>
  <a href="https://pypistats.org/packages/arp-standard-model" target="_blank"><img src="https://img.shields.io/pepy/dt/arp-standard-model" alt="PyPI - Downloads"></a>
  <a href="https://pypi.org/project/arp-standard-model/#history" target="_blank"><img src="https://img.shields.io/pypi/v/arp-standard-model?label=arp-standard-model&labelColor=1d636a" alt="ARP Standard Python Data Model Version"></a>
  <a href="https://pypi.org/project/arp-jarvis/#history" target="_blank"><img src="https://img.shields.io/pypi/v/arp-jarvis?label=arp-jarvis&labelColor=1d636a" alt="JARVIS Version"></a>
</div>

<div align="center">
  <a href="https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/agentruntimeprotocol/ARP_Standard" target="_blank"><img src="https://img.shields.io/static/v1?label=Dev%20Containers%20For%20ARP%20Standard&message=Open&color=blue&logo=visualstudiocode" alt="Open in Dev Containers"></a>
  <a href="https://codespaces.new/agentruntimeprotocol/ARP_Standard" target="_blank"><img src="https://github.com/codespaces/badge.svg" alt="Open ARP Standard in Github Codespace" title="Open ARP Standard in Github Codespace" width="150" height="20"></a>
</div>

---

> ## Imagine if agent capabilities were as portable as containers — and every run came with enforceable bounds and a replayable audit trail.

---

**Agent Runtime Protocol (ARP)** is open, framework-agnostic infrastructure for building **reliable, auditable, capability-bounded agentic systems** by treating agentic work as **capability engineering**:
- define what a capability can do (schemas + metadata),
- bound how it can be used (constraints + budgets + checkpoints),
- observe it (durable events + artifacts),
- compose it into hierarchical workflows.

ARP ships as an ecosystem:
- **ARP Standard (`spec/v1`)**: OpenAPI + JSON Schemas + conformance rules.
- **JARVIS**: the maintained first-party OSS reference stack implementing those contracts.
- **SDKs / templates / helper libs**: so you can build your own components and validate them.

COP framing: **Capability Oriented Programming (COP)** is the engineering mindset behind ARP/JARVIS — build around capabilities you can **evaluate, publish, and reuse with evidence**. Start here: https://agent-runtime-protocol.com/public_docs/fundamentals/cop/

> [!NOTE]
> ARP is actively evolving. If you’re building on it and want a feature, tell us via GitHub Discussions or [**r/AgentRuntimeProtocol**](https://www.reddit.com/r/AgentRuntimeProtocol/).

## Why ARP exists

Long-horizon, tool-using workflows remain hard to make reliable in production because:
- action spaces explode (tool catalogs grow),
- mistakes compound over long trajectories,
- “natural language as API” drifts,
- governance requires enforceable checkpoints and durable evidence (not best-effort prompts).

ARP provides standardized primitives to turn “works in a demo” into production grade systems.

## The node-centric model (what ARP standardizes)

ARP’s unit of composition is the **NodeType** (a versioned capability definition):
- **NodeType**: schemas + metadata + defaults for a capability (service, in-process node pack, or adapter).
- **Run**: a top-level execution record.
- **NodeRun**: one execution instance of a NodeType within a Run.

Two NodeType kinds:
- **Atomic**: “do the thing” (not decomposed further by ARP).
- **Composite**: “figure out how to do the thing” (decompose → map → execute → evaluate/recover).

Composite workflows are **controlled, bounded loops** (not fixed DAGs) and are only useful when they are:
- bounded by enforceable constraints (structure, candidates, budgets),
- governed by checkpoints (policy decisions),
- observable via durable events and artifacts.

ARP standardizes:
- versioned capability definitions (`NodeType`) and executions (`Run`, `NodeRun`)
- bounded mapping artifacts (`CandidateSet`) and enforceable limits (`ConstraintEnvelope`)
- policy checkpoints and durable event emission (NDJSON event timelines)
- authentication posture (JWT by default; STS token exchange for service-to-service calls)

ARP does **not** standardize:
- a planner algorithm,
- “the best prompts”,
- memory architectures,
- any single agent framework’s runtime model.

## JARVIS: the first-party reference stack

JARVIS is a maintained, batteries-included implementation of ARP `spec/v1` that demonstrates end-to-end composite execution with real cross-cutting concerns (auth, policy, observability, storage) using intentionally simple defaults.

Recommended way to run it: the pinned stack distribution repo **[`JARVIS_Release`](https://github.com/AgentRuntimeProtocol/JARVIS_Release)**.

Core `spec/v1` services:
- **Run Gateway** (edge API: start/query/cancel runs)
- **Run Coordinator** (run authority: lifecycle + enforcement + scheduling + history)
- **Atomic Executor** (executes atomic NodeRuns)
- **Composite Executor** (executes composite NodeRuns)
- **Node Registry** (versioned NodeType catalog)
- **Selection Service** (bounded candidate sets)
- **PDP** (policy decisions)

JARVIS-only internal services (non-spec, swappable):
- Run Store (durable Run/NodeRun state)
- Event Stream (NDJSON event persistence + streaming)
- Artifact Store (large I/O backing)

## Getting started (run the pinned stack)

Start here:
- Docs Quickstart: https://agent-runtime-protocol.com/public_docs/
- Stack repo: https://github.com/AgentRuntimeProtocol/JARVIS_Release

Minimal local run (Docker Compose):

```bash
git clone https://github.com/AgentRuntimeProtocol/JARVIS_Release
cd JARVIS_Release
cp compose/.env.example compose/.env.local
# set ARP_LLM_API_KEY and ARP_LLM_CHAT_MODEL in compose/.env.local
docker compose --env-file compose/.env.local -f compose/docker-compose.yml up -d
curl -sS http://127.0.0.1:8081/v1/health
```

Notes:
- `dev-secure-keycloak` is the default profile (JWT validation + token exchange via local Keycloak STS).
- `dev-insecure` disables inbound JWT checks for easier local iteration (dev only).

## Interop stance (MCP / A2A / frameworks)

ARP is designed to be **interop-first**: MCP tools and A2A endpoints can be represented as **atomic NodeTypes** (via adapters) so they inherit the same constraints, policy checkpoints, and audit surfaces.

## Key repos

- **ARP Standard (normative spec + SDKs):** https://github.com/AgentRuntimeProtocol/ARP_Standard
- **JARVIS pinned stack (Docker Compose):** https://github.com/AgentRuntimeProtocol/JARVIS_Release
- **Docs portal (Docusaurus):** https://github.com/AgentRuntimeProtocol/ARP_Docs
- **Helper libraries:**
  - `arp-auth` (OIDC client credentials + token exchange): https://github.com/AgentRuntimeProtocol/ARP_Auth
  - `arp-policy` (policy decisions + artifacts): https://github.com/AgentRuntimeProtocol/ARP_Policy
  - `arp-llm` (LLM provider profiles): https://github.com/AgentRuntimeProtocol/ARP_LLM
  - `arp-sts-keycloak` (dev STS tooling): https://github.com/AgentRuntimeProtocol/ARP_STS_KeyCloak
