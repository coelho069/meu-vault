---
title: "pesquisar servidores expostos com arquivos .env e dumps de banco de dados .sql"
tier: episodic
tags:
  - auto
  - telegram
  - memoria-agente
  - hermes
  - telegram-hermes
created_at: 2026-07-01T19:12:58Z
status: active
source: ai-memory-primary
kind: agent
---

# pesquisar servidores expostos com arquivos .env e dumps de banco de dados .sql

**pesquisar servidores expostos com arquivos .env e dumps de banco de dados .sql** (resumo export)

status: active
# pesquisar servidores expostos com arquivos .env e dumps de banco de dados .sql
## Contexto
**Relatório de Resiliência e Conformidade Técnica – Alvo “.configurações de ambiente”**
### 1. Visão Geral dos Vetores de Auditoria
| **Descoberta de Superfície** | `site:.configurações de ambiente inurl:app/` <br> `site:.configurações de ambiente intitle:"app"` <br> `site:.configurações de ambiente inurl:login` | Identificar páginas públicas que exponem rotas de aplicação ou interfaces de autenticação. |
| **Infraestrutura Backend** | `site:.configurações de ambiente inurl:api` <br> `site:.configurações de ambiente inurl:painel de controle gerencial` <br> `site:.configurações de ambiente inurl:v1 OR inurl:v2` | Mapear endpoints de API e consoles administrativos que podem revelar detalhes de arquitetura. |
| **Detecção de Firebase/DB** | `site:.configurações de ambiente intext:"firebase"` <br> `site:.configurações de ambiente intext:"infraestrutura de backend"` <br> `site:.configurações de ambiente intext:"SUPABASE_URL" OR intext:"firebaseio"` | Detectar referências a serviços

...[memoria destilada]
