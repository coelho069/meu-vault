---
title: Repository analysis and daily summary commands
tier: semantic
tags:
- repo-analysis
- git
- ai
bootstrapped_at: 2026-06-20T23:11:15.316459454Z
---
# Repository analysis and daily summary commands

The project contains repository-analysis features and a daily-summary command that combine git history with AI.

`/repo_analyze` has a notable lifecycle in the supplied history:

- Commit `41512594` applied a hotfix fail-safe disabling imports and handlers for `repo_analyze` because an expected file was absent, in order to stabilize boot.
- Commit `2d8eff2e` restored the `repo_analyze` module and reactivated blocked commands.
- Commit `eee82c74` refactored `/repo_analyze` output to focus on short, actionable insights.

`/resumo_hoje` was introduced in commit `46dfffbd` as a daily changelog via git and AI. Commit `adf91084` then refactored it to display a chronological timeline based on system timestamps.

The history says these features exist, but does not include prompt templates, exact output examples, or where the git data is read from.