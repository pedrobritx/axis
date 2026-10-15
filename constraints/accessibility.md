---
title: "Constraint: Accessibility"
owner: Design
status: Draft
last_updated: 2026-07-01
---

# Constraint: Accessibility

> Constraints are **immutable during execution**. AI never violates them. Changing one requires an ADR + human approval (Level 0).

## Non-negotiables
- WCAG 2.2 AA minimum
- Full keyboard operability
- Contrast ratios enforced from DESIGN_SYSTEM tokens
- Every interactive element has an accessible name
- Never rely on color alone to convey state

## Verification
> _How compliance is checked (automated where possible)._

## Template adoption
This is a project-policy template derived from Polaris, not a second constitutional canon. Record the adopting project's context and explicit approval before changing its hard constraints. Essential validation, access-control, privacy and accessibility outcomes apply to engineering work independently of full Polaris governance.
