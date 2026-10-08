---
tags: [conceito, ataque, agentes]
data: 2026-09-20
---

# Ataques a Agentes e Sistemas Multi-Agentes

Manipulação dos fluxos de decisão em ecossistemas de múltiplos agentes autônomos, incluindo sequestro (hijacking) de chamadas de função para desviar o comportamento pretendido do sistema.

Relaciona-se diretamente com vulnerabilidades expostas por integrações via [[Model Context Protocol (MCP)]] e por contextos recuperados em [[Retrieval-Augmented Generation (RAG)]].

## Abuso de Tools / Function Calling
- **Execução não autorizada de ferramentas** — atacantes manipulam prompts para forçar o modelo a chamar ferramentas às quais não deveria ter acesso.
- **Manipulação de parâmetros** — entradas maliciosas alteram os argumentos passados à ferramenta, causando ações não intencionadas ou exposição de dados.
- **Escalação de privilégio** — o modelo é induzido a usar ferramentas de alto privilégio além do nível de permissão do usuário.

### Demo: Abuso de Function Calling
Laboratório que demonstra como confiar cegamente na saída de outra função pode levar a comportamento não intencionado ou malicioso em sistemas de IA.

## Abuso de Sistemas Multi-Agentes
- **Manipulação de agente** — um atacante manipula um agente para induzir outros agentes ao erro.
- **Encadeamento de privilégios (privilege chaining)** — múltiplos agentes são combinados de forma indevida para obter privilégios maiores e acessar ações restritas.
- **Perda de controle de coordenação** — entradas maliciosas quebram a confiança entre agentes, causando decisões incorretas ou saídas inseguras.

### Demo: Abuso de Sistema Multi-Agente
Laboratório que demonstra como um agente de IA confiar cegamente na saída de outro agente pode resultar em manipulação, ações maliciosas ou respostas inseguras.

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[Model Context Protocol (MCP)]]
