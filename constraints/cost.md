---
title: "Constraint: Cost"
owner: CEO
status: Draft
last_updated: 2026-10-15
---

# Constraint: Cost

> Prevents AI from suggesting overengineered solutions. Immutable during execution.

## Non-negotiables
- **Any new recurring cost is L0.** No exceptions, no trials that auto-convert.
- Prefer free tiers and services already in the stack before adding vendors.

## Infrastructure and vendor decisions
- New recurring spend, paid trials and per-seat services require explicit L0 approval.
- Introduce infrastructure only with a concrete need, maintenance/exit costs and rollback plan.
- Reuse services actually present and suitable in the project; do not assume a vendor is installed.
- Historical vendor preferences and infrastructure avoid-list are retained in `profiles/web-typescript.md`. Adopting that profile does not approve spend or provisioning.

## Verification
- PR reviewer checks new dependencies/services against this list.
- `STATUS.md` risk section flags any cost-bearing proposal awaiting L0.

## Template adoption
This is a project-policy template derived from Polaris, not a second constitutional canon. Record the adopting project's context and explicit approval before changing its hard constraints. Essential validation, access-control, privacy and accessibility outcomes apply to engineering work independently of full Polaris governance.
