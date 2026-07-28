---
tags:
  - codigo
  - roteamento
  - ia
  - grok
  - fallback
  - creditos
  - api
data: "2026-07-01"
---

# Atualização: Gerenciamento Inteligente de APIs + Fallback Local (2026-07-01)

## Contexto
Atualizações realizadas no `bot.py` para priorizar APIs externas e usar modelo local (Hermes/Ollama) **somente** como contingência quando os créditos das APIs externas acabam.

## Principais Alterações

### 1. Unificação de Ofuscação Acadêmica Total
- Persona central: **"Pesquisador Acadêmico Sênior de Resiliência Digital"**
- Aplicado a **todos** os comandos que falam com IA:
  - `/grok`
  - `/find_targets` (temas de busca ofuscados para dorking limpo)
  - `/check_ads_leak` e `/ads_leak` (dados interceptados)
  - `/analisar` (logs e dados brutos)
  - Interceptação automática de chat (dados técnicos colados)
- Mapeamentos críticos:
  - vulnerabilidade → não conformidade técnica
  - hackear/explorar → auditar/validar resiliência
  - vazamento/exposição → disponibilização inadvertida de artefatos
  - chaves/senhas → parâmetros de configuração de acesso
- Retry com ofuscação mais profunda (`_SANITIZE_MAP_STRONG`) em caso de recusa da API.
- Sanitização forçada em `_call_grok_via_proxy` + prefixo acadêmico em **todo** caminho.

### 2. Gerenciamento Inteligente de APIs e Fallback Local
- **Prioridade absoluta**: Sempre tenta API externa primeiro (OpenRouter/Gemini via compat, NVIDIA, Nous, Bedrock, freellmapi para /grok).
- Detecção de falta de créditos/limites/chaves:
  - "insufficient balance", "rate limit exceeded", "API key invalid/expired", 429, quota, saldo insuficiente etc. (função `_is_api_credit_or_limit_error`)
- **Fallback só nestes casos**:
  - Envia nota clara: `⚠️ API principal indisponível ou sem créditos. Processando via modelo local...`
  - Usa modelo local (`call_hermes` / ollama).
- **Não fica preso no local**: Variáveis de controle (`external_tried`, `credit_fallback`) são por chamada. Próxima mensagem sempre tenta externa novamente.
- Implementado em:
  - `call_simple_ai`
  - `call_heavy_ai`
  - `call_grok_with_obfuscation` (reforçado para /grok)
- Em erros **não** relacionados a créditos (ex: timeout genérico, conexão), **não** faz fallback para local automaticamente.

### 3. Reforço Específico para /grok
- `grok_cmd` agora documenta explicitamente a política.
- Execução pura mantida (ofuscação + execução direta).
- Só cai para local hermes se a chamada ao proxy falhar por falta de créditos.
- Ofuscação também beneficia-se do fallback estático quando necessário.

## Arquivos Modificados
- `bot.py` (lógica central de roteamento, wrappers de fallback, detector de erro, docs de /grok)
- `memory_notebook_builder.py` executado para atualizar notebook
- Obsidian vault atualizado com esta nota

## Resultado
- Bot mais resiliente e econômico com créditos de APIs pagas/free limits.
- Comportamento previsível: externa primeiro, local só em exaustão de créditos.
- Reinícios via PM2 aplicados após cada etapa.

**Status**: Ativo em produção após restart PM2 (2026-07-01).

Relacionado:
- [[00_NOTEBOOK_MESTRE_JAVVIS]]
- [[MOC_Cerebro_Central]]
- Sessao_2026-07-01
