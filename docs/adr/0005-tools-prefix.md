# 0005 — Tools use the `tools-*` prefix

## Status
Accepted (2026-10-12). Supersedes the tools rule in [ADR 0001](0001-repository-naming.md).

## Context
ADR 0001 gave tools plain names (`benchmark-tool`, `dataset-tool`), while catalogs and datasets have role prefixes. A shared library for the tools also needed a home.

## Decision
- Tools use the `tools-*` prefix, like `catalog-*` and `dataset-*`:
  - `benchmark-tool` was renamed to `tools-benchmark`;
  - `dataset-tool` was renamed to `tools-dataset`;
  - `tools-commons` is new and holds the shared libraries and utilities of the tools, such as contract checkers and common CLI helpers.
- `perfratio` keeps its product name, because it is a standalone tool with its own website and distribution.

## Consequences
- The prefix gives the role of every repo: `catalog-*`, `dataset-*` and `tools-*`. Sites and dot repos keep their names.
- GitHub redirects the old URLs, but submodules, CI checkouts and docs are updated to the new names.
- Code shared by several tools moves to `tools-commons` instead of being copied between them.
