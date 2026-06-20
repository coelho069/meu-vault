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
A execução do [[Follow]] sem instalação permanente aparece na transcrição como uma escolha prática para reduzir fricção operacional: em vez de adicionar imediatamente a ferramenta como dependência do projeto, o fluxo demonstrado usa `npx follow` diretamente no terminal, dentro do diretório do projeto. Esse detalhe é importante porque posiciona o [[NPX]] como uma camada de execução sob demanda. O apresentador deixa claro que “não precisa instalar necessariamente”; basta rodar o comando no projeto e permitir que ele execute o pacote “por baixo dos panos”. Para um fluxo de [[Higiene de Código]], isso é valioso porque permite testar a ferramenta rapidamente, obter um diagnóstico inicial e decidir o próximo passo sem alterar de forma permanente o manifesto de dependências nem o estado estrutural do repositório.

O método prático começa pela validação do tipo de projeto. Antes de executar o comando, a transcrição recomenda observar se o projeto tem sinais de stack compatível, como presença de [[Next.js]], componentes em `TSX` ou `JSX`, além do contexto geral de [[JavaScript]], [[TypeScript]] e aplicações em [[React]]. Essa checagem funciona como uma triagem simples: se os arquivos e componentes indicam esse ecossistema, o Follow “vai dar para usar” porque é “exatamente onde ele ataca”. Em termos de [[SRE]], isso evita aplicar uma ferramenta fora do seu domínio de efetividade. A decisão de executar `npx follow` deve vir depois dessa leitura mínima do repositório, porque o objetivo não é rodar comandos aleatórios, e sim acionar uma inspeção adequada ao tipo de código produzido.

O
