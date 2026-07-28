---
title: "Postiz massa + /cortar_video auto (sem Photos)"
tier: episodic
tags:
  - telegram-hermes
  - postiz
  - cortar_video
  - publicacao-em-massa
  - youtube-shorts
created_at: 2026-07-28T12:00:00Z
status: active
source: grok-cli-session
kind: decision
---

# Postiz massa + /cortar_video auto (sem Photos)

Sessão de implementação no bot `telegram-hermes-freebot` (2026-07-28).

## Objetivo

Unificar **corte de vídeos** com **publicação em massa** via Postiz, sem depender de Google Fotos/Drive.

## O que mudou

### 1) Publicação em massa Postiz (`/postiz_massa`)

- Locks + watchdog `postiz_massa` (4h)
- Pacing anti-429 (`POSTIZ_DELAY_BETWEEN_PLATFORMS` / `POSTIZ_DELAY_BETWEEN_VIDEOS`)
- X/Twitter **excluído** por padrão (`POSTIZ_EXCLUDE_PLATFORMS=x,twitter`)
- YouTube sempre como **Shorts** (`YOUTUBE_FORCE_SHORTS=1` + formato 9:16)
- Mídia anexada na mensagem do comando
- Lote multi-mídia com **confirmação** (`/postiz_ok`) — avisos só após pausa no envio (sem spam por mídia)
- Falhas em `cache/postiz_massa_errors.json` + retry via `/republicar_erros`

### 2) `/cortar_video` → Postiz automático

- Após cortes OK em `Cortes_Salvos/<nome>/`, dispara `_start_postiz_massa_from_clips`
- Lock separado: `cortar_video` → libera → `postiz_massa`
- **Não apaga** arquivos locais se Postiz falhar
- Env: `CORTAR_AUTO_POSTIZ=1`

### 3) Sem Google Fotos / Drive no fluxo padrão

- `CORTAR_UPLOAD_GPHOTOS=0` (default OFF no código)
- `CORTAR_UPLOAD_DRIVE=0` (default OFF)
- Fluxo: **corta local → publica Postiz**

## Como usar

```text
/cortar_video https://youtube.com/...
```

Nome da pasta (ex.: `Lucas`) → corta → Postiz auto.

Manual:

```text
/postiz_massa pasta Lucas all
```

Múltiplas mídias:

```text
# anexa vídeos com legenda
/postiz_massa all Minha legenda
# …mais vídeos…
/postiz_ok
```

## Env relevante

```bash
POSTIZ_EXCLUDE_PLATFORMS=x,twitter
YOUTUBE_FORCE_SHORTS=1
YOUTUBE_FORCE_SHORTS_FORMAT=1
CORTAR_AUTO_POSTIZ=1
CORTAR_UPLOAD_GPHOTOS=0
CORTAR_UPLOAD_DRIVE=0
```

## Arquivos principais

- `bot.py` — handlers massa, pending/confirm, cortar→postiz
- `mcp_postiz.py` — exclude X, Shorts, bulk settings
- `.env` — flags acima

## Comandos de controle

| Comando | Função |
|---------|--------|
| `/postiz_ok` | Confirma lote e publica |
| `/postiz_cancela` | Cancela lote |
| `/postiz_lote` | Lista lote |
| `/cancelar` | Para tarefa + limpa lote |
| `CORTAR_AUTO_POSTIZ=0` | Desliga auto-postiz |

## Critério de pronto

- [x] Massa multi-rede com lock/pacing
- [x] Sem X
- [x] YouTube Shorts
- [x] Cortar → Postiz auto
- [x] Sem Photos/Drive no padrão
- [x] PM2 reinicia limpo
