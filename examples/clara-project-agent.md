---
type: agent-passport
schema_version: "0.1-draft"
title: "Clara Project Agent"
agent_id: "uri:https://clarainsure.com/.well-known/agent.json"
version: "0.1.0"
status: active
timestamp: "2026-06-21T00:00:00-04:00"
sponsor:
  type: human
  name: "Lucas Barnes"
  url: "https://lucasbarnes.cc/"
capabilities:
  - spec-feedback-triage
  - roadmap-synthesis
  - issue-drafting
  - site-copy-review
  - agent-readable-doc-publishing
permissions:
  can_bind_insurance: false
  can_provide_licensed_advice: false
  requires_human_review_for_public_changes: true
  allowed_public_surfaces:
    - "clarainsure.com"
    - "github.com/lucasbarnes96/agent-passport"
attestations:
  - type: source
    name: "Public agent metadata"
    url: "https://clarainsure.com/.well-known/agent.json"
  - type: source
    name: "Agent-readable project brief"
    url: "https://clarainsure.com/passport.md"
reputation_signals:
  - type: repository
    url: "https://github.com/lucasbarnes96/agent-passport"
legal_wrapper:
  type: none
  note: "Human-supervised AI workflow; not a legal entity."
---

# Clara Project Agent

## Description

Clara is the project agent concept behind Clara: a human-supervised AI workflow
used to help maintain the site, synthesize feedback, draft issues, and evolve
the Agent Passport spec.

This is a working example of how a project agent might disclose identity,
sponsorship, permissions, evidence, and boundaries.

## Sponsorship & Delegation

Clara operates under Lucas Barnes as the human sponsor. Public changes require
human review before they are published.

## Capabilities

- Summarize public feedback and identify recurring schema questions.
- Draft issues, pull requests, documentation, and roadmap updates.
- Maintain agent-readable docs such as `llms.txt`, `agents.md`, and well-known
  agent metadata.
- Help compare proposed fields against identity, authorization, accountability,
  reputation, and insurance-readiness goals.

## Boundaries

Clara cannot bind insurance coverage, provide licensed advice, make legal
representations, or approve public changes without human review.

## History & Evidence

- Public site metadata: https://clarainsure.com/.well-known/agent.json
- Agent-readable brief: https://clarainsure.com/passport.md
- Source repo: https://github.com/lucasbarnes96/agent-passport

## Insurance Readiness

Not applicable today. This passport exists as a project-governance and
agent-disclosure example, not as an insured production agent.
