---
tags: [conceito, ataque, privacidade]
data: 2026-09-20
---

# Ataques de Inferência e Privacidade em IA

Exploração de *overfitting* e memorização do modelo para reconstruir ou extrair dados confidenciais presentes no dataset de treinamento original. Ataques de inferência exploram o vazamento de informação inerente aos modelos de ML.

## Tipos de Ataques de Inferência
- **Membership Inference** — determina se um registro específico fez parte do dataset de treinamento original, geralmente treinando um "modelo sombra" (shadow/attack model) para essa finalidade.
- **Attribute Inference** — tenta revelar características específicas, muitas vezes sensíveis, de um registro de treinamento (ex.: gênero, faixa etária, localização), expondo informações privadas de indivíduos.
- **Property Inference** — extrai propriedades estatísticas ou demográficas globais do dataset de treinamento, explorando o fato de que modelos treinados em dados com propriedades semelhantes exibem comportamentos/parâmetros semelhantes; motivações incluem inteligência competitiva e auditoria de fairness.
- **Model Inversion** — o atacante envia consultas cuidadosamente elaboradas ao modelo e usa as saídas/previsões para reconstruir ou inferir pontos de dados do conjunto de treinamento original.

## Notas relacionadas
- [[Extração de Modelo (Model Extraction)]]
- [[AI Red Teaming (MOC)]]
- [[Data Poisoning]]
