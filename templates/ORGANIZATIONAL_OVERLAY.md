# Organizational Overlay to the AI Coding Assistant Policy

> **Template notice.** This file is a template governed by Section 18.3 of `CODING_AGENT_POLICY.md`. To use it, copy it to `ORGANIZATIONAL_OVERLAY.md` at the repository root (or to a user- or organization-scoped instruction location supported by your tools), replace every `<placeholder>`, delete sections that do not apply, and remove this notice. An agent shall not apply this template as an overlay.

## 1. Identification

| Field | Value |
|---|---|
| Organization | `<organization legal or common name>` |
| Overlay version | `<semantic version>` |
| Effective date | `<ISO 8601 date>` |
| Policy version overlaid | `<CODING_AGENT_POLICY.md version>` |
| Owning role | `<role responsible for this overlay, not a personal name>` |
| Contact | `<team mailbox or ticket queue>` |

## 2. Scope

This overlay applies to: `<repositories, programs, systems, or business units covered>`.

This overlay does not apply to: `<explicit exclusions, if any>`.

## 3. Precedence Statement

This overlay supplements `CODING_AGENT_POLICY.md`. It adds requirements and may make DEFAULT or RECOMMENDED practices mandatory for the organization. It does not relax any requirement that the policy or applicable law makes mandatory. Conflicts are resolved under Section XVII of the policy. Each requirement below carries a classification from Section 18.2 and, where MANDATORY, its governing authority.

## 4. Identity and Attribution

| Item | Value | Classification |
|---|---|---|
| User Service Principal Identity | `<service or bot identity used for technical authorship>` | MANDATORY |
| Commit signing | `<required / not required; key management reference>` | `<classification>` |
| Copyright and license notice text | `<exact notice, or "per project">` | `<classification>` |

## 5. Governing Requirements

Record only regimes whose applicability has been determined by the authorized organizational or governmental authority. Do not infer applicability from customer identity or terminology (policy Section 4.1).

| Regime | Applies | Determined by | Reference |
|---|---|---|---|
| Controlled Unclassified Information (CUI) | `<Yes / No / Conditional>` | `<authority>` | `<contract clause, program instruction, or marking guide>` |
| Classified information | `<Yes / No>` | `<authority>` | `<Security Classification Guide reference>` |
| International Traffic in Arms Regulations (ITAR) | `<Yes / No / Conditional>` | `<authority>` | `<jurisdiction determination or agreement>` |
| Export Administration Regulations (EAR) | `<Yes / No / Conditional>` | `<authority>` | `<ECCN determination>` |
| Privacy (for example PII, PHI, GDPR) | `<Yes / No / Conditional>` | `<authority>` | `<policy or assessment>` |
| Cloud authorization boundary and impact level | `<Yes / No>` | `<authority>` | `<ATO, impact level, or Security Requirements Guide reference>` |
| Contractual security clauses | `<Yes / No>` | `<authority>` | `<clause identifiers>` |

## 6. Information Handling and Disclosure

| Item | Value | Classification |
|---|---|---|
| Approved external services and connectors | `<list, or "none">` | MANDATORY |
| Prohibited destinations | `<list>` | MANDATORY |
| Retention rules for agent-generated records | `<rule and authority>` | `<classification>` |
| Data residency constraints | `<regions or boundaries>` | `<classification>` |

## 7. Secrets and Credentials

| Item | Value | Classification |
|---|---|---|
| Approved secret stores | `<for example AWS Secrets Manager, Azure Key Vault, HashiCorp Vault>` | MANDATORY |
| Required secret-scanning tooling | `<tool names>` | `<classification>` |
| Placeholder convention for examples | `<pattern, or "per policy Section III">` | DEFAULT |

## 8. Style Authorities and Tooling

Overrides or additions to the policy's Section XI table. Omit rows where the policy default stands.

| Language / Technology | Style Authority | Validation tooling | Classification |
|---|---|---|---|
| `<language>` | `<standard>` | `<tools>` | `<classification>` |

## 9. Reporting Conventions

| Item | Value | Classification |
|---|---|---|
| Formal report voice | `<for example first-person plural on behalf of the team>` | `<classification>` |
| Session Activity Journal placement | `<per policy Section XV, or organization-specific>` | `<classification>` |
| Metrics required in formal reports | `<cost, schedule, scale, velocity categories, or "as available">` | `<classification>` |

## 10. Additional Requirements

List each additional requirement as one entry. State the requirement, its classification, and, for MANDATORY entries, the governing authority.

1. `<Requirement statement.>` Classification: `<MANDATORY / PROJECT / DEFAULT / RECOMMENDED / CONDITIONAL>`. Authority: `<authority or "organizational policy">`.
2. `<Requirement statement.>` Classification: `<classification>`. Authority: `<authority>`.

## 11. Change Control

Changes to this overlay follow `<change-control process reference>`. Record each revision below.

| Version | Date | Summary |
|---|---|---|
| `<version>` | `<ISO 8601 date>` | `<summary>` |
