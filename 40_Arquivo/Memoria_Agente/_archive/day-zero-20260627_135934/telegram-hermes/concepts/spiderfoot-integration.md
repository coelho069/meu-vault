---
title: SpiderFoot integration
tier: semantic
tags:
- spiderfoot
- osint
- telegram
bootstrapped_at: 2026-06-20T23:11:15.316459454Z
---
# SpiderFoot integration

SpiderFoot appears as the project’s OSINT / attack-surface engine, exposed through Telegram commands.

From commit `70cc0e86`: the project implemented `/ipcheck` by integrating the SpiderFoot engine with Telegram.

From commit `5f381947`: the project integrated a “suite completa de comandos spiderfoot” via `/osint` and `/attack_surface`, organized by use case.

From commit `89c7427d`: `/osint` and `/attack_surface` were later reconnected in the bot router. This implies those routes can be present in the codebase but not effectively reachable if the router wiring is broken.

The log does not provide the SpiderFoot module list, output schema, or supported target types beyond what is implied by the command names.

### Conexões Relacionadas

- [[telegram-bot-command-surface]]
- [[router-wiring-can-hide-existing-commands]]
- [[Spiderfoot]]
- [[0001-guard-startup-with-venv-and-single-instance-protection]]
- [[ai-memory-mcp-server]]
