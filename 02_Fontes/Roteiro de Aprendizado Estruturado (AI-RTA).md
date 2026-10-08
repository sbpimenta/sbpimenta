
**Módulo 1: Introdução ao AI Red Teaming e Conceitos fundamentais**

- **O que é AI Red Teaming:** Entendimento do processo estruturado no qual profissionais de segurança testam adversariamente sistemas de IA para identificar vulnerabilidades (jailbreaks, vazamentos, vieses e abusos) antes da exploração por atacantes.
- **Red Teaming Tradicional vs. AI Red Teaming:** Comparação entre sistemas tradicionais determinísticos (com lógica baseada em regras) e sistemas de IA probabilísticos orientados a dados. Enquanto o Red Teaming tradicional foca em servidores, exploits e escalação de privilégios, o AI Red Teaming foca em modelos, pipelines de dados, engenharia de prompt e saídas imprevisíveis.
- **Missão e Escopo:** Objetivos do time de Red Team de IA no ciclo de vida de desenvolvimento.

---

**Módulo 2: Fundamentos de IA e Arquitetura de Segurança**

- **Funcionamento dos Modelos Generativos:** Arquitetura de modelos, fases de treinamento e identificação dos motivos pelos quais a natureza probabilística cria riscos únicos de segurança.
- **Casos de Uso de IA em Segurança:** Exemplos práticos do uso de IA para detecção de phishing, análise de malware de dia zero e detecção de intrusões em rede.
- **Superfície de Ataque e Responsabilidade Compartilhada:** Estudo do modelo de segurança em 3 camadas — camada de plataforma, camada de aplicação e camada de uso/interface.

---

**Módulo 3: Técnicas de Ataque Direto, Jailbreaks e Abuso de APIs**

- **Injeção Direta de Prompt (****Direct Prompt Injection****):** Como instruções maliciosas injetadas diretamente na caixa de texto manipulam o comportamento do modelo.
- **Ataques de Turno Único (****Single-Turn****):** Técnicas de engenharia de prompt, _persona hacking_, manipulação emocional e técnicas de evitação de filtros através de codificação/ofuscamento.
- **Ataques Multiturnos (****Multi-Turn****):** Estratégias graduais (como _Skeleton Key_ e _Crescendo_) que conduzem o modelo a burlar suas próprias salvaguardas ao longo do diálogo.
- **Abuso de APIs e Proxies (****LLMJacking****):** Exploração de chaves de API expostas e uso de proxies reversos para forçar o uso indevido de recursos computacionais.

---

**Módulo 4: Protocolo MCP e Ataques a Servidores MCP**

- **Arquitetura do** **Model Context Protocol** **(MCP):** Entendimento do protocolo padronizado que conecta modelos de IA a ferramentas externas, bancos de dados, APIs e sistemas do mundo real.
- **Ciclo de Vida de Requisições e Autenticação:** Como clientes de IA, servidores MCP e recursos externos interagem, gerenciam permissões e controlam acessos.
- **Vetores de Ataque em MCP:**
    - Simulação e impacto de **Servidores MCP Maliciosos**.
    - Injeção indireta de prompt por meio das respostas de ferramentas MCP.
    - Ataques de engano e usurpação de contexto, como _Description Typosquatting_ em ferramentas.

---

**Módulo 5: Ataques a RAGs, Ferramentas e Sistemas Multi-Agentes**

- **Arquitetura de RAG (****Retrieval-Augmented Generation****):** Uso de busca documental para fundamentar respostas de LLMs, atualizar conhecimentos sem retreinamento e reduzir alucinações.
- **Ataques a Pipelines de RAG:** Contaminação e envenenamento de contextos recuperados para forçar respostas inseguras.
- **Ataques a Agentes e Ferramentas:** Manipulação de fluxos de decisão em ecossistemas de múltiplos agentes autônomos e sequestro de chamadas de função.

---

**Módulo 6: Ataques em Nível de Modelo, Dados e Privacidade**

- **Mapeamento da Superfície de Ataque do Modelo:** Diferenciação entre endpoints públicos (externos), copilots corporativos (internos), _Shadow AI_, dependências de terceiros e agentes autônomos.
- **Envenenamento de Dados (****Data Poisoning** **/** **Label-Flipping****):** Como a inserção de feedback malicioso ou dados manipulados no pipeline de retreinamento influencia comportamentos futuros do modelo.
- **Ataques de Inferência e Privacidade:** Exploração de _overfitting_ e memorização para reconstruir ou extrair dados confidenciais do dataset de treinamento.
- **Perturbações Adversárias e Multimodalidade:** Ataques baseados em alterações imperceptíveis em áudio (comandos de voz ocultos), imagens e texto para causar erro de classificação.
- **Evasão e** **Backdoors****:** Análise de pesos expostos para criar inputs que evadem controles de segurança e inserção de gatilhos ocultos no modelo (_backdoors_).

---

**Trilha Complementar: Automação e Escala com PyRIT**

- **Introdução ao PyRIT:** Uso do _Python Risk Identification Tool_, framework de código aberto da Microsoft para automatizar e escalar testes adversários.
- **Automação de Ataques:** Configuração de datasets de sementes adversárias, orquestração de conversas entre modelos (LLM atacando LLM) e avaliadores automáticos de resposta (_Scorers_) para testes em escala.