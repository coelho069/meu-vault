---
title: youtube https---youtu.be-waHGleiNmMk-is=gxz0CeQR3CkvaofG
tier: episodic
tags:
- auto
- hermes
- memoria-agente
- telegram
- telegram-hermes
created_at: 2026-06-20T12:00:00Z
source: hermes-obsidian
migrated_from: 2026-06-20_youtube_https_youtu_be_wahgleinmmk_is_gxz0ceqr3ckvaofg_141628.md
---

# youtube https---youtu.be-waHGleiNmMk-is=gxz0CeQR3CkvaofG

## Contexto

**Usuario:**
/youtube https://youtu.be/waHGleiNmMk?is=gxz0CeQR3CkvaofG

**Hermes:**
As [[Correções Automáticas]] aparecem no vídeo como o ponto de equilíbrio entre velocidade e segurança no uso do [[Follow]]. A ferramenta não é apresentada apenas como um scanner que aponta problemas, mas como um mecanismo capaz de executar parte da limpeza do projeto de forma autônoma, especialmente quando os problemas são considerados triviais e de baixo risco. O fluxo demonstrado começa com a inspeção por `npx follow` e `summary`, mas ganha força operacional quando entra o comando `npx follow fix --dry-run`. Esse detalhe é central: antes de modificar qualquer arquivo, o [[Follow]] mostra exatamente o que pretende fazer. Na prática, o `--dry-run` funciona como uma camada de [[Preview de Mudanças]], permitindo que o usuário valide a intenção da ferramenta antes de aceitar a correção. Essa abordagem reduz o risco de uma automação agressiva apagar algo importante apenas porque, naquele momento, parece não estar em uso.

O vídeo enfatiza que o [[Follow]] pode remover automaticamente itens como [[Exports Não Utilizados]], [[Dependências Não Utilizadas]] e partes de [[Código Morto]] quando a ferramenta entende que a remoção não deve impactar o projeto. O exemplo citado mostra o comando informando que vai remover um export, remover um pacote e aplicar ajustes equivalentes. Para tornar essa decisão mais auditável, o apresentador demonstra também `npx follow fix --dry-run --format json`, que organiza a saída em um formato mais fácil de ler, mostrando o tipo do ajuste, o caminho do arquivo, a linha e o nome do recurso envolvido. Do ponto de vista de [[SRE]], isso é importante porqu
