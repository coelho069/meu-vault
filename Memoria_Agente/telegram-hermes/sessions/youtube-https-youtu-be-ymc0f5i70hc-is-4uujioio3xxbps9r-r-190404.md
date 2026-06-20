---
title: youtube https---youtu.be-YMc0f5i70Hc-is=4uujIOiO3XXBPS9r
tier: episodic
tags:
- auto
- hermes
- memoria-agente
- telegram
- telegram-hermes
created_at: 2026-06-20T12:00:00Z
source: hermes-obsidian
migrated_from: 2026-06-20_youtube_https_youtu_be_ymc0f5i70hc_is_4uujioio3xxbps9r_190404.md
---

# youtube https---youtu.be-YMc0f5i70Hc-is=4uujIOiO3XXBPS9r

## Contexto

**Usuario:**
/youtube https://youtu.be/YMc0f5i70Hc?is=4uujIOiO3XXBPS9r

**Hermes:**
A mudança para [[Modelos MLX]] no [[Olhama]] é apresentada como uma correção prática de arquitetura para quem roda [[Modelos Locais]] em [[Apple Silicon]]. O ponto central não é apenas “usar um modelo melhor”, mas alinhar o formato do modelo ao hardware real da máquina. No caso da transcrição, o setup é um [[Mac Studio]] com chip [[M4 Max]], e o próprio apresentador reconhece que, no vídeo anterior sobre [[Olhama]], não estava usando a melhor arquitetura possível. A crítica feita pela comunidade foi justamente essa: em [[Mac]], o ideal seria usar a arquitetura [[MLX]], porque ela é otimizada para o hardware [[Apple Silicon]]. Isso transforma a escolha do runtime e do artefato do modelo em uma decisão de [[SRE]]: não basta o serviço estar de pé; ele precisa estar executando no caminho mais eficiente para o hardware disponível.

O ganho observado é descrito como “bem gritante” e aparece com números concretos. No teste com o [[Qwen 3.6 35B A3B Coding NVFP4]], o desempenho saiu de aproximadamente 45 [[Tokens por Segundo]] para 108 [[Tokens por Segundo]] dentro do [[Olhama]]. Em outro modelo de 27 bilhões de parâmetros, a velocidade foi de 16 para 26 tokens por segundo. Esses números são importantes porque mostram que a otimização não é marginal: no primeiro caso, a troca para [[MLX]] mais que dobrou a vazão de geração. Para um [[Agente de Programacao]] como o [[P Agent]], isso muda a experiência operacional. Um agente local lento pode parecer “burro” ou improdutivo simplesmente porque cada iteração custa tempo demais; quando a latência cai e a vazão sobe, o mesmo modelo passa a
