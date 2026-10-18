---
title: Documentation Index
owner: Technical Writer
status: Active
last_updated: 2026-10-16
---

# Documentation Index

This is a catalogue of optional adopter templates, not a description of Axis's own implemented product. Every adopted document owns **one subject**; everything else links to it.

## Adopt the minimum

Start with actual product intent/acceptance criteria, the affected architecture or interface, and a continuity record. Keep existing repository names and formats. Select other templates when the work needs them; do not copy every empty document, policy, recipe or business page into a new product. A Draft remains unanswered until the adopter supplies context and approves it.

The generic design slots record whichever design system the product selects; Meridian's reusable tokens/components stay in Meridian. Security slots record the product's actual requirements and evidence; Sentinel supplies optional review methods. Completed Constellation product records belong in the Constellation repository. [Tracking patterns](../guides/project-tracking.md) are optional.

## Product — *why and what*
- [Vision](product/VISION.md) — why the product exists
- [Product](product/PRODUCT.md) — what it does: goals, audience, requirements, KPIs
- [Roadmap](product/ROADMAP.md) — milestone sequence
- [User Stories](product/USER_STORIES.md) — user needs
- [Billing](product/BILLING.md) — plans and pricing rules

## Design — *how it looks and feels*
- [Branding](design/BRANDING.md) · [Design System](design/DESIGN_SYSTEM.md) · [Icon Guidelines](design/ICON_GUIDELINES.md)
- [UX Flows](design/UX_FLOWS.md) · [Screen Library](design/SCREENS.md)
- [Accessibility](design/ACCESSIBILITY.md) · [Localization](design/LOCALIZATION.md)

## Engineering — *how it is built*
Hub: [Architecture](engineering/ARCHITECTURE.md)
- Contracts: [API](engineering/API.md) · [Auth](engineering/AUTH.md) · [Error Handling](engineering/ERROR_HANDLING.md)
- Data: [Schema](engineering/SCHEMA.md) · [Data Dictionary](engineering/DATA_DICTIONARY.md) · [Seed Data](engineering/SEED_DATA.md) · [Migration Guide](engineering/MIGRATION_GUIDE.md)
- Ops: [DevOps](engineering/DEVOPS.md) · [Workflows](engineering/WORKFLOWS.md) · [Release](engineering/RELEASE.md) · [Environment](engineering/ENVIRONMENT.md) · [Setup](engineering/SETUP.md)
- Quality: [Testing](engineering/TESTING.md) · [Performance](engineering/PERFORMANCE.md) · [Security](engineering/SECURITY.md) · [Observability](engineering/OBSERVABILITY.md)

## Business
- [Terms](business/TERMS.md) · [Privacy](business/PRIVACY.md) · [Trademark Policy](business/TRADEMARK_POLICY.md)
- [Incident Response](business/INCIDENT_RESPONSE.md) · [Licensing](business/LICENSING.md)

## Open Source
- [Changelog](oss/CHANGELOG.md) · [Contributing](oss/CONTRIBUTING.md) · [Code of Conduct](oss/CODE_OF_CONDUCT.md) · [CLA](oss/CLA.md)

---

## Ownership table

| Document | Owns |
|---|---|
| VISION | Why the product exists |
| PRODUCT | What the product does |
| USER_STORIES | User needs |
| UX_FLOWS | User journeys |
| DESIGN_SYSTEM | UI rules |
| BRANDING | Visual identity |
| ARCHITECTURE | System structure (hub — links, doesn't explain) |
| API | Endpoints and contracts |
| SCHEMA | Database structure |
| DATA_DICTIONARY | Meaning of data |
| AUTH | Authentication and authorization |
| SECURITY | Security policies |
| DEVOPS | Infrastructure |
| WORKFLOWS | Git + CI/CD |
| TESTING | Testing strategy |
| ERROR_HANDLING | Error taxonomy |

If another document needs information from one of these areas, it **links** to the owner. It never duplicates.
