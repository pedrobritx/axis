---
title: "Constraint: Performance"
owner: Engineering
status: Draft
last_updated: 2026-10-15
---

# Constraint: Performance

> Constraints are **immutable during execution**. AI never violates them. Changing one requires an ADR + human approval (Level 0).

## Non-negotiables
- Set measurable budgets for the project's actual platform, user tasks and representative hardware.
- The historical web/API defaults are retained in `profiles/web-typescript.md`; adopting another platform does not import web-only metrics.
- No unbounded client-side lists — paginate or virtualize
- Record applicable runtime, payload, memory and response budgets in `docs/engineering/PERFORMANCE.md`.

## Verification
Record the tested workload, device/environment, measurements and limits. Budget declarations are not evidence of measured performance.

## Template adoption
This is a project-policy template derived from Polaris, not a second constitutional canon. Record the adopting project's context and explicit approval before changing its hard constraints. Essential validation, access-control, privacy and accessibility outcomes apply to engineering work independently of full Polaris governance.
