# Changelog

All notable changes to this project are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/). Versioning follows a documentation-adapted form of [Semantic Versioning](https://semver.org/): MAJOR for structural or taxonomy changes, MINOR for new substantive normative requirements or fully drafted sections, and PATCH for wording, clarity, consistency, or editorial corrections.

## [Unreleased]

### Planned

- No planned changes currently recorded.

## [0.3.0] - 2026-09-04

### Added

- Section 18.3, Organizational Overlays: defines how an adopting organization layers its own requirements on the policy, what an overlay may add or tighten, what it may not relax, and where it sits in the Section 17.1 precedence order. States that tool-specific instruction files are adapters with no independent normative weight.
- `templates/ORGANIZATIONAL_OVERLAY.md`: fill-in template for an organizational overlay covering identity and attribution, governing regimes, information handling, secrets, Style Authorities, reporting conventions, and additional classified requirements.
- `AGENTS.md`: cross-vendor adapter stating required reading, precedence, overlay location, and repository working rules.
- `CLAUDE.md` and `GEMINI.md`: import-based adapters that load `AGENTS.md` and the full policy at session start.
- `.github/copilot-instructions.md` and `.cursor/rules/coding-agent-policy.mdc`: pointer adapters for GitHub Copilot and Cursor.
- README sections "With coding-agent tools" and "With an organizational overlay", including a tool-to-file table verified against vendor documentation on 2026-09-04.

### Changed

- Section XVIII split into 18.1 Resolution Procedure, 18.2 Requirement Classification, and 18.3 Organizational Overlays. Existing content is unchanged.
- README repository tree and policy-scope list updated for the new files.

## [0.2.1] - 2026-09-04

### Added

- Version line beneath the policy title so the artifact identifies its own revision.
- Abbreviations table in the policy front matter defining the regulatory and domain acronyms used throughout (ATO, BIS, CUI, DDTC, EAR, ECCN, ITAR, USML, and others), satisfying the policy's own acronym-definition requirement.
- Definitions for the normative actors "System" and "User", which were used throughout the policy but never defined.

### Changed

- Demoted all section and subsection headings by one level so the policy has a single top-level heading.
- Enclosed the Session Activity Journal template and the no-activity sentence in HTML code blocks so the template's headings no longer appear in the document outline and the literal text is unambiguous.
- Replaced the undefined "10 steps ahead" phrase in Proactive Engineering Posture with a self-contained statement.
- Changelog release links now point at this repository instead of the OWNER/REPOSITORY placeholder.

### Fixed

- Session Activity Journal cross-references in the Definitions table and in Incidental Non-Compliance Discovery & Remediation pointed at Section XVI (Formal Reports) instead of Section XV.
- Interpretation and Authority referenced "Section 17" using Arabic numbering and an ampersand; it now matches the Section XVII heading.
- Double-encoded UTF-8 characters (em dashes in the journal template, curly quotes in this changelog, and the em dash in the README author line).
- README repository tree listed `LICENSE` and a truncated word; the file is `LICENSE.txt`, and the README license link now resolves.
- "bona-fide" corrected to "bona fide".
- Blank lines added after changelog headings and before lists for Markdown lint compliance.

## [0.2.0] - 2026-08-26

### Added

- Incidental Non-Compliance Discovery & Remediation requirements under Universal Code Documentation, Hygiene & Traceability, including:
  - Detection and reporting of documentation and quality-policy drift encountered during any authorized work.
  - Dedicated, scoped remediation PRs where branch/PR capability exists.
  - Maintainer/CODEOWNERS tagging using available repository mechanisms.
  - Human review requirement before merge or finalization.
  - Scoped findings inventory and phased remediation when discovered non-compliance is too broad for a single PR.
- Efficiency, Performance & Complexity Awareness requirements, including:
  - Appropriate time/space complexity consideration.
  - Preference for materially more efficient standard techniques where justified.
  - Big-O or equivalent complexity awareness for non-trivial functions.
  - Documentation of non-obvious complexity and intentional efficiency trade-offs.
  - Increased scrutiny for performance-critical paths.
- Standards-First Construction requirements under Core Operating Principles, including preference for:
  - Established tools, libraries, packages, modules, frameworks, language and standard-library facilities.
  - Existing project and ecosystem conventions.
  - Established design patterns and accepted engineering practices.
  - Explicit justification before replacing established functionality with custom implementations.
- Constructive Skepticism at Critical Decision Boundaries requirements under Decision & Response Model, including:
  - Proactive identification of material technical assumptions and risks.
  - Specific pushback at decisions involving significant irreversibility, security exposure, technical debt, scalability, or rework risk.
  - Consideration of viable alternatives and trade-offs.
  - Reassessment of prior agent recommendations when new information changes the engineering basis.
  - Recording of acknowledged risks and user-directed decisions in the Session Activity Journal.

### Changed

- Consolidated proactive engineering posture so prevention, standards-first construction, and critical-decision skepticism are defined as engineering behaviors rather than duplicated across documentation or language-specific requirements.
- Clarified that incidental policy non-compliance is reported and remediated through scoped work rather than silently corrected as an unrelated side effect.
- Clarified that performance optimization is balanced against readability and maintainability rather than treated as an unconditional objective.
- Clarified that established standards and existing repository conventions take precedence over novel parallel constructs unless an explicit technical reason supports deviation.
- Clarified that constructive skepticism informs user decisions but does not override an informed user decision below applicable safety, security, legal, or policy boundaries.
- Consolidated validation and non-fabrication requirements to distinguish actual tool execution and observed results from intended or assumed outcomes.
- Reduced redundant statements describing generic AI-agent behaviors where those behaviors are already established by the policy's operational, validation, applicability, or conflict-resolution requirements.
- Removed or consolidated duplicate language and repeated requirements identified during structural and literal duplication review.
- Tightened terminology and cross-references among Core Operating Principles, Universal Code Documentation, Language and Tooling Standards, Decision & Response Model, and Session Activity Journal.
- Converted literal examples that would otherwise terminate the enclosing Markdown code block into HTML code blocks for safe inclusion within the policy source representation.

### Fixed

- Duplicate DevSecOps Playbook statement in the Domain Expertise & Operational Baseline section.
- Duplicate export-control section numbering.
- Redundant export-control requirements and repeated jurisdiction/authorization cautions where equivalent requirements could be consolidated.
- Repeated non-fabrication and verification language where a single authoritative requirement and cross-reference is sufficient.
- Inconsistent use of “System,” “agent,” and “AI coding assistant” where the surrounding policy establishes the System as the normative actor.
- Overly absolute or aspirational wording that could imply capabilities the System cannot guarantee, including predictive certainty, universal prevention, or unrestricted environmental verification.
- Structural ambiguity between policy requirements, project requirements, defaults, recommendations, conditional requirements, and unverifiable states.
- Changelog taxonomy mismatch with the current policy structure.

## [0.1.0] - 2026-08-25

### Added

- Initial AI Coding Assistant Policy structure and normative operating requirements.
- Data confidentiality, privacy, non-provenance, and organizational attribution requirements.
- Cybersecurity hygiene and secret-sanitization requirements.
- Classification, CUI, information-protection, and export-control boundaries.
- Domain expertise and operational engineering baseline.
- Communication, prose, formatting, and ambiguity standards.
- Formal report generation and quantitative-impact requirements.
- Universal code documentation, hygiene, and traceability requirements.
- Language-specific coding standards and validation tooling.
- File headers, purpose-driven documentation, and repository documentation requirements.
- Merge-readiness standards.
- Operational integrity and non-fabrication requirements.
- Session Activity Journal (STAR) requirements, including CRUD action tagging, failure reporting, metrics, and journal-protection requirements.
- Policy priority, conflict-resolution, applicability, authority-resolution, and environment-dependent enforcement requirements.
- Decision and response model.
- Final operating standard.

[Unreleased]: https://github.com/zedtran/Agentic-AI-Policy-Framework/compare/v0.3.0...HEAD
[0.3.0]: https://github.com/zedtran/Agentic-AI-Policy-Framework/releases/tag/v0.3.0
[0.2.1]: https://github.com/zedtran/Agentic-AI-Policy-Framework/compare/v0.2.0...v0.2.1
[0.2.0]: https://github.com/zedtran/Agentic-AI-Policy-Framework/releases/tag/v0.2.0
[0.1.0]: https://github.com/zedtran/Agentic-AI-Policy-Framework/releases/tag/v0.1.0
