---
title: Telegram bot command surface
tier: semantic
tags:
- telegram
- commands
- integrations
bootstrapped_at: 2026-06-20T23:11:15.316459454Z
---
# Telegram bot command surface

The project is a Telegram bot with AI automation and integrations. The earliest supplied history says it was expanded with “Telegram AI automation commands” and then broader “Telegram bot automation and integrations” (commits `32c6f668` and `ac9ce359`).

The command surface grew over time:

- API health/status checking was added in commit `2f34bc56` (“add API health check status command”).
- `/ipcheck` was added to integrate the SpiderFoot engine with Telegram in commit `70cc0e86`.
- `/osint` and `/attack_surface` were added as a “suite completa de comandos spiderfoot” organized by use case in commit `5f381947`.
- `/repo_analyze` existed, was disabled during a hotfix because a file was absent, and later restored (commits `41512594` and `2d8eff2e`).
- `/resumo_hoje` was added for a daily changelog via git and AI in commit `46dfffbd`, then refactored to show a chronological timeline based on system timestamps in commit `adf91084`.

The supplied sources do not include handler names, exact command arguments, or message formats, so those details should be checked in the code rather than inferred from the log.

### Conexões Relacionadas

- [[spiderfoot-integration]]
- [[repository-analysis-and-daily-summary]]
- [[router-wiring-can-hide-existing-commands]]
- [[Progress_feedback_Telegram_terminal]]
- [[Akita_YouTube_article_processing]]
