# Repository Instructions

## HACS release workflow

When a change modifies the shipped integration under `custom_components/solem_toolkit/`, always do the following before pushing:

1. Bump `custom_components/solem_toolkit/manifest.json`.
2. Add a matching entry to `CHANGELOG.md`.
3. Add or update `release-notes/<version>.md` for the GitHub Release body.
4. Run `python -m compileall custom_components/solem_toolkit`.
5. Check for unresolved merge markers with `rg -n "^(<<<<<<<|=======|>>>>>>>)" custom_components/solem_toolkit`.
6. Push the verified branch to `origin/main`.

If a change is docs-only or repo-only and does not alter the shipped integration files, do not bump the integration version just for that.

## Packaging hygiene

- Do not commit `__pycache__` directories or `.pyc` files.
- Do not publish a release if the integration fails to import or compile.
