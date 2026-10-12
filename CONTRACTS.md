# Contracts between repos

Each contract is specified once, in its owner repo. Consumers reference that spec and never redefine it.

| Contract | Owner | Consumers | Status |
|---|---|---|---|
| Catalog contract: per-implementation layout, metadata schema, pinned Dockerfile, canonical runner, correctness check, result markers | benchmark-tool | catalog-algorithms, catalog-ssg, catalog-web-frameworks | to specify ([benchmark-tool#29](https://github.com/BenchCommons/benchmark-tool/issues/29)) |
| Measurement output: perfratio JSON schema, versioned | perfratio | benchmark-tool | to specify ([perfratio#240](https://github.com/BenchCommons/perfratio/issues/240)) |
| Benchmark inputs: deterministic samples, checksums, versioned releases | dataset-tool | dataset-names, dataset-commons, catalog-algorithms, benchmark-tool | to specify ([dataset-tool#1](https://github.com/BenchCommons/dataset-tool/issues/1)) |
| Published results: `docs/results/<date>/…`, `results.json` schema | benchmark-tool | website | exists for SSGs (`docs/results/README.md`); to generalize ([website#5](https://github.com/BenchCommons/website/issues/5)) |
| Generator index: `generators.json` | catalog-ssg | website, benchmark-tool | exists (`schema/generators.schema.json`) |
