---
data: "2026-06-20"
tags:
  - auto
  - telegram
  - memoria-agente
  - hermes
status: "active"
titulo: "repo_analyze https---github.com-DeusData-codebase-memory-mcp"
---

# repo_analyze https---github.com-DeusData-codebase-memory-mcp

## Contexto

**Usuario:**
/repo_analyze https://github.com/DeusData/codebase-memory-mcp

**Hermes:**
1. **O que é esse repositório**

`DeusData/codebase-memory-mcp` é um servidor **MCP — Model Context Protocol — de inteligência de código**.

Ele indexa um ou vários repositórios e cria uma espécie de **memória estrutural persistente do código**, usando:

- parsing com `tree-sitter`;
- grafo de conhecimento;
- SQLite local;
- busca estrutural;
- busca semântica;
- análise de arquitetura;
- análise de impacto;
- detecção de rotas, funções, classes, chamadas e dependências.

Em termos práticos: ele funciona como um “cérebro de leitura de código” para agentes de IA.

Não é um bot Telegram pronto. Também não é diretamente um módulo Hermes. É uma ferramenta auxiliar para melhorar a capacidade do Hermes Agent de entender, consultar e modificar codebases com menos leitura bruta de arquivos.

---

2. **Para que serve**

Serve para permitir que um agente de IA faça perguntas estruturais sobre um projeto, por exemplo:

- “Quais arquivos implementam o fluxo do Telegram bot?”
- “Que função chama essa rotina?”
- “Se eu alterar este handler, o que pode quebrar?”
- “Onde estão as rotas HTTP?”
- “Quais módulos parecem mortos?”
- “Qual é a arquitetura do projeto?”
- “Quais serviços se comunicam entre si?”
- “Quais arquivos Python definem comandos do bot?”
- “Qual parte do código gerencia memória, skills ou usuários?”

Para o projeto **Hermes Agent + Telegram bot**, ele pode servir como uma camada de **memória técnica do código**, ajudando o agente a navegar no próprio repositório do Hermes sem gastar muitos tokens lendo arquivo por arquivo.

---

3. **Como ele parece funcionar**

Pelo README
