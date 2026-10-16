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

No repository is deployed or provisioned by these commands. This relocation selects no general redistribution licence; the existing licensing template remains unresolved. Review the coordinated migration before merging Polaris's removal branch.
