---
title: analisar_chat integracao bot
tier: semantic
tags:
- auto
- comando
- hermes
- memoria-agente
- telegram
- telegram-hermes
created_at: 2026-06-27T03:30:00Z
status: active
source: hermes-telegram
---

# analisar_chat integracao bot

## Contexto

**Usuario:**
Comando não reconhecido: /analisar_chat — corrigir e implementar.

**Hermes:**
Criado o comando `/analisar_chat` no `bot.py` para analisar o historico da conversa atual com o Hermes.

## Implementacao

- **Handler:** `handle_analisar_chat_command` em `bot.py`
- **Helpers:** `_collect_analisar_chat_context`, `_build_analisar_chat_prompt`
- **Fontes de contexto:** memoria curta (`cache/memory.json`) + memoria persistente (`cache/persistent_memory.json`)
- **IA:** `call_simple_ai` com intent `analisar_chat`
- **Saida:** relatorio em 5 secoes (resumo, topicos, decisoes, pendencias, observacoes) via `_repo_chunk_send`
- **Roteador:** registrado apos `/resumo_hoje`, antes de `handle_unknown_slash_command`
- **Aliases de canal:** `/analisar`, `/channel_analyze`, `/channel_analyze_help`, `/channel_debug` adicionados em `known_prefixes`

## Uso

```
/analisar_chat
/analisar_chat pendencias de api
```

## Notas

- Comando distinto de `/analisar` (analise de canais Telegram via Telethon, modulo `channel_analyze.py` ainda ausente).
- Se nao houver historico salvo, o bot orienta o usuario a conversar antes de tentar novamente.
- Bot reiniciado via `pm2 restart telegram-bot` apos deploy.

---
**Tronco Cerebral:** [[MOC_Cerebro_Central]] | **Índice:** [[MOC_Indice_Geral]]
