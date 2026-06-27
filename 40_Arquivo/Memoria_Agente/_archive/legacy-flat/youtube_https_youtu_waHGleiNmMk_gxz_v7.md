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
O ponto mais importante do `fix` no [[Follow]] é que ele não deve ser entendido como um botão mágico de limpeza total, mas como uma etapa controlada dentro de um fluxo de [[Higiene]]. A transcrição deixa claro que a ferramenta identifica problemas como [[Morto]], [[Exports]], [[IAs]], [[Codigo_Duplicado]] e funções com [[premissa_central_simples_operacionalmente_importante]], mas também mostra que a correção automática tem limites deliberados. Quando o autor roda o `npx follow fix --dry-run`, a ferramenta primeiro informa exatamente o que pretende fazer, sem modificar o projeto. Esse comportamento é essencial para segurança operacional: antes de apagar um export, remover um pacote ou alterar algum recurso, o desenvolvedor consegue observar a intenção da ferramenta e decidir se aquilo faz sentido no contexto real do projeto.

O uso de `--dry-run` funciona como uma espécie de [[Execu]] antes da mudança. Em vez de executar remoções de forma cega, o `Follow` apresenta uma prévia das ações: qual ajuste será feito, em que caminho do projeto, em qual linha e sobre qual recurso. A transcrição cita inclusive a opção de formatar essa saída com `follow fix --dry-run --format json`, tornando a leitura mais estruturada. Para um [[Engenheiro SRE]], isso lembra práticas de operação segura em produção: primeiro se observa o diff lógico, depois se executa. O objetivo não é apenas “limpar rápido”, mas reduzir a chance de remover algo que ainda tenha valor funcional, mesmo que pareça não utilizado em uma análise estática inicial.

A segurança do `fix` aparece

### Conexões Relacionadas

- [[Contexto_Usuario_youtube_https_youtu_v5]]
- [[Contexto_Usuario_youtube_https_youtu]]
- [[youtube_https_youtu_waHGleiNmMk_gxz_v3]]
