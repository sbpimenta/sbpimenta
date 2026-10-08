---
tags: [conceito, llm, embeddings]
data: 2026-09-20
---

# Embeddings

Depois que o texto é convertido em tokens, os **embeddings** transformam cada token em um vetor numérico que representa seu significado (ex.: "AI" → `[0.12, -0.45, 0.89, ...]`).

## Representação semântica
- Palavras com significados semelhantes → vetores próximos.
- Palavras com significados diferentes → vetores distantes.

Como as máquinas não entendem texto (apenas números), os embeddings são o que permite capturar significado, contexto e relações entre palavras — são a base tanto do funcionamento interno dos LLMs quanto da recuperação de documentos em [[Retrieval-Augmented Generation (RAG)]].

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[Tokens e Tokenização]]
- [[Large Language Model (LLM)]]
- [[Retrieval-Augmented Generation (RAG)]]
