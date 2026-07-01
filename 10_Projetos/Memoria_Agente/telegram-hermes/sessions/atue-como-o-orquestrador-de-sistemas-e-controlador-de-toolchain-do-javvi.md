---
title: "atue como o Orquestrador de Sistemas e Controlador de Toolchain do Javvis.bot. V"
tier: episodic
tags:
  - auto
  - telegram
  - memoria-agente
  - hermes
  - telegram-hermes
created_at: 2026-07-01T04:07:12Z
status: active
source: ai-memory-primary
kind: agent
---

# atue como o Orquestrador de Sistemas e Controlador de Toolchain do Javvis.bot. V

**atue como o Orquestrador de Sistemas e Controlador de Toolchain do Javvis.bot. V** (resumo export)

status: active
# atue como o Orquestrador de Sistemas e Controlador de Toolchain do Javvis.bot. V
## Contexto
atue como o Orquestrador de Sistemas e Controlador de Toolchain do Javvis.bot. Você tem acesso privilegiado às ferramentas locais instaladas neste ambiente VPS (/home/ubuntu/). Sua função é coordenar a execução do pipeline de auditoria. Sua Missão: 1. Ativação do Motor de Busca: Execute o módulo autonomous_search.py (via subprocess) para identificar 10 URLs reais de projetos ativos em *.vercel.app e *.lovable.app. 2. Execução do Analisador: Para cada URL capturada, dispare o comando python3 seo_analyzer.py <url> --json. 3. Processamento de Resultados: Leia o JSON gerado, extraia os campos 'title', 'hero_snippet' e 'config_exposed'. 4. Relatório de Terminal: Formate o output final para o chat do Telegram, mostrando os alvos e o status de conformidade de cada um. Não aja como um assistente de texto. Aja como o controlador de backend que dispara os comandos de sistema necessários para completar a tarefa de auditoria.
