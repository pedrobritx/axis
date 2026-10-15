---
title: "Constraint: Privacy"
owner: Business
status: Draft
last_updated: 2026-07-01
---

# Constraint: Privacy

> Constraints are **immutable during execution**. AI never violates them. Changing one requires an ADR + human approval (Level 0).

## Non-negotiables
- Collect the minimum data necessary
- PII flagged in DATA_DICTIONARY and encrypted at rest
- GDPR + LGPD compliant by default (Brazilian market)
- No third-party trackers without explicit approval
- User deletion must be real deletion (or documented anonymization)

## Verification
> _How compliance is checked (automated where possible)._

## Template adoption
This is a project-policy template derived from Polaris, not a second constitutional canon. Record the adopting project's context and explicit approval before changing its hard constraints. Essential validation, access-control, privacy and accessibility outcomes apply to engineering work independently of full Polaris governance.
