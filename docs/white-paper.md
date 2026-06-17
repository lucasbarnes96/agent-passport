---
title: "Agent Passport: Foundational Identity for Autonomous Economic Actors"
version: "3"
date: "2026-06-17"
status: "Working document for discussion and iteration"
github: "https://github.com/lucasbarnes96/agent-passport"
---

# Agent Passport

## Foundational Identity for Autonomous Economic Actors

**A White Paper on Verifiable Identity, Trust, and Coordination Infrastructure for AI Agents**

Version 3 — Expanded Draft · June 17, 2026

> Working document for discussion and iteration. Not legal, regulatory, or financial advice.

## Executive Summary

Autonomous AI agents are becoming first-class economic actors. They discover information, negotiate, transact, delegate, and coordinate at machine speed across digital (and increasingly physical) environments.

Existing rails enable action. What is missing is a foundational, portable identity layer — the equivalent of human passports, KYC processes, corporate registries, and verifiable credentials combined into one machine-native system.

**Agent Passport** (implemented as a simple, portable `PASSPORT.md` file in an Open Knowledge Format style) provides exactly that:

- A standardized, verifiable digital identity for any agent.
- Binding to sponsors, capabilities, permissions, and history.
- Support for reputation, attestations, and dynamic trust signals.
- Interoperability across platforms, protocols (MCP, x402, A2A), and chains (via ERC-8004 patterns).
- Foundation for risk assessment, compliance, access control, financial services, and multi-agent coordination.

This is broader than risk/insurance alone. Just as a human passport enables travel, banking, employment, and legal participation, an Agent Passport enables discovery, authorization, accountability, and economic participation for software actors.

**Key benefits include:**

- **Discovery & Interoperability:** Agents can be found, understood, and interacted with consistently.
- **Trust & Authorization:** Verifiable claims about capabilities, history, and constraints (KYA — Know Your Agent).
- **Accountability & Compliance:** Binding to responsible entities with auditable records.
- **Economic Enablement:** Portable reputation and credentials that support lending, insurance, payments, and delegation.
- **Risk Management:** Structured data for dynamic scoring, benchmarking, and targeted protection (one powerful use case among many).

The result: Agents become first-class, accountable participants in digital economies — not opaque black boxes.

## 1. The Emerging Need for Agent Identity

AI agents are evolving from chat-based assistants into autonomous systems that plan, use tools, execute actions, and interact with other agents and systems.

**Current challenges:**

- Every new agent or platform reinvents context, identity, and trust assembly.
- No portable way to verify "who" an agent is, "what" it can do, or "why" it should be trusted.
- Delegation chains and multi-agent systems create accountability gaps.
- Rapid evolution (model changes, new tools, behavioral drift) makes static approaches obsolete.
- Lack of standardized identity hinders interoperability, compliance, and safe scaling.

Human societies solved similar problems with layered identity systems: passports for travel and basic identity, KYC for financial participation, driver's licenses for specific privileges, corporate registries for legal entities, and credit scores for economic reputation.

Agent Passport applies the same principle to software actors in a machine-native, portable format.

### 1.1 What Is an Agent? (Scope and Definition)

For this framework, an **AI agent** is a software system that uses AI to perceive inputs or environments, reason toward goals, plan and execute sequences of actions (including tool use), adapt based on outcomes, and operate with a meaningful degree of autonomy — without requiring continuous human intervention for every decision.

**Important Distinctions:**

- **Autonomy Level:** Ranges from highly scaffolded/harnessed agents (strong external orchestration and oversight) to self-contained agents (persistent state, dedicated resources, long-horizon independent operation).
- **Resource Access:** Some agents operate within tightly controlled environments with mediated compute and permissions. Others have direct access to wallets, APIs, compute instances, data stores, or even physical systems.
- **Action Capability:** The ability to initiate effects in the world (payments, code changes, data modifications, physical actions) is what creates economic and risk exposure.

This framework focuses on agents with action capability and meaningful autonomy, as these are the ones that participate in economic and operational systems and therefore benefit most from portable, verifiable identity.

**Legal Context:** Policy experiments such as Argentina's proposed "non-human corporations" (entities operated by AI agents/robots with optional human shareholders) highlight the direction toward treating sufficiently autonomous agents as capable of running economic entities. Robust identity infrastructure is a prerequisite for accountability in such models.

## 2. The Agent Passport Concept

The Agent Passport is a portable, verifiable digital identity artifact for AI agents.

**Core Analogy to Human Systems:**

| Human System | Agent Equivalent |
| --- | --- |
| Passport | Basic portable identity and participation rights |
| KYC / Digital Agent Passport | Verified identity bound to responsible entities |
| Driver's License | Scoped capability credentials |
| Corporate Registry | Entity-level identity and limited liability |
| Credit File | Historical behavior and trustworthiness |

**Implementation:** A simple, elegant file-based format (`PASSPORT.md`) using Markdown + structured YAML frontmatter (inspired by the Open Knowledge Format style). This keeps it:

- Human-readable and editable.
- Machine-parseable.
- Git-native and versionable.
- Extremely portable (files, repos, tarballs, filesystems).
- Easy to extend and integrate.

**Example Structure (high-level):**

```yaml
---
type: agent-passport
title: "Procurement-Agent-v3.2"
agent_id: "eip155:1:0x..."
version: "3.2.1"
sponsor: "Entity or Human ID"
capabilities: ["vendor-discovery", "invoice-processing", "payment-initiation"]
permissions:
  max_single_txn: 50000
  requires_approval_above: 10000
attestations:
  - type: benchmark
    name: "procurement-v1"
    score: 87
    date: "2026-06-01"
  - type: platform
    source: "Stripe-MCP"
    successful_txns_30d: 1247
reputation_signals:
  - type: onchain
    registry: "ERC-8004"
    score: "..."
status: active
timestamp: "2026-06-17T00:00:00Z"
---

# Rich Markdown Content
## Description
## History & Evidence
## Sponsorship & Delegation
```

The frontmatter holds queryable structured data. The body holds narrative, evidence, and context.

This format aligns with emerging real-world efforts:

- ERC-8004 on-chain identity registries (NFT-based agent IDs with metadata).
- Know Your Agent (KYA) frameworks from multiple vendors.
- Digital Agent Passport concepts already deployed in commerce.
- NIST, IETF, OpenID Foundation, and NCCoE work on agent identity and authorization standards.

## 3. Benefits of an Agent Passport (Beyond Risk)

While risk assessment and insurance are powerful applications, the Agent Passport delivers broad value as foundational identity infrastructure:

### 3.1 Discovery and Interoperability

Agents can be discovered, described, and understood consistently across platforms. Portable metadata reduces integration friction and enables agent-to-agent economies.

### 3.2 Authentication, Authorization, and Access Control

Verifiable proof of identity and authorized scope before actions. Supports least-privilege principles and complements OAuth, SPIFFE/SVID, and workload identity with agent-specific capability binding.

### 3.3 Accountability and Auditability

Binds agents to sponsors or responsible entities. Creates auditable records and supports KYA processes analogous to KYC.

### 3.4 Reputation and Trust Signals

Accumulates attestations from benchmarks, platforms, and interactions. Portable reputation that travels with the agent across ecosystems.

### 3.5 Enabling Financial and Economic Services

Verifiable identity + history + attestations support lending, credit, and insurance. Staking and collateral mechanisms can be tied directly to the passport.

### 3.6 Legal and Governance Wrappers

Provides the identity layer needed for corporate structures (DAO LLCs, non-human corporations). Supports delegation chains with clear provenance.

### 3.7 Multi-Agent Coordination and Delegation

Clear identity and capability claims enable safe delegation and orchestration in complex agent networks.

### 3.8 Security and Governance at Scale

Helps organizations discover, classify, govern, and decommission agents. Supports Zero Trust approaches and reduces the "many hands" problem in multi-provider deployments.

## 4. Path to Insurance

Insurance is one of the most consequential applications of Agent Passport — and the long-term focus of Clara.

**The stack:**

1. **Payment rails** (Coinbase, x402, stablecoins) let agents transact.
2. **Legal wrappers** (Argentina Sociedad Automatizada, DAO LLCs) may grant personhood.
3. **Agent Passport** provides verifiable identity, capabilities, and history.
4. **Insurance** converts tail risk into a priced commitment — social permission for autonomous actors to operate at scale.

Without identity, underwriting is guesswork. Without insurance, counterparties won't trust agents with meaningful exposure. Passport-backed signals enable:

- Dynamic risk scoring from benchmark attestations and transaction history.
- Parametric triggers (treasury drain, reputation collapse, behavioral drift).
- Proof-of-coverage as a protocol primitive for marketplaces and B2B contracts.
- On-chain pools and mutuals where regulated markets move too slowly.

Clara's moonshot: **insurance for autonomous actors**, built on Agent Passport as the underwriting substrate.

## 5. Technical and Standards Alignment

The Agent Passport is designed to be lightweight and composable:

- **Format:** Markdown + YAML frontmatter (OKF-inspired) for the canonical artifact.
- **On-Chain Layer:** Aligns with ERC-8004 for discoverability, portable IDs, and on-chain signals.
- **Verification:** Cryptographic attestations, platform integrations (MCP, x402), and optional zero-knowledge proofs.
- **Ecosystem:** Compatible with KYA frameworks, Digital Agent Passport concepts, NIST agent identity efforts, and OpenID Foundation agentic identity work.

## 6. Roadmap and Next Steps

**Immediate:**

- Finalize `PASSPORT.md` schema and reference examples.
- Map core fields to ERC-8004 and KYA concepts.
- Produce tooling prototypes (validators, visualizers, enrichment agents).

**Short term:**

- Pilot with specific agent personas and platforms.
- Integrate with benchmark/evaluation systems for attestations.
- Publish updated white paper and open schema for feedback.

**Medium term:**

- Build reference implementations and integrations with major rails and frameworks.
- Explore on-chain reputation and validation extensions.
- Engage standards bodies and ecosystem partners.

**Moonshot:**

- Passport-backed parametric insurance products.
- On-chain liquidity pools and mutual structures.
- Proof-of-coverage as composable infrastructure.

Success will be measured by adoption of the portable identity artifact and the emergence of an ecosystem of tools, attestations, and services built around it.

## 7. Conclusion

The agentic future needs more than action rails — it needs identity rails.

Agent Passport provides a simple, elegant, and powerful foundation: a portable digital identity that makes agents discoverable, verifiable, accountable, and economically integrable.

By drawing on the proven power of human identity systems while embracing machine-native formats and on-chain primitives, we can accelerate safe, scalable adoption of autonomous agents.

This is not just about managing risk. It is about giving agents the identity infrastructure they need to participate fully and responsibly in the digital economy.

We invite collaboration on the specification, tooling, pilots, and standards development.

## References & Further Reading

- Google Cloud Open Knowledge Format (OKF)
- ERC-8004: Trustless Agents (Ethereum standard for agent identity and reputation)
- Know Your Agent (KYA) frameworks (Trulioo Digital Agent Passport, Sumsub, AstraSync, and others)
- Workday Agent Passport (enterprise agent verification and monitoring)
- NIST AI Agent Standards Initiative and NCCoE work on software/AI agent identity
- IETF and OpenID Foundation efforts on agent authentication and identity management
- Open Agent Passport (OAP) specification for pre-action authorization
- Argentina non-human corporations legislative proposals (2026)

---

**Agent Passport** — Foundational Identity for Autonomous Economic Actors

Version 3 · June 17, 2026 · For discussion and collaboration.

Canonical source: [github.com/lucasbarnes96/agent-passport](https://github.com/lucasbarnes96/agent-passport)
