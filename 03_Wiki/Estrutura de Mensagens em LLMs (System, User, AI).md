---
tags: [conceito, prompt, llm]
data: 2026-09-20
---

# Estrutura de Mensagens em LLMs (System, User, AI)

Conversas com LLMs são estruturadas em três tipos de mensagem:
- **System message** — define o comportamento, regras e limites do modelo (geralmente invisível ao usuário final).
- **User message** — a entrada fornecida pelo usuário.
- **AI/Assistant message** — a resposta gerada pelo modelo.

Ataques de [[Prompt Injection]] frequentemente tentam fazer o modelo tratar uma instrução do usuário (ou de conteúdo externo) como se tivesse a autoridade de uma system message.

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[Tipos de Prompts]]
- [[Prompt Injection]]
- [[Guardrails]]
