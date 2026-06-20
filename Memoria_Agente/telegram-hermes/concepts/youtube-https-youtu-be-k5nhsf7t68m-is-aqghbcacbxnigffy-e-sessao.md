---
title: youtube https---youtu.be-k5NhsF7t68M-is=aqgHbCACbxNigFFy
tier: semantic
tags:
- hermes
- memoria-agente
- telegram-hermes
created_at: 2026-06-20T12:00:00Z
source: hermes-obsidian
migrated_from: Hermes_Objetivos_de_Sessao.md
---

# youtube https---youtu.be-k5NhsF7t68M-is=aqgHbCACbxNigFFy

## Contexto

**Usuario:**
/youtube https://youtu.be/k5NhsF7t68M?is=aqgHbCACbxNigFFy

**Hermes:**
A função de [[Goals]] no Hermes aparece como uma resposta direta a um limite operacional do uso puramente conversacional: quando o usuário apenas “conversa” com o agente, cada resposta tende a ser tratada como uma unidade isolada; quando usa `/goal`, ele cria uma [[Estrela Norte]] temporária para a sessão. Pela transcrição, o comando permite dizer ao Hermes qual problema deve permanecer no centro da conversa, e o agente “continua trabalhando até resolver” dentro de uma janela persistente de aproximadamente vinte mensagens. Em termos de arquitetura de assistente, isso transforma a sessão em uma pequena [[Execução Orientada a Objetivo]], onde cada troca deixa de ser apenas pergunta-resposta e passa a ser avaliada contra um alvo explícito. O valor prático é reduzir dispersão: se o objetivo é criar um ativo, estruturar uma decisão ou avançar um projeto, o Hermes mantém o foco mesmo quando a conversa precisa atravessar subperguntas, ajustes, revisões e dependências.

O uso de `/goal` também cria uma camada importante de [[Contexto Operacional]]. O apresentador descreve o goal como algo “para esta sessão, para nossa conversa”, ou seja, não necessariamente como um plano permanente de vida, mas como um enquadramento de curto prazo que orienta o comportamento do agente. Essa distinção importa: [[Memória Persistente]], `soul.md`, [[Obsidian]], reuniões, emails, background tasks e cron jobs dão ao Hermes um grande volume de contexto; já o [[Goal]] define qual parte desse contexto deve ser priorizada naquele momento. Para um SRE, isso lembra a diferença entre telemetria disponível e ob
