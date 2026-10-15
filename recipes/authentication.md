---
title: "Recipe: Authentication"
owner: Engineering
status: Active
last_updated: 2026-10-15
---

# Recipe: Authentication

This recipe applies only to an explicitly adopted Supabase/TypeScript web profile and approved identity model. It does not mandate Supabase for other projects or authorise external configuration. Policy rationale lives in `decisions/decision-engine/authentication.md`; record material departures from an adopted identity model through review.

## Before implementing — answer these (Question Engine)
- [ ] Social login? Which providers?
- [ ] MFA required, optional, or none?
- [ ] Passwordless (magic link / passkeys)?
- [ ] Session lifetime and refresh policy?
- [ ] Account recovery flow?
- [ ] Roles/permissions model (RBAC granularity)?
- [ ] B2B needs (orgs, invites, SSO later)?

Unanswered items → escalate at L2 before writing code.

## Default stack
Within that adopted profile, **Supabase Auth** with email+password and OAuth providers as decided above. Sessions via Supabase SSR helpers; middleware-protected routes.

## Implementation steps
1. Confirm explicit L0 approval for provider choice and external configuration before enabling a provider. Record approved configuration in `docs/engineering/AUTH.md`; this recipe alone grants no external write authority.
2. Env vars added to `docs/engineering/ENVIRONMENT.md` (never values, only purpose).
3. Server-side client + middleware session refresh (SSR helpers).
4. Route protection: everything private by default; public routes are an explicit allow-list (`constraints/security.md`).
5. RBAC: `roles` in DB, enforced by **RLS policies** — never client-side only.
6. UI: login/register/recover screens from `docs/design/SCREENS.md`, all states, localized strings.
7. In this adopted TypeScript profile, Zod-validate every auth-related input at the boundary. Other platforms use their approved validation mechanism.
8. Recovery flow tested end-to-end, including expired-token path.
9. If analytics is explicitly justified and approved, document minimal auth events in `docs/engineering/OBSERVABILITY.md`. Tests and operational evidence may be sufficient; do not collect authentication telemetry solely to satisfy this recipe.

## Security notes
- Required session/JWT security properties belong to `docs/engineering/SECURITY.md`; actual application values belong to `docs/engineering/AUTH.md`. Root `SECURITY.md` owns reporting, not runtime settings.
- Auth posture changes are always **L0**.
- Never log tokens, emails in plaintext beyond need, or recovery links.

## Definition of Done additions
- [ ] RLS verified with tests (authorized AND unauthorized paths)
- [ ] Recovery + logout + session-expiry paths tested
- [ ] docs/engineering/AUTH.md updated in the same PR
