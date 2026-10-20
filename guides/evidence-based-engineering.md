---
title: Evidence-Based Engineering
owner: Engineering
status: Active
last_updated: 2026-10-20
---

# Evidence-Based Engineering

Use evidence to make a useful change safe enough for its context. This is Axis's reusable engineering policy; existing project commitments and explicit adoption control its application. It does not install Polaris governance, replace a stricter adopted requirement or grant publication authority. Read it with [operating rules](../PROJECT_RULES.md) and [completion criteria](../DONE.md).

## Frame a small, reversible change

Inspect actual source, conventions, decisions and unfinished work. State the intended user outcome, observable acceptance criteria, affected contracts and likely failure cost before implementation. A bug report, issue or short task note is sufficient for a small correction. Prefer focused increments that can be inspected, tested and reverted independently; preserve unrelated work. For data changes, distinguish code rollback from data recovery, rehearse applicable migrations with disposable data, and establish backup/restore or forward-repair evidence before an authorised irreversible operation.

Use an ADR for a consequential or costly-to-reverse choice, including context, alternatives, evidence, consequences and a review trigger. Reuse existing project records. Routine reversible choices need no new ADR, service, document catalogue or approval round.

## Verify locally before publishing

Run applicable checks and inspect the integrated result locally before pushing a branch, creating/updating a GitHub PR, saving changes to a shared Figma file, publishing a library, deploying or releasing. For design work, inspect a local preview/export when feasible before a shared-file write. State what the local preview cannot establish and obtain any required authority for subsequent shared verification. CI and remote previews supplement local evidence; they do not replace available local checks.

A local Git commit is a reversible checkpoint, not remote publication. Prefer relevant checks before committing; an explicitly labelled work-in-progress checkpoint may retain known failures without claiming readiness. Re-run affected checks on the final changes before push. Publishing a review branch/PR, merging, Figma library publication, deployment and release are distinct actions with distinct authority and evidence. A passing local check authorises none of them by itself.

When a required check cannot run locally, record the exact blocker, affected acceptance criteria, feasible substitute evidence and remaining risk. Complete available checks. If the missing check is a publication prerequisite, stop dependent publication until the owner explicitly authorises a bounded exception; never silently convert an unavailable check into a pass.

## Docker first, where it helps

For container-compatible applications and services, default to a versioned Docker development/test environment with reproducible setup and teardown. Reuse existing Dockerfiles, Compose configuration and scripts. Record the image/runtime version (and immutable image digest for durable evidence), dependency lockfiles, required tools and exact commands; use synthetic fixtures and safe example configuration. Prefer the same commands locally and in CI. A clean checkout should be enough to reproduce checks without undocumented global dependencies.

Native Apple builds, simulators, signing, entitlements, platform accessibility and native UI verification use macOS/Xcode and the applicable device/simulator. Containerise compatible supporting services where useful. Document the required Apple toolchain and destination; a Linux container cannot prove native behaviour.

Docker is a default, not an architectural mandate. For documentation-only changes, unsupported hardware/platforms or a repository whose established native workflow provides better fidelity, use the appropriate local tools and briefly record why. If Docker is unavailable, report that fact and the alternative's limits. Do not add container scaffolding, change frameworks/providers or simulate production parity solely to satisfy a rule. Container execution alone does not establish security, deployment or production equivalence.

## Scale checks to failure cost

Start with the narrowest meaningful checks, then broaden for affected contracts and unresolved risk. Preserve all required adopted checks. Add or update behaviour tests when behaviour changes and a test infrastructure exists; verify observable outcomes, not implementation trivia. Avoid arbitrary coverage percentages or tests solely to satisfy a count.

| Changed scope | Relevant evidence |
| --- | --- |
| Documentation/instructions | Metadata/link validation, instruction consistency and diff review; no invented application test |
| Behaviour or bug fix | Reproduction/regression evidence, targeted tests, applicable lint/types/build and user-path smoke checks |
| Cross-system or UI contract | Integration/contract checks; loading, empty, error, offline and permission states as applicable; keyboard/focus, accessibility and localisation evidence |
| Auth, permissions, private data or dependencies | Allowed/denied paths, boundary validation and least-privilege checks; Sentinel methods or equivalent accountable security review |
| Data, release or costly-to-reverse operation | Migration/recovery rehearsal, affected broader suite, rollback limits and independent review when warranted |

## Secure and observable by default

Validate untrusted inputs at boundaries; deny unauthorised access, preserve least privilege and secure defaults. Keep credentials out of source, images, fixtures, prompts and logs; use the project's approved secret mechanism. Review dependency necessity, provenance and risk. Never weaken authentication, RLS or another control to pass a check. Use Sentinel's security guidance when relevant, without making a sibling checkout mandatory.

Make failures diagnosable with proportionate structured errors/logs, health signals and recovery instructions. Exercise relevant failure paths locally. Redact sensitive data; limit collection and retention. Observability is not permission for analytics or a new monitoring provider; retain explicit purpose/approval requirements. Record performance claims against a reproducible baseline when performance is part of acceptance.

## CI and reporting

Run relevant repository checks on review changes and before merge/release, using reproducible dependencies and the intended supported environments. Required failures or unknown results block readiness. Review required checks and branch protections separately: a workflow file or policy is not proof that GitHub enforcement is enabled. Do not change repository protections or bypass gates without explicit authority.

Report the outcome, changed files/revision, checks actually run with environment/results, material gaps, residual risks and next owner/action. Distinguish local results, CI results, review, merge, deployment, runtime observation and human acceptance. Retest affected evidence after changes. A concise PR or existing handoff usually suffices; no duplicate evidence ledger is required. Plan/schema/document validation proves only its stated scope.
