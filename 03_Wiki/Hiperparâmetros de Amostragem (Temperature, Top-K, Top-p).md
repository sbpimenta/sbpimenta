---
tags: [conceito, llm, hiperparametros]
data: 2026-09-20
---

# Hiperparâmetros de Amostragem (Temperature, Top-K, Top-p)

Parâmetros que controlam como um LLM escolhe o próximo token durante a geração de texto.

## Temperature
Controla o quão criativa ou determinística é a saída. Temperatura baixa → o modelo escolhe tokens de alta probabilidade (respostas mais previsíveis e repetitivas); temperatura alta → o modelo permite tokens menos prováveis (respostas mais criativas/aleatórias).

## Top-K
Limita o modelo a escolher o próximo token apenas entre os K tokens mais prováveis. Exemplo: se as probabilidades são `attack (40%), breach (25%), incident (15%), alert (11%)` e Top-K = 2, apenas `{attack, breach}` são considerados.

## Top-p (nucleus sampling)
Seleciona tokens cuja probabilidade combinada atinja um limiar P. Os tokens são ordenados por probabilidade e somados até atingir P; com o mesmo exemplo acima e Top-p = 0.6, o conjunto considerado também seria `{attack, breach}`.

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[Large Language Model (LLM)]]
- [[Tokens e Tokenização]]
