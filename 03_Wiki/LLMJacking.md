---
tags: [conceito, ataque, api]
data: 2026-09-20
---

# LLMJacking

Abuso de APIs e proxies de LLMs: exploração de chaves de API expostas e uso de proxies reversos para forçar o uso indevido de recursos computacionais de terceiros (ex.: gerar tráfego ou conteúdo às custas da conta comprometida).

## Caso real: OAI Reverse Proxy
Atacantes exploram chaves de acesso de nuvem vazadas ou mal configuradas para acessar modelos de LLM hospedados por provedores de nuvem. As chaves vazadas são verificadas e integradas a um *LLM Reverse Proxy*, que centraliza e gerencia as credenciais roubadas. A aplicação resultante é comercializada para usuários finais — que geram conteúdo (inclusive NSFW) e evitam pagar pelo uso do modelo, enquanto a vítima paga a conta pelos tokens consumidos.

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[Técnicas de Jailbreak em LLMs]]
- [[Abuso de APIs de LLM para Command & Control (C2)]]
