# 0006 — Name sites as `website-*`

## Status
Accepted (2026-10-12). Amends the site rule in [ADR 0001](0001-repository-naming.md).

## Context
ADR 0001 named sites with plain names or `<tool>-website` (`website`, `perfratio-website`). The two patterns were inconsistent, and the plain name `website` did not say which site it was. Catalogs, datasets and tools already carry a role prefix followed by a subject (`catalog-*`, `dataset-*`, `tools-*`).

## Decision
- Sites are named `website-<subject>`, like the other role prefixes:
  - `website` was renamed to `website-results` (benchmark results);
  - `perfratio-website` was renamed to `website-perfratio` (marketing and documentation for perfratio).
- The rest of ADR 0001 is unchanged.

## Consequences
- The prefix gives the role of every repo: `catalog-*`, `dataset-*`, `tools-*` and `website-*`.
- GitHub redirects the old URLs, but docs, links and package names are updated to the new names.
- The Cloudflare worker of website-perfratio still uses the old name `perfratio-website`. Renaming it creates a new deployment, so it is tracked in an issue in that repo.
