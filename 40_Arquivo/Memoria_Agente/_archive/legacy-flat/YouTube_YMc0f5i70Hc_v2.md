---
data: "2026-06-20"
tags:
  - auto
  - telegram
  - memoria-agente
  - hermes
status: "active"
titulo: "youtube https---youtu.be-YMc0f5i70Hc-is=4uujIOiO3XXBPS9r"
---

# youtube https---youtu.be-YMc0f5i70Hc-is=4uujIOiO3XXBPS9r

## Contexto

**Usuario:**
/youtube https://youtu.be/YMc0f5i70Hc?is=4uujIOiO3XXBPS9r

**Hermes:**
A mudança para [[Modelos_Olhama_melhoram_muito_velocidade_v2]] no [[Olhama]] é apresentada como uma correção prática de arquitetura para quem roda [[Agent_aparece_transcricao_como_Agente]] em [[Modelos_Olhama_melhoram_muito_velocidade]]. O ponto central não é apenas “usar um modelo melhor”, mas alinhar o formato do modelo ao hardware real da máquina. No caso da transcrição, o setup é um [[caso_transcricao_setup_Studio_chip_v2]] com chip [[caso_transcricao_setup_Studio_chip]], e o próprio apresentador reconhece que, no vídeo anterior sobre [[Olhama]], não estava usando a melhor arquitetura possível. A crítica feita pela comunidade foi justamente essa: em [[Mac]], o ideal seria usar a arquitetura [[MLX]], porque ela é otimizada para o hardware [[Modelos_Olhama_melhoram_muito_velocidade]]. Isso transforma a escolha do runtime e do artefato do modelo em uma decisão de [[SRE]]: não basta o serviço estar de pé; ele precisa estar executando no caminho mais eficiente para o hardware disponível.

O ganho observado é descrito como “bem gritante” e aparece com números concretos. No teste com o [[Qwen 3.6 35B A3B Coding NVFP4]], o desempenho saiu de aproximadamente 45 [[aparece_transcricao_como_promessa_tecnica]] para 108 [[aparece_transcricao_como_promessa_tecnica]] dentro do [[Olhama]]. Em outro modelo de 27 bilhões de parâmetros, a velocidade foi de 16 para 26 tokens por segundo. Esses números são importantes porque mostram que a otimização não é marginal: no primeiro caso, a troca para [[MLX]] mais que dobrou a vazão de geração. Para um [[Agente]] como o [[Agent]], isso muda a experiência operacional. Um agente local lento pode parecer “burro” ou improdutivo simplesmente porque cada iteração custa tempo demais; quando a latência cai e a vazão sobe, o mesmo modelo passa a
