---
title: "Playbook: New Feature"
owner: Engineering
status: Active
last_updated: 2026-10-15
---

# Playbook: New Feature

Use this loop for the applicable parts of an approved feature. Scale documentation and evidence to risk; omit inapplicable steps with a short reason. Record durable significant decisions as ADRs rather than using an ADR for every routine variation.

## When to use
New user-facing capability or significant behavior change. (Small corrections → Bug Fix; structure-only → Refactor.)

## Phase 0 — Context (Product Manager role)
1. Read `docs/product/PRODUCT.md`, `docs/product/USER_STORIES.md`, `docs/product/ROADMAP.md`.
2. Write the spec from `templates/feature_spec.md`.
3. **Question Engine pass:** review the relevant recipes. Resolve or escalate questions that materially affect behaviour, architecture, data, security or UX; routine reversible details may be settled within the approved scope.
4. Confirm that the feature direction and scope have human authorisation. Existing explicit approval satisfies this step; ask only for missing or materially changed decisions.

## Phase 1 — Design (Designer + Architect roles)
5. Designer: UX flow + screen spec, all states, from Design System components. Update `docs/design/UX_FLOWS.md` / `docs/design/SCREENS.md`.
6. Architect: check applicable complete adopted policies for consequential technical choices; new significant decisions → ADR via `templates/adr.md`.
7. Data Engineer: schema delta per `templates/database_table.md` — migration and rollback drafted now, not later.

## Phase 2 — Build (Backend + Frontend roles)
8. Backend: endpoints per `templates/api_endpoint.md`; boundary validation appropriate to the adopted platform; error taxonomy from `docs/engineering/ERROR_HANDLING.md`.
9. Frontend: implement from the screen spec; tokens only; loading/empty/error states are part of the feature, not polish.
10. Both: check `memory/preferences.md` and `memory/patterns.md` before choosing any pattern.

## Phase 3 — Quality (QA role)
11. Run the task-relevant test set from the adopting project's testing strategy; broaden when changed behaviour or unresolved risk justifies it.
12. Accessibility + localization verification.
13. QA verdict against `DONE.md` — every item passed or explicitly N/A with justification.

## Phase 4 — Ship & Learn
14. Merge per `docs/engineering/WORKFLOWS.md`; release per the Release playbook if applicable.
15. `docs/oss/CHANGELOG.md` entry (*Added*).
16. New reusable pattern discovered? Write it back: `recipes/` (if a standard) or `memory/patterns.md` (if a technique).
17. Update `STATUS.md` + `HANDOFF.md` when state changed or unfinished work needs continuity.

## Validation
Acceptance criteria demonstrably met; applicable DONE.md checks pass; proportionate outcome evidence recorded. Verify analytics only if explicitly adopted and approved.

## Completion checklist
- [ ] Feature direction/scope authorised; material specification decisions resolved before dependent implementation
- [ ] Material Question Engine items resolved, explicitly deferred with an owner, or inapplicable
- [ ] ADRs filed for significant decisions
- [ ] DONE.md fully satisfied
- [ ] Learning written back (recipe/pattern/lesson)
- [ ] Continuity records updated when state changed or unfinished work needs handoff
