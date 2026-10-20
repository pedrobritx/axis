---
title: Definition of Done
owner: QA Engineer
status: Active
last_updated: 2026-10-20
---

# DONE — Definition of Done

Nothing is complete until every **applicable** item passes. "Not applicable" must be stated explicitly in the PR, not assumed silently.

## Checklist

### Product
- [ ] Meets acceptance criteria in the feature spec / user story
- [ ] `docs/product/` updated if behavior or scope changed

### Architecture
- [ ] Consistent with `docs/engineering/ARCHITECTURE.md`; deviations recorded as ADR
- [ ] No new dependency without Decision Engine check + license check

### Quality
- [ ] Applicable local checks pass before remote/shared publication per [Evidence-Based Engineering](guides/evidence-based-engineering.md); environment and any scoped exceptions recorded
- [ ] Behaviour tests added/updated and passing where behaviour changed; justify inapplicable checks
- [ ] Integration tests for cross-system behavior
- [ ] Error, loading, and empty states implemented and tested
- [ ] Manual smoke test performed

### Non-functional
- [ ] Accessibility verified against `constraints/accessibility.md`
- [ ] Localization: no hardcoded user-facing strings
- [ ] Performance within budgets (`constraints/performance.md`)
- [ ] Security review for auth/input/secrets surface (`constraints/security.md`)

### Instrumentation
- [ ] Evidence of the intended outcome recorded. Analytics is optional and requires a justified purpose, minimal collection and explicit approval; follow `docs/engineering/OBSERVABILITY.md` if adopted.
- [ ] Relevant failures are diagnosable through the adopted logging/error-reporting mechanism with sensitive data redacted; no new tracker is required solely for this checklist

### Documentation
- [ ] Owning docs updated in the same PR
- [ ] `docs/oss/CHANGELOG.md` entry added
- [ ] New reusable pattern? → written back to `recipes/` or `memory/patterns.md`

### Continuity
- [ ] `STATUS.md` updated
- [ ] `HANDOFF.md` updated
