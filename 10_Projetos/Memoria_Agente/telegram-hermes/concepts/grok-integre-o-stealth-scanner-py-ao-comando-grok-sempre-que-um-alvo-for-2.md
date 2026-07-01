---
title: "Grok, integre o stealth_scanner.py ao comando -grok. Sempre que um alvo for anal"
tier: episodic
tags:
  - auto
  - telegram
  - memoria-agente
  - hermes
  - telegram-hermes
created_at: 2026-07-01T20:20:13Z
status: active
source: ai-memory-primary
kind: agent
---

# Grok, integre o stealth_scanner.py ao comando -grok. Sempre que um alvo for anal

**Grok, integre o stealth_scanner.py ao comando -grok. Sempre que um alvo for anal** (resumo export)

title: Grok, integre o stealth_scanner.py ao comando -grok. Sempre que um alvo for anal
status: active
# Grok, integre o stealth_scanner.py ao comando -grok. Sempre que um alvo for anal
## Contexto
Grok, integre o stealth_scanner.py ao comando /grok. Sempre que um alvo for analisado, execute o scanner e mostre os resultados reais no chat.
Faltam dados no grafo. Não há referência a `stealth_scanner.py` nem ao ponto de integração com `/grok` além do handler `handle_grok_command` (bot.py:23072), que hoje só dispara `_run_gemini_to_pdf_cli`. Para integrar, preciso saber: (1) caminho absoluto do `stealth_scanner.py`, (2) assinatura/CLI dele, (3) onde no fluxo do `/grok` você quer o gatilho (antes ou depois do PDF). Sem isso, qualquer patch é chute. Me passa esses três pontos que eu entrego o diff mínimo via `sed`/`python3` one-liner, igual ao padrão que já usamos aqui.
