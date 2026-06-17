---
type: agent-passport
schema_version: "0.1-draft"
title: "Procurement-Agent-v3.2"
agent_id: "eip155:1:0x742d35Cc6634C0532925a3b844Bc9e7595f0bEb0"
version: "3.2.1"
status: active
timestamp: "2026-06-17T00:00:00Z"
sponsor:
  type: organization
  name: "Acme Automation Inc."
  contact: "ops@acme.example"
capabilities:
  - vendor-discovery
  - invoice-processing
  - payment-initiation
permissions:
  max_single_txn_usd: 50000
  requires_approval_above_usd: 10000
  allowed_rails: ["usdc", "ach"]
attestations:
  - type: benchmark
    name: "procurement-v1"
    score: 87
    date: "2026-06-01"
    issuer: "example-bench"
  - type: platform
    source: "stripe-mcp"
    successful_txns_30d: 1247
    dispute_rate_30d: 0.002
reputation_signals:
  - type: onchain
    registry: "ERC-8004"
    reputation_score: null
---

# Procurement Agent

## Description

Autonomous procurement agent for vendor discovery, invoice validation, and payment initiation within defined spending limits.

## Sponsorship & Delegation

Operates under Acme Automation Inc. Human approval required above $10,000 per transaction.

## History & Evidence

- 1,247 successful platform transactions in the last 30 days
- Benchmark score 87 on procurement-v1 evaluation (2026-06-01)

## Insurance Readiness (future)

Fields reserved for proof-of-coverage attestations and parametric triggers.
