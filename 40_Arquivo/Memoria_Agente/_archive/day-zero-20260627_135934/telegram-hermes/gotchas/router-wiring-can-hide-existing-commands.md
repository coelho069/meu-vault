---
title: Router wiring can hide existing commands
tier: semantic
tags:
- router
- commands
- spiderfoot
bootstrapped_at: 2026-06-20T23:11:15.316459454Z
---
# Router wiring can hide existing commands

Commit `5f381947` added the SpiderFoot command suite for `/osint` and `/attack_surface`.

Immediately after, commit `89c7427d` fixed the bot by reconnecting the `/osint` and `/attack_surface` routes in the router (“religa rotas ... no roteador do bot”).

The practical gotcha from the history is that implementing command functionality is not sufficient: commands can exist but still be unavailable if the bot router is not wired to them.

The supplied log does not name the router file or handler functions.

### Conexões Relacionadas

- [[spiderfoot-integration]]
- [[telegram-bot-command-surface]]
- [[Akita_YouTube_article_processing]]
- [[Spiderfoot]]
- [[repository-analysis-and-daily-summary]]
