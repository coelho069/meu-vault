---
title: Progress feedback in Telegram and terminal
tier: semantic
tags:
- progress
- telegram
- terminal
bootstrapped_at: 2026-06-20T23:11:15.316459454Z
---
# Progress feedback in Telegram and terminal

The project added progress feedback in two stages.

First, commit `c81f3506` added a real-time progress bar specifically to the `akita` command.

Later, commit `210f3c02` implemented a visual progress bar in both Telegram and the terminal. The commit message does not state whether this generalized the earlier `akita` progress bar or introduced a separate implementation.

The supplied sources do not include progress states, formatting, update frequency, or cancellation behavior.

### Conexões Relacionadas

- [[telegram-bot-command-surface]]
- [[spiderfoot-integration]]
- [[Akita_YouTube_article_processing]]
- [[dynamic-timeouts-for-youtube-processing]]
- [[langgraph-stateful-agents]]
