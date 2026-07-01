---
title: "altere a configuração padrão do bot para usar a API -api_test freemode como o"
tier: episodic
tags:
  - auto
  - telegram
  - memoria-agente
  - hermes
  - telegram-hermes
created_at: 2026-07-01T21:46:46Z
status: active
source: ai-memory-primary
kind: agent
---

# altere a configuração padrão do bot para usar a API -api_test freemode como o

**altere a configuração padrão do bot para usar a API -api_test freemode como o** (resumo export)

title: altere a configuração padrão do bot para usar a API -api_test freemode como o
status: active
# altere a configuração padrão do bot para usar a API -api_test freemode como o
## Contexto
altere a configuração padrão do bot para usar a API [/api_test freemode] como o motor principal. Certifique-se de que a base_url e o model sejam atualizados em todas as funções de chamada de IA ( _call_grok_via_proxy , etc.) para garantir que o bot use este novo provedor por padrão."
### 1. Scope
- **Goal**: Replace the default provider with the new endpoint **`/api_test freemode`** and ensure the new model identifier is used consistently across all internal call helpers (`_call_grok_via_proxy`, `_call_grok_direct`, etc.).
### 2. High‑Level Migration Steps
| 1 | Define new configuration constants (`BASE_URL_NEW`, `MODEL_NEW`). | `config.py` (or equivalent). | Unit test that imports `config` and asserts values. |
