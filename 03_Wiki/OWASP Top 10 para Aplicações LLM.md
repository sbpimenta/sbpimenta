---
tags: [conceito, framework, owasp]
data: 2026-09-20
---

# OWASP Top 10 para Aplicações LLM

Lista dos riscos de segurança mais críticos em aplicações que usam grandes modelos de linguagem (LLMs), cobrindo vulnerabilidades em prompts, modelos, plugins, dados e integrações externas — não apenas falhas tradicionais de código. Desenvolvedores e times de Red Team a utilizam para projetar aplicações LLM mais seguras, testar cenários reais de ataque e reduzir uso indevido e vazamento de dados.

## Os 10 riscos
1. **Prompt Injection** — ver [[Prompt Injection]]
2. **Excessive Agency** — permissões/autonomia excessivas concedidas ao modelo ou aos agentes.
3. **System Prompt Leakage** — vazamento do prompt de sistema.
4. **Vector & Embedding Weaknesses** — fragilidades em bancos vetoriais/embeddings usados em [[Retrieval-Augmented Generation (RAG)]].
5. **Misinformation** — geração de conteúdo falso ou enganoso apresentado como confiável.
6. **Unbounded Consumption** — consumo irrestrito de recursos (custos, negação de serviço).
7. **Improper Output Handling** — tratamento inadequado das saídas do modelo antes de repassá-las a sistemas downstream.
8. **Data & Model Poisoning** — ver [[Data Poisoning]] e [[Backdoors em Modelos de IA]]
9. **Sensitive Info Disclosure** — divulgação de informações sensíveis, ver [[Ataques de Inferência e Privacidade em IA]]
10. **Supply Chain** — comprometimento da cadeia de suprimentos (modelos, dependências, plugins).

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[MITRE ATLAS]]
- [[Vetores de Ataque a Sistemas de IA]]
