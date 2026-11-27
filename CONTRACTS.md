# Contracts between repos

Each contract is specified once, in its owner repo. Consumers reference that spec and never redefine it.

| Contract | Owner | Consumers | Status |
|---|---|---|---|
| Catalog contract: per-implementation layout, metadata schema, pinned Dockerfile, canonical runner, correctness check, result markers | tools-benchmark | catalog-algorithms, catalog-ssg, catalog-web-frameworks | proposed, awaiting review: [tools-benchmark spec 010](https://github.com/BenchCommons/tools-benchmark/blob/master/docs/specs/010-catalog-contract/spec.md) ([tools-benchmark#29](https://github.com/BenchCommons/tools-benchmark/issues/29)) |
| Measurement output: perfratio JSON schema, versioned | perfratio | tools-benchmark | to specify ([perfratio#240](https://github.com/BenchCommons/perfratio/issues/240)) |
| Benchmark inputs: deterministic samples, checksums, versioned releases | tools-dataset | dataset-names, dataset-commons, catalog-algorithms, tools-benchmark | spec written: [tools-dataset spec 001](https://github.com/BenchCommons/tools-dataset/blob/main/docs/specs/001-input-contract/spec.md); not implemented yet ([tools-dataset#1](https://github.com/BenchCommons/tools-dataset/issues/1)) |
| Published results: `docs/results/<date>/…`, `results.json` schema | tools-benchmark | website-results | exists for SSGs ([`docs/results/README.md`](https://github.com/BenchCommons/tools-benchmark/blob/master/docs/results/README.md)); to generalize ([website-results#5](https://github.com/BenchCommons/website-results/issues/5)) |
| Generator index: `generators.json` | catalog-ssg | website-results, tools-benchmark | exists ([`schema/generators.schema.json`](https://github.com/BenchCommons/catalog-ssg/blob/master/schema/generators.schema.json)) |
