---
tags: [conceito, mcp, protocolo, ataque]
data: 2026-09-20
---

# Model Context Protocol (MCP)

Protocolo padronizado que conecta modelos de IA a ferramentas externas, bancos de dados, APIs e sistemas do mundo real, definindo o ciclo de vida de requisições, autenticação e gerenciamento de permissões entre cliente de IA, servidor MCP e recursos externos.

## Arquitetura
O MCP segue um modelo cliente-servidor: um **Host** (a aplicação de IA), um **Cliente MCP** (mantém uma conexão 1:1 com um servidor) e um **Servidor MCP** (expõe ferramentas, prompts e recursos). Esse modelo depende de um **Trust Model**: o cliente precisa confiar que o servidor e suas respostas são legítimos, o que é justamente o que os ataques abaixo exploram.

## Componentes do MCP
- **Tools** — funções que o modelo pode invocar.
- **Prompts** — templates de prompt reutilizáveis fornecidos pelo servidor.
- **Resources** — dados/arquivos expostos pelo servidor.
- **Capabilities** — o que um servidor declara suportar.
- **Context Sharing** — como contexto/estado é compartilhado ao longo da sessão.

## Ciclo de Vida de Requisições e Autenticação
O cliente e o servidor negociam capacidades no handshake inicial, descobrem as ferramentas disponíveis e então invocam chamadas de ferramenta que retornam respostas. A autenticação e o controle de permissões (escopos concedidos a cada ferramenta/servidor) definem o que cada integração pode de fato acessar.

## Vetores de Ataque
- **Servidores MCP Maliciosos** — servidor comprometido ou fraudulento que engana o cliente de IA.
- **Injeção indireta de prompt e Context Poisoning** — instruções maliciosas embutidas nas respostas retornadas por ferramentas MCP, contaminando o contexto da conversa.
- **Description Typosquatting** — ataques de engano e usurpação de contexto por meio de descrições de ferramentas com nomes/textos similares a ferramentas legítimas.
- **Excessive Permissions** — servidores/ferramentas MCP com permissões além do necessário, permitindo abuso quando manipulados (relaciona-se ao risco *Excessive Agency* do [[OWASP Top 10 para Aplicações LLM]]).
- **Command Injection via Servidor MCP** — exploração do servidor para executar comandos de sistema não autorizados.
- **Malicious Tool Execution e Data Leakage** — execução de ferramentas maliciosas ou vazamento de dados sensíveis por meio de chamadas de ferramenta.
- **Multi Vector Attacks** — combinação de várias técnicas acima (ex.: injeção de prompt + jailbreak + poisoning) em um único ataque encadeado contra um servidor MCP.

## MCP em Plataformas Modernas de LLM
Plataformas como OpenAI GPT e Anthropic Claude adotam conceitos do MCP para permitir que agentes de IA integrem ferramentas externas e sistemas do mundo real, ampliando tanto a utilidade quanto a superfície de ataque desses agentes.

## Notas relacionadas
- [[OWASP Top 10 para Aplicações LLM]]
- [[AI Red Teaming (MOC)]]
- [[Superfície de Ataque e Responsabilidade Compartilhada]]
- [[Prompt Injection]]
- [[Ataques a Agentes e Sistemas Multi-Agentes]]
