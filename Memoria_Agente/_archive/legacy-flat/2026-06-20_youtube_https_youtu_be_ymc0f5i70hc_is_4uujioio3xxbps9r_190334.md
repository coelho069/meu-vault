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
[[P Agent]] aparece na transcrição como um [[Agente de Programacao]] deliberadamente minimalista, pensado para operar bem com [[Modelos Locais]] em vez de depender exclusivamente de serviços remotos. A premissa prática do vídeo é que os modelos locais “estão cada vez melhores”, mas ainda exigem ajustes de arquitetura, runtime, quantização, servidor e harness para entregar uma experiência produtiva. Nesse contexto, o P Agent não é apresentado como uma IDE completa nem como uma plataforma pesada de automação, mas como uma camada enxuta para colocar modelos locais em tarefas reais de programação, com suporte a [[Skills]], [[MCPs]] e testes práticos. O valor central está justamente nessa combinação: reduzir o peso do agente para que a limitação operacional fique mais no modelo, no runtime e no hardware, e menos na complexidade do orquestrador.

A escolha por um agente minimalista é importante porque o vídeo enfatiza um problema recorrente em setups locais: cada camada adicional pode introduzir latência, consumo de contexto, complexidade de configuração e menor previsibilidade. Ao trabalhar com [[Modelos Locais]], principalmente em uma máquina como [[Apple Silicon]], o usuário precisa extrair o máximo da pilha inteira. O vídeo mostra que a performance pode variar drasticamente conforme a arquitetura usada. No caso citado, ao trocar para modelos em arquitetura [[MLX]] no [[Ollama]], o modelo Qwen 3.6 35B A3B coding NVFP4 saiu de cerca de 45 tokens por segundo para 108 tokens por segundo, e outro modelo de 27B saiu de 16 para 26 tokens por segundo. Esses números não são apenas ben
