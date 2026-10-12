# 0004 — Continue the TechEmpower Framework Benchmarks

## Status
Proposed. The license review is done (BSD-3-Clause, see below); awaiting the maintainer's decision to start the import.

## Context
TechEmpower officially sunset the project on 2026-03-24 ([FrameworkBenchmarks#10932](https://github.com/TechEmpower/FrameworkBenchmarks/issues/10932)) and archived the repo. FrameworkBenchmarks, TFBVerifier, TFBDatabases, TFBToolset and tfb-status are BSD-3-Clause (© TechEmpower, Inc.). tools-benchmark is already derived from its toolset, and `catalog-web-frameworks` exists for web frameworks.

## Decision (proposed)
- Import the framework implementations, with their history, directly from `TechEmpower/FrameworkBenchmarks` into `catalog-web-frameworks`, and adapt them to the catalog contract. The old `BenchCommons/FrameworkBenchmarks` fork was removed; the archived upstream is the source.
- Fork TFBVerifier as the correctness stage and TFBDatabases as a `dataset-*` input.
- Use TFBToolset, tfb-status and tfb-azure-terraform as references.
- Keep the copyright and license notices (BSD-3, clause 1 and 2). Do not use the TechEmpower name to endorse or promote BenchCommons (clause 3): describe it as continuing the archived project, with attribution. Contact: tfb@techempower.com.

## Consequences
BenchCommons becomes the maintained home of a large multi-language web benchmark. This adds maintenance load, so CI must test only changed implementations on pull requests.
