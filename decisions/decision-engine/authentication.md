---
title: "Decision: Authentication"
owner: Engineering
status: Active
last_updated: 2026-10-15
---

# Decision Policy: Authentication

## Scope and prerequisites
This is a provider-selection recommendation for an explicitly adopted Supabase web profile, not evidence that any project has adopted it. Confirm identity needs, data isolation, recovery, cost and external configuration. Provider adoption and auth/security posture require explicit L0 approval; no complete policy overrides those gates.

## Default
**Supabase Auth** is a recommendation only for an adopted Supabase web profile. Confirm the project context; do not infer that Supabase is already installed or that cost and identity requirements are satisfied.

## Use Clerk instead only if
- Complex B2B org management (orgs, invitations, per-org roles) is a day-one requirement, or
- Enterprise SSO (SAML/OIDC) is on the near-term roadmap.

## Avoid
- **Firebase Auth** — locks into a parallel ecosystem we don't use; weaker Postgres/RLS story.
- **Hand-rolled auth** — never. Security constraint.

## Rationale
See `recipes/authentication.md` for the how. First ADR applying this policy should be filed as `decisions/adr/00X-auth-provider.md` per project.

## Review trigger
Revisit when the identity model, provider, risk profile, recovery requirements or platform changes, or when evidence shows the recommendation no longer fits. Do not switch providers automatically.

## Delegation level
**Level 0** for provider adoption, external provider configuration and any auth/security posture change. Reversible implementation inside an already approved identity model may proceed within its authorised scope, with access-control and recovery tests. This policy never authorises dashboard changes, spend or deployment by itself.
