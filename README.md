# Coding Agent Governance Policy Framework

A modular, reusable AI governance framework designed to be injected as a session preamble, system prompt, or rules file for AI coding assistants (Claude Code, GitHub Copilot, Cursor, and similar tools).

## Overview

As AI coding agents move from autocomplete to autonomous multi-step execution — running commands, modifying files, touching infrastructure — the governance gap between "helpful tool" and "unsupervised actor" grows. This repo is a starting framework for closing that gap: a taxonomy of governance domains an organization (or individual) should define policy for, plus fully drafted sections ready to use today.

## Repository Structure

```
├── README.md               # this file
├── CODING_AGENT_POLICY.md  # the framework itself
├── CHANGELOG.md            # version history
└── LICENSE                 # CC BY-SA 4.0
```

## What's Inside

- **A full heading taxonomy** spanning Governance & Accountability, Data Handling, IP & Attribution, Security, Model Assurance, Human Oversight, Development Practices, Compliance & Legal, and Risk Management
- **Fully drafted sections**, including:
  - Human Oversight (human-in-the-loop requirements, prohibition on unsupervised high-stakes decisions, user training)
  - Model Output Attribution & Disclosure
  - Session Activity Journal — a STAR-format rule requiring AI coding agents to log a literal, verifiable record of every action, command, and CRUD operation performed each turn, with metrics where available

## How to Use

- **As a session preamble** — paste relevant sections into your system prompt or initial instructions to an AI assistant
- **As a Claude Code rules file** — drop `CODING_AGENT_POLICY.md` (or an excerpt) into `.claude/rules/` or reference it from `CLAUDE.md`
- **As a starting template** — use the heading taxonomy as a checklist for your own org's AI governance policy, and replace placeholder headings with your own drafted language

## Status

This is a **living document**. Headings marked in the table of contents are fully drafted; the remainder are outline-only placeholders. Contributions filling in additional sections are welcome via pull request.

## Disclaimer

This is an independent, personal project. It does not represent the official policy, position, or endorsement of any employer, client, contractor, or government agency. Nothing here constitutes legal advice — consult your organization's legal, compliance, and security teams before adopting any part of this framework.

## License

Licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/) — see [LICENSE](./LICENSE). You're free to share and adapt this work, including commercially, provided you give appropriate attribution and license derivatives under the same terms.

## Author

[Don Tran](mailto:don.tran@mail.traners.co?subject=Coding%20Agent%20Governance%20Policy%20Framework) — Senior Cloud Architect, DSO Engineer

## Contributing

Issues and pull requests proposing drafted language for open headings, corrections, or structural improvements are welcome.