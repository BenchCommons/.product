# BenchCommons product

Org-level product governance for [BenchCommons](https://github.com/BenchCommons):

- [`ROADMAP.md`](ROADMAP.md): org initiatives, their order and dependencies. Each initiative links to the issues and specs in the repos that own the work.
- [`CONTRACTS.md`](CONTRACTS.md): the contracts between repos. Each contract has one owner repo, where its spec lives; consumers only reference it.
- [`docs/adr/`](docs/adr): decisions that apply to several repos (format: context, decision, status, consequences).

Per-repo requirements, plans and tasks stay in each repo under `docs/specs/<NNN>-<feature>/`. This repo only holds what spans several repos.
