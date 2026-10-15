---
title: "Constraint: Coding Standards"
owner: Engineering
status: Draft
last_updated: 2026-10-15
---

# Constraint: Coding Standards

> Constraints are **immutable during execution**. AI never violates them. Changing one requires an ADR + human approval (L0).

## Universal outcomes
- Preserve the repository's language, framework and architecture unless a change is explicitly justified and approved.
- Use strong typing where the language supports it; justify untyped escape hatches.
- Validate untrusted inputs at system boundaries with the tools appropriate to the adopted language and platform.
- Keep responsibilities explicit, state transitions understandable and public contracts small.
- Prefer native platform capabilities before adding dependencies; check maintenance and licence compatibility.
- Technology-specific defaults belong in an explicitly adopted project profile. See `profiles/web-typescript.md`.

## Structure
- Keep translatable UI content separate from application logic; follow the project's localisation conventions.
- Errors follow the project's documented taxonomy in `docs/engineering/ERROR_HANDLING.md`; expose useful user-facing errors without leaking sensitive details.
- Idempotent scripts; versioned config; small pure functions over clever abstractions.

## Verification
- Run the repository's relevant build, type, lint and behavioural checks. State what ran and what remains unverified. Do not assume ESLint or a particular toolchain exists.

## Template adoption
This is a project-policy template derived from Polaris, not a second constitutional canon. Record the adopting project's context and explicit approval before changing its hard constraints. Essential validation, access-control, privacy and accessibility outcomes apply to engineering work independently of full Polaris governance.
