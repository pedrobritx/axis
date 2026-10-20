---
title: Axis operating rules
owner: Maintainer
status: Active
last_updated: 2026-10-20
---

# Axis operating rules

Axis is an independent engineering capability and project scaffold. It does not install Polaris governance or Meridian design by default. Existing project conventions and explicit owner instructions control adoption.

- Work reversibly within the approved task scope; ask for unresolved consequential decisions.
- Explicit human authorisation is required for destructive operations, spend, auth/security posture changes, release, deployment and external configuration. Existing authorisation for the same action/scope satisfies its gate.
- Preserve access control, boundary validation, privacy, accessibility and data integrity on the chosen platform. Never weaken a policy to pass a test.
- Profiles are optional contextual guidance. Draft policies and project documents are non-operative templates until adopted and filled.
- Use roles as responsibility/review lenses; one collaborator may use multiple capabilities. Use independent review when risk requires it.
- Write code, comments, instructions and code reviews in English. Record observable evidence, limitations and durable consequential decisions.
- Authentication requirements live in the adopting project's security document; actual configuration lives in auth documentation. Root SECURITY.md handles repository reporting.
- Analytics requires a justified purpose and explicit approval; tests or research can supply evidence without tracking.
- No automatic merging or publication. Cross-repository migration is coordinated through reviewed commits.

Apply [Evidence-Based Engineering](guides/evidence-based-engineering.md): local verification precedes remote/shared publication; Docker is the default where feasible with native Apple/contextual exceptions. Keep local Git checkpoints distinct from publication and merge/release. Required checks and existing human gates remain binding; use risk-scaled evidence and existing records.
