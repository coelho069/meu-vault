---
title: "Gere um comando único de terminal (Bash One-Liner) que use 'sed' ou 'python3' pa"
tier: episodic
tags:
  - auto
  - telegram
  - memoria-agente
  - hermes
  - telegram-hermes
created_at: 2026-07-01T06:45:54Z
status: active
source: ai-memory-primary
kind: agent
---

# Gere um comando único de terminal (Bash One-Liner) que use 'sed' ou 'python3' pa

**Gere um comando único de terminal (Bash One-Liner) que use 'sed' ou 'python3' pa** (resumo export)

title: Gere um comando único de terminal (Bash One-Liner) que use 'sed' ou 'python3' pa
status: active
# Gere um comando único de terminal (Bash One-Liner) que use 'sed' ou 'python3' pa
## Contexto
Gere um comando único de terminal (Bash One-Liner) que use 'sed' ou 'python3' para injetar no arquivo /home/ubuntu/telegram-hermes-freebot/bot.py o seguinte: 1. O 'import aiohttp' no topo. 2. A função 'async def scan_db_interfaces_command' com a lógica de varredura. 3. A linha 'application.add_handler(CommandHandler("scan_db_interfaces", scan_db_interfaces_command))' dentro da função main(). O comando deve ser seguro e não sobrescrever o arquivo inteiro, apenas adicionar essas partes.
sed -i "/^def main()/a application.add_handler(CommandHandler(\"scan_db_interfaces\", scan_db_interfaces_command))" /home/ubuntu/telegram-hermes-freebot/bot.py
f.write(line); f.write('    application.add_handler(CommandHandler(\"scan_db_interfaces\", scan_db_interfaces_command))\n'); main_reached = True; \
