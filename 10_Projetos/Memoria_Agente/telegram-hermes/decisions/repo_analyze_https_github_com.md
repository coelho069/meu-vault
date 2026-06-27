---
title: repo_analyze https---github.com-DeusData-codebase-memory-mcp
tier: semantic
tags:
- auto
- telegram
- memoria-agente
- hermes
- telegram-hermes
created_at: 2026-06-27T08:27:19Z
status: active
source: hermes-telegram
---

# repo_analyze https---github.com-DeusData-codebase-memory-mcp

## Contexto

**Usuario:**
/repo_analyze https://github.com/DeusData/codebase-memory-mcp

**Hermes:**
**🎯 Resumo Executivo** Servidor MCP de inteligência de código que indexa repositórios em um grafo persistente para consultas rápidas por agentes de IA. Útil para dar ao Hermes memória estrutural sobre codebases sem enviar o código para serviços externos. **🏗️ Arquitetura Core** - C - MCP Server - Grafo de conhecimento local - Análise AST - Binário estático **💡 Valor para o Hermes** - Permite responder perguntas técnicas sobre repositórios com menos leitura manual de arquivos. - Pode acelerar fluxos de auditoria, onboarding e análise de PRs via Telegram. - Reduz consumo de contexto ao trocar buscas extensas por consultas estruturais. **🛠️ Integração** Onde plugar: no módulo de ferramentas MCP do Hermes, como backend local de análise de repositórios acessado pelos workers do bot. 1. Baixar o binário Linux compatível na VPS e validar assinatura/checksum antes de usar. 2. Rodar o comando de instalação/configuração para registrar o MCP no ambiente do agente usado pelo Hermes. 3. Criar comandos no Telegram para indexar repositórios autorizados e consultar funções, rotas, classes e relações do grafo.
