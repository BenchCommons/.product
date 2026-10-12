# 0003 — Default branch and licenses

## Status
Proposed. Awaiting the maintainer's decision.

## Context
Default branches are mixed: `master` in benchmark-tool, catalog-algorithms, catalog-ssg, dataset-names, perfratio and professor-website-exemple; `main` in the rest.

Licenses are also mixed: MIT (website, catalog-algorithms), Apache-2.0 (perfratio, dataset-names), Unlicense (catalog-ssg), and TechEmpower's BSD-3 (benchmark-tool, FrameworkBenchmarks; GitHub reports NOASSERTION). Other repos have none: .github, perfratio-website, catalog-web-frameworks, dataset-commons and dataset-tool.

## Options
- Branch: standardize on `main`. GitHub retargets open PRs and redirects the old name, but local clones, CI filters and docs must be updated. The other option is to keep each repo as it is.
- Code licenses: a single default for new repos (e.g. Apache-2.0, which has a patent grant). Inherited licenses such as TechEmpower's BSD-3 are kept.
- Data licenses: datasets use a data license compatible with their sources (e.g. CC-BY-4.0 or ODbL), checked per source.

## Consequences
To be defined with the decision.
