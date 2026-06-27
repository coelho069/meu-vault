---
data: "2026-06-20"
tags:
  - auto
  - telegram
  - memoria-agente
  - hermes
status: "active"
titulo: "youtube https---youtu.be-waHGleiNmMk-is=gxz0CeQR3CkvaofG"
---

# youtube https---youtu.be-waHGleiNmMk-is=gxz0CeQR3CkvaofG

## Contexto

**Usuario:**
/youtube https://youtu.be/waHGleiNmMk?is=gxz0CeQR3CkvaofG

**Hermes:**
O detalhamento dos problemas no [[Follow]] aparece como a camada em que a ferramenta deixa de ser apenas um painel geral de [[Qualidade]] e passa a funcionar como um mecanismo operacional de investigação. No fluxo demonstrado, o primeiro contato acontece com `npx follow` e depois com `summary`, que entregam uma visão consolidada dos problemas encontrados no projeto: [[Exports]], [[IAs]], [[Morto]], [[Duplicações]] e [[Funções com Alta Complexidade]]. Porém, essa visão inicial não é suficiente para concluir a limpeza, porque ela mostra o estado geral do sistema, mas não necessariamente resolve todos os pontos nem detalha cada caso que exige decisão humana. É nesse ponto que entram os comandos específicos, especialmente `dead code` e `dups`, usados para localizar com precisão onde estão os resíduos que permaneceram após a tentativa de correção automática.

A sequência prática descrita no vídeo é importante porque estabelece uma ordem segura de trabalho. Primeiro, o operador roda `npx follow` no terminal dentro do projeto, sem precisar instalar a ferramenta permanentemente. Em seguida, usa `summary` para obter um resumo mais sucinto dos problemas. Depois, antes de aplicar qualquer alteração, executa `npx follow fix --dry-run`, que mostra exatamente o que o [[Follow]] pretende corrigir sem modificar o código. Essa etapa é crítica em termos de [[SRE]] e [[Governança de Mudanças]], porque transforma uma ação potencialmente destrutiva em uma prévia auditável. A ferramenta informa que pode remover um export, um pacote ou outro

### Conexões Relacionadas

- [[Contexto_Usuario_youtube_https_youtu_v2]]
- [[Contexto_Usuario_youtube_https_youtu]]
- [[YouTube_YMc0f5i70Hc_v2]]
