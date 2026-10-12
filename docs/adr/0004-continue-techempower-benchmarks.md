# 0004 — Continue the TechEmpower Framework Benchmarks

## Status
Proposed. Depends on the license review in [.github#2](https://github.com/BenchCommons/.github/issues/2).

## Context
`TechEmpower/FrameworkBenchmarks` was archived in 2026. benchmark-tool is already derived from its toolset, and `catalog-web-frameworks` exists for web frameworks.

## Decision (proposed)
- Import the framework implementations, with their history, into `catalog-web-frameworks`, and adapt them to the catalog contract.
- Fork TFBVerifier as the correctness stage and TFBDatabases as a `dataset-*` input.
- Use TFBToolset, tfb-status and tfb-azure-terraform as references.
- Keep attribution and license notices. Do not reuse TechEmpower branding or results.

## Consequences
BenchCommons becomes the maintained home of a large multi-language web benchmark. This adds maintenance load, so CI must test only changed implementations on pull requests.
