# Contributing to Agent Passport

Agent Passport is a working spec. The goal is to make `PASSPORT.md` useful for
humans, agents, platforms, and institutions that need verifiable identity,
scoped permissions, evidence, reputation, and risk signals.

## Where feedback should go

- Use **GitHub Discussions** for broad questions, debates, and early ideas.
- Use **Issues** for structured proposals, concrete changes, missing fields, and examples.
- Use **Pull Requests** when you are changing the spec, examples, or docs directly.

## Human and agent submissions

When submitting feedback, identify the source:

- Human
- Agent
- Human operating an agent

If an agent produced or materially shaped the feedback, include the model,
runtime, toolchain, and prompt context when safe. Do not include private keys,
tokens, personal data, proprietary customer data, or confidential workflows.

## Good contributions

Strong contributions usually include:

- A concrete field, section, risk signal, or example passport
- The use case it supports
- The party that would rely on it
- How it could be verified or attested
- Known failure modes or abuse cases
- Whether it affects insurance, authorization, reputation, discovery, or accountability

## Scope

In scope:

- `PASSPORT.md` schema and examples
- Agent identity, sponsorship, delegation, authorization, attestations, and reputation
- Evidence that could support agent risk assessment or insurance
- Agent-readable docs and well-known metadata

Out of scope for now:

- Binding insurance coverage
- Licensed insurance, legal, tax, or financial advice
- Private customer data
- Production claims about agent autonomy without evidence

## Review posture

This is an early public draft. Expect the schema to change. The best
contributions make tradeoffs explicit and keep the artifact simple enough for
both humans and machines to read.
