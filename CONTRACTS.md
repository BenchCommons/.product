# Contracts between repos

Each contract is specified once, in its owner repo. Consumers reference that spec and never redefine it.

| Contract | Owner | Consumers | Status |
|---|---|---|---|
| Catalog contract: per-implementation layout, metadata schema, pinned Dockerfile, canonical runner, correctness check, result markers | tools-benchmark | catalog-algorithms, catalog-ssg, catalog-web-frameworks | to specify ([tools-benchmark#29](https://github.com/BenchCommons/tools-benchmark/issues/29)) |
| Measurement output: perfratio JSON schema, versioned | perfratio | tools-benchmark | to specify ([perfratio#240](https://github.com/BenchCommons/perfratio/issues/240)) |
| Benchmark inputs: deterministic samples, checksums, versioned releases | tools-dataset | dataset-names, dataset-commons, catalog-algorithms, tools-benchmark | to specify ([tools-dataset#1](https://github.com/BenchCommons/tools-dataset/issues/1)) |
| Published results: `docs/results/<date>/…`, `results.json` schema | tools-benchmark | website | exists for SSGs (`docs/results/README.md`); to generalize ([website#5](https://github.com/BenchCommons/website/issues/5)) |
| Generator index: `generators.json` | catalog-ssg | website, tools-benchmark | exists (`schema/generators.schema.json`) |
