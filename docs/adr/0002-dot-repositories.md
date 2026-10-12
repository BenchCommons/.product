# 0002 — Three dot repositories for org governance

## Status
Accepted (2026-10-12).

## Context
Candidates were `.github`, `.github-private`, `.security`, `.workflow`, `.product`, `.specs` and `.agents`. Every extra governance repo spreads the rules thinner and makes them easier to drift apart.

## Decision
Use three repos:
- `.github` (public). It holds the org profile and the default community health files (CONTRIBUTING, CODE_OF_CONDUCT, SECURITY, issue and PR templates). It also holds the reusable workflows and `workflow-templates/`, and the org `AGENTS.md` with the rules for AI agents.
- `.github-private` (members only). It holds the member profile, runbooks, incident response, and DevOps governance (rulesets, runners, infrastructure, secrets policy).
- `.product` (public). It holds the org roadmap, cross-repo ADRs and the contract index.

Rejected:
- `.security`: GitHub already uses `SECURITY.md` in `.github` as the default policy, and private procedures go to `.github-private`.
- `.workflow`: public repos can only call reusable workflows that live in public repos, and workflow templates must live in `.github`.
- `.specs`: same role as `.product`.
- `.agents`: AI rules are not secret, so they fit in `.github`.

## Consequences
- `.github` and `.github-private` get special treatment from GitHub, so their contents apply automatically.
- Changes to shared CI are reviewed in one place (`.github`).
