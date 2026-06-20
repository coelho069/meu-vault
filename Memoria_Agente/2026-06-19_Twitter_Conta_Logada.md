---
data: "2026-06-19"
titulo: "Twitter Conta Logada"
status: active
tags:
  - auto
  - hermes
  - memoria-agente
  - social
  - telegram
  - twitter
---






# agora verificar qual conta do Twitter ta logada

## Contexto

**Usuario:**
agora verificar qual conta do Twitter ta logada

**Hermes:**
Vou verificar no projeto qual conta do Twitter está logada — primeiro explorando a configuração e credenciais em `/home/ubuntu/telegram-hermes-freebot`.
Encontrei o comando `twitter whoami` — vou executá-lo para confirmar a conta logada.
A conta logada no Twitter/X agora é **@SynMateus**.

Confirmei com `twitter whoami`:

| Campo | Valor |
|-------|-------|
| **Username** | `SynMateus` |
| **Nome** | `mateus.syn` |
| **ID** | `2002457797229965312` |
| **Seguidores** | 2 |
| **Seguindo** | 191 |
| **Tweets** | 307 |

### Onde a autenticação está configurada

1. **CLI `twitter`** (publicar, feed, etc.) — cookies em `~/.bashrc` (`TWITTER_AUTH_TOKEN` + `TWITTER_CT0`)
2. **`tools/twitter_reach/cookies.json`** — mesmos cookies (para ler curtidas)
3. **`.env`** — `TWITTER_USERNAME=SynMateus` (só metadado, não controla login)

### Observação

Antes (sessão de hoje) estava logado como **@1MarcoAurelio2**; os cookies foram atualizados e agora apontam para **@SynMateus**.

Há uma inconsistência no `.env`: `TWITTER_USER_ID=1519721757303033858`, mas o `whoami` retorna `2002457797229965312`. O username está certo; o ID no `.env` parece desatualizado.

O `xurl` não está autenticado (401) — o que importa para o bot é o CLI `twitter`, que está OK como @SynMateus.

<!-- memoria-agente-graph -->
**Índice:** [[000_INDEX_CENTRAL]]

#auto #hermes #memoria-agente #social #telegram #twitter
<!-- /memoria-agente-graph -->
