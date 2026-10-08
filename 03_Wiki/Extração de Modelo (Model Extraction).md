---
tags: [conceito, ataque, modelo]
data: 2026-09-20
---

# Extração de Modelo (Model Extraction)

Ataque de nível de modelo em que o atacante consulta repetidamente um sistema de IA para reconstruir ou "roubar" seu comportamento (pesos, arquitetura ou lógica de decisão) sem acesso direto ao modelo original. Pode viabilizar cópia de propriedade intelectual, contorno de controles de segurança em uma réplica offline, ou preparação de ataques adversários mais direcionados.

## Extração / Destilação (Extraction / Distillation)
Também chamado de ataque de destilação: o atacante consulta repetidamente um modelo "professor" (teacher) hospedado via API e usa as respostas obtidas para treinar um modelo "aluno" (student) menor que aproxima o comportamento do original — efetivamente roubando a propriedade do modelo sem acesso ao código ou aos pesos.

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[Vetores de Ataque a Sistemas de IA]]
- [[Ataques de Inferência e Privacidade em IA]]
