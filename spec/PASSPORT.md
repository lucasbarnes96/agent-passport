# PASSPORT.md Specification (v0.1 Draft)

> Working draft. See [white paper](../docs/white-paper.md) for full context.

## Format

- File name: `PASSPORT.md`
- Structure: YAML frontmatter + Markdown body
- Inspired by Open Knowledge Format (OKF) portability

## Required frontmatter fields (v0.1)

| Field | Type | Description |
| --- | --- | --- |
| `type` | string | Must be `agent-passport` |
| `schema_version` | string | Spec version (e.g. `0.1-draft`) |
| `title` | string | Human-readable agent name |
| `agent_id` | string | Stable identifier (wallet, ERC-8004, URI) |
| `version` | string | Agent software/config version |
| `status` | string | `active`, `suspended`, `deprecated` |
| `timestamp` | string | ISO 8601 last-updated time |
| `sponsor` | object | Responsible entity binding |

## Recommended fields

- `capabilities` — list of capability strings
- `permissions` — spending limits, scopes, approval thresholds
- `attestations` — benchmarks, platform signals, certifications
- `reputation_signals` — on-chain or off-chain trust data
- `legal_wrapper` — entity type and jurisdiction (when applicable)

## Markdown body sections

Suggested sections (flexible):

1. Description
2. Sponsorship & Delegation
3. History & Evidence
4. Insurance / coverage readiness (future)

## Validation

Validator tooling planned. See Clara roadmap: [clarainsure.com/roadmap](https://clarainsure.com/roadmap).

## Interoperability targets

- MCP (agent tool context)
- x402 (payment-aware agents)
- ERC-8004 (on-chain identity and reputation)
- Emerging KYA / Digital Agent Passport frameworks
