---
title: "PROTOCOLO DE CRIAÇÃO DE MÓDULO AUTÔNOMO - NÍVEL INFINITO Instrução- Gere um coma"
tier: episodic
tags:
  - auto
  - telegram
  - memoria-agente
  - hermes
  - telegram-hermes
created_at: 2026-07-01T06:52:21Z
status: active
source: ai-memory-primary
kind: agent
---

# PROTOCOLO DE CRIAÇÃO DE MÓDULO AUTÔNOMO - NÍVEL INFINITO Instrução- Gere um coma

**PROTOCOLO DE CRIAÇÃO DE MÓDULO AUTÔNOMO - NÍVEL INFINITO Instrução- Gere um coma** (resumo export)

status: active
# PROTOCOLO DE CRIAÇÃO DE MÓDULO AUTÔNOMO - NÍVEL INFINITO Instrução- Gere um coma
## Contexto
## PROTOCOLO DE CRIAÇÃO DE MÓDULO AUTÔNOMO - NÍVEL INFINITO Instrução: Gere um comando único de terminal (Bash One-Liner) que: 1. Crie o arquivo /home/ubuntu/telegram-hermes-freebot/scan_db.py contendo a função 'async def scan_db_interfaces_command(update, context)' com a lógica de varredura assíncrona para os 10 domínios brasileiros. 2. Adicione 'from scan_db import scan_db_interfaces_command' no topo do seu bot.py. 3. Adicione 'application.add_handler(CommandHandler("scan_db_interfaces", scan_db_interfaces_command))' na função main() do bot.py. 4. Reinicie o bot via PM2. O objetivo é a modularização da arquitetura de observabilidade. Entregue o comando Bash completo pronto para execução no VPS.
printf "\nasync def scan_db_interfaces_command(update: Update, context: ContextTypes.DEFAULT_TYPE):\n    import aiohttp, asyncio\n    domains = [\n        'google.com.br', 'uol.com.br', 'globo.com', 'terra.com.br', 'bol.com.br',\n        'r7.com', 'ig.com.br', 'abril.com.br', 'g1.c

...[memoria destilada]
