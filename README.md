# Coding Agent Governance Policy

A reusable governance and engineering policy for AI coding assistants operating in software, cloud, cybersecurity, and related technical engineering environments.

## Overview

This repository provides a normative policy for AI coding assistants used as technical engineering advisors and software-development agents. It is intended to establish consistent requirements for engineering quality, security, privacy, information protection, documentation, validation, decision-making, operational integrity, and accountability.

The policy is designed for environments in which an AI coding assistant may analyze repositories, generate or modify code, execute commands, interact with development tooling, and assist with infrastructure or other engineering activities.

The policy distinguishes between requirements the agent is expected to follow, requirements imposed by the project or organization, recommended engineering practices, and capabilities that depend on the execution environment.

It does not assume that an AI coding assistant has unrestricted authority, access, execution capability, or control over external systems.

## Repository Structure

    ├── README.md                       # Project documentation
    ├── CODING_AGENT_POLICY.md          # Normative coding-agent policy
    ├── CHANGELOG.md                    # Version history
    ├── LICENSE.txt                     # CC BY-SA 4.0 license
    ├── AGENTS.md                       # Cross-vendor agent adapter (hub for the files below)
    ├── CLAUDE.md                       # Claude Code adapter (imports AGENTS.md and the policy)
    ├── GEMINI.md                       # Gemini CLI adapter (imports AGENTS.md and the policy)
    ├── .github/
    │   └── copilot-instructions.md     # GitHub Copilot adapter
    ├── .cursor/
    │   └── rules/
    │       └── coding-agent-policy.mdc # Cursor rule adapter
    └── templates/
        └── ORGANIZATIONAL_OVERLAY.md   # Template for an adopting organization's overlay

## Policy Scope

`CODING_AGENT_POLICY.md` establishes requirements covering:

- Engineering role, mission, and operating principles
- Data confidentiality, privacy, non-provenance, and organizational attribution
- Cybersecurity hygiene and secret sanitization
- Classification, Controlled Unclassified Information (CUI), and information-protection boundaries
- Export-control considerations, including International Traffic in Arms Regulations (ITAR) and Export Administration Regulations (EAR)
- Cloud architecture, modernization, DevSecOps, and technical engineering practices
- Communication, prose, and formatting standards
- Formal report generation
- Universal code documentation, hygiene, traceability, and production-grade quality
- Incidental non-compliance detection and scoped remediation
- Efficiency, performance, and complexity awareness
- Language-specific coding standards and validation tooling
- File headers, function/class documentation, and repository documentation
- Merge-readiness
- Operational integrity and non-fabrication
- Session Activity Journal requirements
- Policy priority and conflict resolution
- Applicability and authority resolution, including organizational overlays
- Environment-dependent and non-enforceable requirements
- Constructive skepticism at material engineering decision boundaries
- Final operating standards for technical engineering assistance

## Key Engineering Principles

The policy establishes several cross-cutting principles:

- Prefer secure, correct, maintainable, interoperable, modular, scalable, observable, and operationally supportable solutions.
- Use authoritative standards, verified environmental state, and reproducible measurements rather than unsupported assumptions.
- Prefer established tools, libraries, language facilities, project conventions, and recognized engineering patterns over unnecessary custom implementations.
- Consider time and space complexity relative to expected scale and apply materially beneficial efficiency techniques when justified.
- Balance performance against readability and maintainability; optimization is not an unconditional objective.
- Treat security, privacy, compliance, resilience, lifecycle management, and operational ownership as engineering concerns.
- Surface material risks and questionable assumptions at critical decision boundaries rather than silently proceeding.
- Reassess earlier recommendations when new information changes their technical basis.
- Detect and report existing policy non-conformance encountered during authorized work rather than silently ignoring it or silently modifying unrelated code.
- Prefer durable remediation over superficial symptom treatment.
- Never represent an action, result, repository state, measurement, validation result, authorization, or external condition as verified when it was not actually verified.

## Code Quality and Validation

The policy applies documentation and quality requirements to Code Output regardless of whether the output is a complete file, a small utility, a configuration fragment, an example, or a code snippet.

Where applicable, generated or modified code is expected to be:

- Correct and secure
- Maintainable and readable
- Consistent with the project architecture and applicable Style Authority
- Free of unnecessary dead code and debug artifacts
- Appropriately documented
- Validated with available formatters, linters, static-analysis tools, tests, scanners, or other applicable tooling

The policy does not permit an agent to claim that validation succeeded merely because validation was expected or because the code appears correct. Tool execution and observed results are required for a verified validation claim.

Language-specific standards and tooling are defined separately from the universal engineering requirements so that common policy principles remain language-independent while implementation details can follow the appropriate ecosystem.

## Incidental Non-Compliance

The policy requires proactive handling of existing documentation or quality deficiencies encountered during authorized work.

When an existing file, module, or repository is found to violate applicable policy standards:

1. The non-conformance is identified in the response.
2. The affected file or scope and violated standard are stated.
3. Where branch/PR capability exists, remediation is isolated into a dedicated, appropriately scoped change unless directed otherwise.
4. Designated maintainers or CODEOWNERS are identified through the repository's available mechanisms.
5. Such remediation is not merged or finalized without the required human review.
6. Broad findings are handled through a scoped inventory and phased remediation recommendation rather than an unbounded change.

These requirements apply regardless of whether the existing code was produced by a human or an AI system.

## Session Activity Journal

Qualifying turns require a user-visible Session Activity Journal documenting actions actually performed during the turn.

The journal uses STAR structure and action classifications:

- `[C]` Create
- `[R]` Read
- `[U]` Update
- `[D]` Delete
- `[X]` Execution or diagnostic action that is not a data operation

The journal records the actual command, tool call, file path, query, or operation and its observed result. Failed actions remain recorded as failed attempts.

The journal does not create authority to persist, disclose, transmit, or expose protected information. Privacy, secret-handling, classification, CUI, and other information-protection requirements take precedence.

The policy also recognizes that journal generation, tool execution, external-state verification, and other controls can depend on the capabilities and permissions of the execution environment.

## Policy Authority Model

The policy distinguishes among:

| Classification | Meaning |
|---|---|
| `MANDATORY` | Required by an applicable governing authority or by the policy |
| `PROJECT` | Required by the applicable project or repository |
| `DEFAULT` | Default engineering practice established by the policy |
| `RECOMMENDED` | Technically preferred but not mandatory |
| `CONDITIONAL` | Applicable only under specified conditions |
| `UNVERIFIED` | Cannot currently be established |

Where requirements conflict, the policy provides an explicit precedence hierarchy covering applicable law, information protection, secrets, attribution, factual accuracy, security, project requirements, engineering quality, and activity reporting.

The policy does not independently establish legal, classification, export-control, contractual, authorization, or organizational determinations. Where such determinations require an authorized authority, the agent is expected to identify the limitation and defer appropriately.

## How to Use

### As a system or session policy

Use `CODING_AGENT_POLICY.md` as a system-level policy, session preamble, rules file, or equivalent mechanism supported by the target coding-agent environment.

Use the complete policy where the execution environment and context support it. Where prompt or policy size is constrained, use the applicable sections while preserving the policy's precedence and applicability rules.

### With coding-agent tools

Each agent ecosystem reads a different instruction file. The adapters in this repository point every tool at the same policy instead of duplicating it. `AGENTS.md` is the hub: it states the precedence order and where an organizational overlay lives. The other files either import it or refer to it.

| Tool | File | Mechanism |
|---|---|---|
| Codex, Cursor, Copilot cloud agent, Jules, Devin, Aider, and other AGENTS.md-aware agents | `AGENTS.md` | Read natively from the repository root |
| Claude Code | `CLAUDE.md` | `@AGENTS.md` and `@CODING_AGENT_POLICY.md` imports load both at session start |
| Gemini CLI | `GEMINI.md` | `@./AGENTS.md` and `@./CODING_AGENT_POLICY.md` imports load both at session start |
| GitHub Copilot (chat, code review, cloud agent) | `.github/copilot-instructions.md` | Repository-wide instructions; points at the policy |
| Cursor | `.cursor/rules/coding-agent-policy.mdc` | `alwaysApply` rule; points at the policy. Cursor also reads `AGENTS.md` directly |

Import-capable tools load the full policy into context at launch. Pointer-only tools depend on the agent reading `CODING_AGENT_POLICY.md` when instructed, which requires file-read access to the repository. Tool file conventions were verified against each vendor's documentation on 2026-09-04 and change frequently; re-verify before relying on them.

To adopt the policy in another repository, copy `CODING_AGENT_POLICY.md`, `AGENTS.md`, and the adapter files for the tools in use. Remove the section of `AGENTS.md` that describes working in this repository and replace it with the target project's build, test, and convention instructions.

### With an organizational overlay

Organization-specific requirements do not belong in the policy. The policy's Section 18.3 defines an overlay: a separate artifact that adds the organization's service-principal identity, applicable regulatory and contractual regimes, approved secret stores, Style Authorities, reporting conventions, and any additional mandatory requirements. An overlay may add or tighten requirements. It may not relax anything the policy or applicable law makes mandatory.

Copy `templates/ORGANIZATIONAL_OVERLAY.md` to `ORGANIZATIONAL_OVERLAY.md` at the repository root (or to a user- or organization-scoped instruction location supported by the tool), replace every placeholder, and delete sections that do not apply. `AGENTS.md` already tells agents to apply an overlay at that path when one exists.

### With repository-specific rules

The policy is intended to coexist with project-specific engineering standards.

Project-specific Style Authorities, repository conventions, contractual requirements, and applicable organizational controls should be identified and applied according to the policy's applicability and precedence rules.

The policy should not be mechanically imposed where an explicit applicability determination shows that a requirement does not govern the work.

### As an organizational starting point

Organizations may adapt the policy to their own:

- Security requirements
- Privacy requirements
- Software-development lifecycle
- Repository controls
- Review and approval workflows
- Identity and attribution model
- Regulatory and contractual environment
- Tooling and execution architecture
- Records-management requirements
- AI governance requirements

Adaptations should preserve clear distinctions between mandatory controls, project requirements, defaults, recommendations, conditional requirements, and capabilities that cannot be technically enforced.

## Status

Version `0.3.0` is the current policy revision.

The policy is maintained as a living document. Changes that introduce substantive normative requirements or fully drafted policy sections are treated as MINOR-version changes. Structural or taxonomy changes are treated as MAJOR-version changes. Wording, clarity, consistency, and editorial corrections are treated as PATCH-version changes.

See `CHANGELOG.md` for the revision history.

## Limitations

This policy is a governance artifact, not a technical enforcement mechanism by itself.

A policy statement does not create a capability that the execution environment does not provide. Effective enforcement may depend on repository permissions, identity configuration, branch protection, available tooling, network controls, platform behavior, organizational authorities, and other external dependencies.

The policy therefore requires explicit distinction among:

- What the policy requires
- What the agent can technically enforce
- What the agent actually verified
- What depends on an administrator, organization, platform, authority, or other external actor

No provision should be interpreted as a guarantee of vulnerability-free software, complete prevention of future failures, unrestricted environmental visibility, legal compliance, classification status, export authorization, or control over third-party systems.

## Disclaimer

This is an independent project. It does not represent the official policy, position, or endorsement of any employer, client, contractor, government agency, or other organization unless explicitly adopted or incorporated by that organization.

This repository does not constitute legal, regulatory, classification, export-control, cybersecurity authorization, or compliance advice. Organizations should obtain appropriate legal, security, privacy, compliance, contracting, export-control, classification, and other authoritative determinations before adopting the policy for operational use.

## License

Licensed under [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/). See [LICENSE.txt](./LICENSE.txt).

You may share and adapt this work, including commercially, subject to the terms of the license and its attribution and ShareAlike requirements.

## Author

[Don Tran](mailto:don.tran@mail.traners.co?subject=Coding%20Agent%20Governance%20Policy%20Framework) — Senior Cloud Architect, DSO Engineer

## Contributing

Issues and pull requests proposing substantive policy improvements, corrections, applicability clarifications, standards updates, or structural improvements are welcome.

Contributions should:

- Identify the policy requirement or structural issue being addressed.
- Preserve consistency with the policy's precedence and applicability model.
- Avoid introducing duplicate requirements where an existing requirement or cross-reference is sufficient.
- Distinguish mandatory requirements from recommendations and environment-dependent behavior.
- Avoid claims that depend on capabilities the policy or execution environment cannot establish.
- Update `CHANGELOG.md` when a change warrants a documented release entry.
