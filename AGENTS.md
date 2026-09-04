# Agent Instructions

This repository publishes the AI Coding Assistant Policy, a normative governance policy for AI coding assistants. The policy text is `CODING_AGENT_POLICY.md`. This file tells a coding agent how to apply it. It adds no requirements of its own.

## Required Reading

Before performing any work in a repository that adopts this policy, read `CODING_AGENT_POLICY.md` in full and apply it. Do not rely on this file, or on any other tool-specific instruction file, in place of the policy.

## Precedence

When instructions conflict, apply them in this order and resolve residual conflicts using Section XVII of the policy:

1. Applicable law and valid legal orders.
2. Requirements the policy states as mandatory, together with any classification, Controlled Unclassified Information (CUI), export-control, privacy, contractual, or regulatory requirement identified as applicable under Section XVIII.
3. The adopting organization's overlay, if one is present.
4. Project-specific requirements and Style Authorities found in the repository. These govern over the policy's DEFAULT and RECOMMENDED practices but not over its mandatory requirements.
5. Tool-specific instruction files, including this one.

Classify every requirement you apply using Section 18.2 of the policy (MANDATORY, PROJECT, DEFAULT, RECOMMENDED, CONDITIONAL, UNVERIFIED). Do not promote a DEFAULT or RECOMMENDED practice to MANDATORY.

## Organizational Overlay

If the adopting organization has published an overlay, read and apply it after the policy. The default location is `ORGANIZATIONAL_OVERLAY.md` at the repository root; a project may name a different location in its own instruction files. Section 18.3 of the policy defines what an overlay may and may not do.

`templates/ORGANIZATIONAL_OVERLAY.md` is a template, not an overlay. Do not apply it.

## Working in This Repository

- This repository contains policy documents only. There are no build, test, or runtime steps.
- Every change to `CODING_AGENT_POLICY.md` requires a matching `CHANGELOG.md` entry and a version update in the policy's version line and in `README.md`, following the versioning rule stated in `README.md`.
- Do not introduce terms, actors, or acronyms that the policy does not define. Add new ones to the Definitions or Abbreviations tables.
- Do not add AI provenance markers, AI attribution, or AI co-author trailers to files or commits (policy Section 2.3).
- Do not merge, force-push, or finalize a change without human review (policy Section 9.4).
- Produce a Session Activity Journal for any turn that performs actions (policy Section XV).
