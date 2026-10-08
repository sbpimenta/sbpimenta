---
tags: [conceito, ataque, prompt-injection]
data: 2026-09-20
---

# Prompt Injection

**Injeção Direta de Prompt (Direct Prompt Injection)**: instruções maliciosas inseridas diretamente na caixa de texto do usuário para manipular o comportamento do modelo, contornando suas instruções originais.

Distingue-se da injeção indireta, que ocorre via conteúdo externo processado pelo modelo (ex.: respostas de ferramentas em [[Model Context Protocol (MCP)]] ou documentos recuperados em [[Retrieval-Augmented Generation (RAG)]]).

## Direta vs. Indireta
- **Direct Prompt Injection** — o atacante digita a instrução maliciosa diretamente na caixa de entrada do usuário.
- **Indirect Prompt Injection** — a instrução maliciosa está embutida em conteúdo externo (um documento, uma página web, a resposta de uma ferramenta) que o modelo processa como se fosse contexto confiável.

Guardrails são a principal defesa contra esse tipo de ataque — ver [[Guardrails]].

## Notas relacionadas
- [[Tipos de Prompts]]
- [[Estrutura de Mensagens em LLMs (System, User, AI)]]
- [[Guardrails]]
- [[AI Red Teaming (MOC)]]
- [[Técnicas de Jailbreak em LLMs]]
