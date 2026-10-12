# 0001 — Repository naming by role

## Status
Accepted (2026-10-12). The naming of tools is superseded by [ADR 0005](0005-tools-prefix.md). The site rule is amended by [ADR 0006](0006-website-prefix.md).

## Context
The org grew from one benchmark (static site generators) to several families. Names like `ssg-frameworks` did not say what role a repo plays, and new repos (algorithms, web frameworks, datasets) needed a convention.

## Decision
Name repos by role:
- `catalog-*`: implementations that are measured. Current repos: catalog-algorithms, catalog-ssg, catalog-web-frameworks.
- `dataset-*`: inputs for the benchmarks. Current repos: dataset-names, dataset-commons.
- Tools have plain names: perfratio, benchmark-tool, dataset-tool.
- Sites use plain names or `<tool>-website`: website, perfratio-website.
- Dot repos (`.github`, `.github-private`, `.product`) hold org governance; see ADR 0002.

Renames made: `ssg-frameworks` → `catalog-ssg`; `matbrgz/Hello-World` → `catalog-algorithms`; `OpenSoftwareAlliance/names-commons-dataset` → `dataset-names`.

## Consequences
- A repo's role is clear from its name, and topics mirror the categories.
- Old URLs keep working through GitHub redirects, but submodules, docs and links must be updated (tracked in each repo's issues).
