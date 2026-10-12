# Roadmap

Initiatives in priority order. Each one is decomposed into specs inside the repos that own the work.

| # | Initiative | Tracking | Depends on |
|---|---|---|---|
| 1 | Org organization: naming, dot repos, community files, topics | this repo, [.github#1](https://github.com/BenchCommons/.github/issues/1) | — |
| 2 | Catalog contract and multi-catalog toolset | [tools-benchmark#29](https://github.com/BenchCommons/tools-benchmark/issues/29) | 1 |
| 3 | perfratio as the measurement engine | [tools-benchmark#30](https://github.com/BenchCommons/tools-benchmark/issues/30), [perfratio#240](https://github.com/BenchCommons/perfratio/issues/240) | 2 |
| 4 | Benchmark inputs: the `dataset-*` contract and datasets | [tools-dataset#1](https://github.com/BenchCommons/tools-dataset/issues/1), [dataset-names#24](https://github.com/BenchCommons/dataset-names/issues/24), [dataset-commons#1](https://github.com/BenchCommons/dataset-commons/issues/1) | 1 |
| 5 | catalog-algorithms: classic algorithms across languages | [catalog-algorithms#11](https://github.com/BenchCommons/catalog-algorithms/issues/11) | 2, 3, 4 |
| 6 | Continue TechEmpower Framework Benchmarks as catalog-web-frameworks | [.github#2](https://github.com/BenchCommons/.github/issues/2), [catalog-web-frameworks#1](https://github.com/BenchCommons/catalog-web-frameworks/issues/1) | 2 |
| 7 | Results website with several benchmark families | [website#5](https://github.com/BenchCommons/website/issues/5) | 2, 5 |
| 8 | catalog-ssg follow-up after the rename | [catalog-ssg#203](https://github.com/BenchCommons/catalog-ssg/issues/203) | 2 |
