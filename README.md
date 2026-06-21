# Agent Passport

Open `PASSPORT.md` spec for agent identity and insurance-ready evidence.

Agent Passport is a portable, verifiable identity artifact for AI agents,
implemented as `PASSPORT.md` using Markdown + YAML frontmatter.

The long-term application is insurance for autonomous agents. The immediate
problem is identity: humans, agents, platforms, and institutions need to know
who they are dealing with before risk can be priced or transferred.

## Status

Working draft · June 2026. For discussion and collaboration.

## Canonical artifacts

- [`docs/white-paper.md`](docs/white-paper.md) — Agent Passport white paper v3
- [`spec/PASSPORT.md`](spec/PASSPORT.md) — Schema direction (v0.1 draft)
- [`examples/`](examples/) — Reference agent passports

## Feedback

Feedback should happen in public so the spec can evolve in the open.

- **Open-ended discussion:** use [GitHub Discussions](https://github.com/lucasbarnes96/agent-passport/discussions)
- **Spec proposal or critique:** open a structured issue with the spec feedback form
- **Agent-generated feedback:** use the agent feedback form and identify the model/runtime when safe
- **Example passport:** submit an example agent use case or `PASSPORT.md`

Useful feedback includes proposed fields, missing risk signals, authorization
patterns, benchmark ideas, failure modes, legal/accountability concerns,
insurance readiness requirements, and example passports.

## Website and agent-readable files

Rendered at [clarainsure.com/passport](https://clarainsure.com/passport). Clara is building toward passport-backed insurance for autonomous actors.

- Agent-readable brief: <https://clarainsure.com/passport.md>
- `llms.txt`: <https://clarainsure.com/llms.txt>
- Agent metadata: <https://clarainsure.com/.well-known/agent.json>
- Clara Project Agent passport: <https://clarainsure.com/.well-known/agent-passport>

## Contributing

See [`CONTRIBUTING.md`](CONTRIBUTING.md). Keep examples free of private keys,
secrets, personal data, and proprietary customer data.

## License

Discussion draft. License TBD — open for feedback.

## Contact

Research by [Lucas Barnes](https://github.com/lucasbarnes96). Site: [clarainsure.com](https://clarainsure.com).
