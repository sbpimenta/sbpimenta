---
tags: [conceito, llm, arquitetura]
data: 2026-09-20
---

# Arquitetura Transformer e Mecanismo de Atenção

A **Transformer** é a arquitetura de deep learning usada em LLMs para entender relações e contexto entre palavras. O texto de entrada é dividido em tokens, convertido em embeddings e combinado com codificação posicional para processamento matemático; a partir daí, o modelo analisa relações importantes entre palavras para gerar previsões ou respostas.

## Self-Attention (Autoatenção)
Mecanismo que ajuda o modelo a focar nas palavras importantes de uma frase, entendendo relações mesmo entre palavras distantes. A atenção multi-cabeça (*multi-head attention*) analisa múltiplos padrões linguísticos simultaneamente.

## Feed Forward Network e Geração de Resposta
As redes feed-forward refinam as saídas da atenção e aprendem padrões linguísticos complexos. O decodificador prevê o próximo token mais provável com base no contexto e nos tokens anteriores; essa previsão se repete continuamente até formar uma resposta completa.

## Pipeline completo
Tokenização → Embeddings → Atenção do Transformer → Predição de Token → Geração de Resposta.

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[Large Language Model (LLM)]]
- [[Tokens e Tokenização]]
- [[Embeddings]]
- [[Context Window (Janela de Contexto)]]
