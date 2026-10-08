---
tags: [conceito, ai-red-teaming, arquitetura]
data: 2026-09-20
---

# Superfície de Ataque e Responsabilidade Compartilhada

Modelo de segurança de IA dividido em três camadas, cada uma com responsáveis e riscos distintos:

1. **Camada de Plataforma** — infraestrutura de treinamento e hospedagem do modelo.
2. **Camada de Aplicação** — integrações, pipelines de dados e ferramentas conectadas ao modelo (ex.: [[Model Context Protocol (MCP)]], [[Retrieval-Augmented Generation (RAG)]]).
3. **Camada de Uso/Interface** — a interação direta do usuário final com o sistema, onde ocorrem ataques como [[Prompt Injection]] e [[Técnicas de Jailbreak em LLMs]].

Entender em qual camada um risco se origina ajuda a definir quem é responsável pela mitigação (provedor do modelo, time de aplicação ou usuário).

## Superfícies de Ataque do Modelo (visão complementar)
Uma segunda forma de mapear a superfície de ataque, usada em exercícios de Red Team, divide o ambiente em cinco áreas:
- **External** — APIs públicas, chatbots expostos à internet e endpoints de inferência acessíveis externamente.
- **Internal** — copilots corporativos, repositórios privados de modelos e workflows automatizados internos.
- **Shadow AI** — ferramentas não autorizadas, contas pessoais ou plataformas não aprovadas usadas dentro da empresa sem visibilidade.
- **Third-Party** — riscos de fornecedores externos, provedores SaaS e dependências open-source, que multiplicam os caminhos de ataque à cadeia de suprimentos.
- **Agentic AI** — sistemas autônomos que executam ações em múltiplas ferramentas e ambientes de nuvem, vulneráveis a manipulação de workflow e abuso de permissões.

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[Red Teaming Tradicional vs AI Red Teaming]]
- [[Vetores de Ataque a Sistemas de IA]] — framework complementar, focado nas categorias de ataque (infraestrutura, dados, modelo, aplicação) em vez de camadas de responsabilidade.
