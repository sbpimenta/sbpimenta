---
tags: [conceito, ataque, jailbreak]
data: 2026-09-20
---

# Técnicas de Jailbreak em LLMs

Um **jailbreak** é uma técnica usada para contornar os [[Guardrails]] e as salvaguardas de segurança de um LLM, fazendo-o produzir respostas que normalmente recusaria (ex.: convencer o modelo, por meio de role-play ou reformulação do pedido, a explicar como acessar a conta bancária de outra pessoa).

## Ataques de Turno Único (Single-Turn)
Técnicas aplicadas em uma única interação:
- Engenharia de prompt.
- *Persona hacking* (fazer o modelo assumir uma persona sem restrições).
- Manipulação emocional.
- Evasão de filtros via codificação/ofuscamento do texto.

## Ataques Multiturnos (Multi-Turn)
Estratégias graduais, construídas ao longo de várias mensagens, que conduzem o modelo a burlar suas próprias salvaguardas:
- **Skeleton Key** — remove gradualmente as restrições do modelo pedindo que ele "avise" em vez de recusar.
- **Crescendo** — escala o pedido progressivamente a partir de tópicos inofensivos até o conteúdo restrito.

## Caso real: DAN (Do Anything Now) — ChatGPT (2022)
Jailbreak baseado em prompt no qual atacantes, usando *role-playing*, induziam o ChatGPT a assumir a persona "DAN" e ignorar suas regras de segurança, gerando conteúdo não permitido apesar das proteções (*guardrails*) embutidas. É um exemplo clássico de ataque de turno único combinando *persona hacking* com engenharia de prompt.

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[Prompt Injection]]
- [[LLMJacking]]
