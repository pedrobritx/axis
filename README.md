# Axis

Architecture and engineering capabilities extracted from the original Polaris engineering scaffold. Axis contains engineering roles, recipes, playbooks, optional stack profiles and project-document/specification templates. It works independently of Polaris, Meridian and Sentinel; optional integration is by reviewed references, never runtime imports.

## Start
Read [AGENTS.md](AGENTS.md), [operating rules](PROJECT_RULES.md) and [the project template index](docs/README.md). Draft project documents are slots for an adopting project, not claims about Axis's own implementation. Adopt only the templates relevant to the task and resolve material questions before implementing.

- [Engineering roles](agents/README.md)
- [Decision policies](decisions/README.md): Draft placeholders grant no authority.
- [Optional web profile](profiles/web-typescript.md): existing repository technology remains authoritative.
- [Provenance](migration/provenance.json) records the original Polaris snapshot and every relocated file.

## Verification

```sh
python3 automation/validate_docs.py
python3 -m unittest discover -s tests -v
```

These commands validate Axis documentation/tooling. Select only relevant adopter templates; the licensing template remains unresolved. See [optional tracking patterns](guides/project-tracking.md) for project workflow examples.

## Optional Constellation composition

Polaris is the usual coordinating entry point; [the composition contract](https://github.com/pedrobritx/polaris/blob/main/integration/README.md) defines explicit adoption, task scope and evidence returns. [discipline.json](discipline.json) describes this capability without installing a runtime dependency. Start directly at this repository’s AGENTS.md for standalone work.

When receiving a handoff, inspect the actual adopting project and retain its request ID, acceptance criteria, constraints and reviewed source revision. Return project artifacts, checks actually run, limitations, interface changes and blockers. Product-specific implementation/findings belong in the product repository; reusable capability improvements belong here. Excluded disciplines are explicit choices and never imply that their quality or safety checks passed.
