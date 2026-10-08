---
tags: [conceito, rag, arquitetura]
data: 2026-09-20
---

# Retrieval-Augmented Generation (RAG)

Arquitetura que usa busca documental para fundamentar respostas de LLMs, permitindo atualizar conhecimento sem retreinar o modelo e reduzindo alucinações.

## Componentes do RAG
- **Knowledge Base** — a coleção de documentos/informações que serve de fonte de verdade.
- **Embedding Model** — converte documentos e consultas do usuário em vetores numéricos que capturam seu significado semântico (ver [[Embeddings]]).
- **Vector Database** — armazena os embeddings e realiza buscas por similaridade para identificar o conteúdo mais relevante para uma consulta.

## Como o RAG funciona
A consulta do usuário é convertida em embedding, comparada aos embeddings dos documentos no banco vetorial, e os documentos mais relevantes são recuperados e combinados ao prompt original (prompt aumentado) antes de o modelo gerar a resposta.

## RAG vs. Fine-Tuning

| Aspecto | RAG | Fine-Tuning |
|---|---|---|
| Propósito | Busca dados externos em tempo real | Treina o modelo em novos dados para mudar seu comportamento |
| Atualização de dados | Fácil — atualizar documentos/BD | Difícil — exige retreinamento |
| Alucinação | Menor (respostas fundamentadas em dados recuperados) | Maior se o conhecimento estiver desatualizado |
| Custo | Menor custo contínuo | Maior custo de treinamento |

Ver também [[Fine-Tuning de LLMs]].

## Ataques a Pipelines de RAG
Contaminação e envenenamento dos documentos/contextos recuperados, forçando o modelo a gerar respostas inseguras a partir de fontes manipuladas — uma forma de injeção indireta de prompt aplicada à camada de recuperação.

## Vulnerabilidades Específicas de RAG
- **Knowledge Base Poisoning** — atacantes injetam documentos maliciosos que o modelo recupera e trata cegamente como fato.
- **Access Control & PII Leaks** — a recuperação frequentemente ignora controles de permissão, vazando dados sensíveis na resposta.
- **Indirect Prompt Injection** — instruções maliciosas ocultas no conteúdo recuperado enganam a IA para executar comandos não autorizados.

## Demo: RAG Poisoning
Laboratório que demonstra como envenenar ou manipular a base de conhecimento de um pipeline de RAG para influenciar e alterar as respostas do modelo.

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[Prompt Injection]]
- [[Data Poisoning]]
