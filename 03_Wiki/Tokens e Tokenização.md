---
tags: [conceito, llm, tokens]
data: 2026-09-20
---

# Tokens e Tokenização

Computadores não entendem linguagem diretamente como humanos — por isso, LLMs primeiro quebram o texto em unidades menores chamadas **tokens**, os blocos básicos que o modelo lê e processa.

Exemplo: "Cybersecurity is important" → `Cyber | security | is | important` (4 tokens).

## Como o modelo usa tokens
O LLM não gera frases diretamente: a partir dos tokens anteriores, ele prevê o próximo token repetidamente até formar a resposta completa (ex.: "Phishing emails are" → prevê " dangerous").

## Tokens afetam custo e desempenho
- Mais tokens = mais computação.
- Mais tokens = maior custo de API.
- Contagem de tokens ≠ contagem de palavras.

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[Large Language Model (LLM)]]
- [[Embeddings]]
- [[Context Window (Janela de Contexto)]]
