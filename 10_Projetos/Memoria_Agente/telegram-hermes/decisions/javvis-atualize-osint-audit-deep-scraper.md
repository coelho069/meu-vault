---
title: "Javvis, atualize o osint_audit com deep scraping e fallback para Google Dorks"
tier: episodic
tags:
  - osint
  - telegram
  - memoria-agente
  - hermes
  - telegram-hermes
  - awesome-osint-list
  - scraping
created_at: 2026-07-01T02:30:00Z
status: active
source: ai-memory-primary
kind: agent
---

# Javvis, atualize o osint_audit com deep scraping e fallback para Google Dorks

**Objetivo:** Melhorar o módulo `osint_awesome_engine.py` para que o comando `/osint_audit` nunca retorne 0 resultados. Usar scraping profundo do Awesome-OSINT-List e fallback para busca na web via Dorks.

## Mudanças Implementadas

### 1. Busca por Padrões de URL
- Scraper agora varre TODO o README.md usando regex para domínios de deploy:
  - `*.vercel.app`
  - `*.lovable.app`
  - `*.bolt.new`
  - `*.supabase.co`
  - + netlify, onrender, fly, railway etc.
- Coleta URLs completas com paths.

### 2. Extração de Links por Palavras-chave
- Extrai todos os links Markdown e bare URLs que contenham:
  - app, dashboard, api, dev, staging, vercel, lovable, bolt, supabase etc.

### 3. Fallback para Google Dorks
- Se após Link-Check restarem < 3 alvos ativos:
  - Gera automaticamente dorks como:
    - `site:vercel.app <query>`
    - `inurl:vercel.app (app OR dashboard OR api OR dev OR staging)`
  - Inclui no relatório como seção de busca recomendada.

### 4. Pipeline Completo
- Todos os links passam por:
  - Link-Check (validação de ativos vivos)
  - Plugin Secrets (detecção de chaves expostas via regex)
  - Plugin Resilience (testes de injeção SQL como UNION SELECT)

### 5. Relatório de Descoberta
- Alvos não presentes no parsing original do repositório são marcados como:
  - "✨ New Asset Discovered"

## Estrutura do Módulo Atualizado

- `AwesomeOSINTScraper`: Fetch + parse agressivo de URLs e links.
- `LinkCheckFilter`: Validação paralela de disponibilidade.
- `OSINTOrchestrator`:
  - `discover_and_filter(query)`
  - `fallback_dorks(query)`
  - `run_pipeline(target)` → Secrets + Resilience
  - `generate_report(targets, query)` com marcação de new assets + dorks.

## Como Usar no Bot

```
/osint_audit vercel
/osint_audit lovable
/osint_audit bolt
```

O bot agora:
- Caça no repositório
- Extrai padrões de deploy
- Filtra ativos
- Audita com plugins
- Se pouco resultado → sugere dorks para caçar na web
- Marca novos assets descobertos

## Integração

- Handler `handle_osint_audit_command` adicionado no bot.py
- Módulo importado dinamicamente
- Usa a mesma estrutura de plugins da asset_audit_engine

## Próximos Passos Sugeridos

- Adicionar mais plataformas de deploy (Railway, Render, Fly.io, etc.)
- Integrar busca real via API (ex: Google Custom Search se disponível)
- Salvar descobertas em vault Obsidian automaticamente
- Gerar notebook Jupyter com os resultados

---

**Status:** Implementado e atualizado no arquivo `osint_awesome_engine.py`

**Referência:** Decisões anteriores sobre integração do Awesome-OSINT-List.
