---
title: "Template: Universal Document Layout"
owner: Technical Writer
status: Active
last_updated: 2026-10-15
---

# Universal Document Layout

Use this structure when it helps readers locate ownership, scope and decisions. Short references, native GitHub templates and historical records may use a smaller or native form; preserve clear ownership and provenance.

## The template

```markdown
---
title: <Title>
owner: <Product|Design|Engineering|Business|All>
status: <Draft|Active|Deprecated>
last_updated: YYYY-MM-DD
depends_on: [DOC_A, DOC_B]
related: [DOC_C, DOC_D]
---

# <TITLE>

## Purpose
One sentence describing what this document owns.

---

## Scope
**Belongs here:** …
**Does NOT belong here:** … (name the owning document)

---

## Related Documents
### Depends on
- `DOC_A.md` — why
### Referenced by
- `DOC_C.md` — why

---

## Contents
The actual material. Reference, don't duplicate:
> Actual session configuration is defined in `docs/engineering/AUTH.md`; required security properties are defined in `docs/engineering/SECURITY.md`.

---

## Decisions
Links to ADRs that shaped this document. Never restate an ADR.

---

## Open Questions
- [ ] Unresolved items, each with an owner.
```

## Rules
1. Front matter is required for documents covered by `automation/validate_docs.py`; root README and `.github` files are exempt. The validator checks required fields and relative Markdown file targets, not YAML semantics or dependency resolution.
2. `depends_on` = documents you must read to understand this one. `related` = documents that reference this one.
3. A document with more than one Purpose sentence probably owns too much — split it.
4. `status: Deprecated` documents keep their history and point to their successor.
