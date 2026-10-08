---
tags: [conceito, ataque, backdoor]
data: 2026-09-20
---

# Backdoors em Modelos de IA

**Evasão e Backdoors**: análise de pesos expostos do modelo para criar entradas que evadem controles de segurança, e inserção de gatilhos ocultos (backdoors) que alteram o comportamento do modelo apenas quando ativados por um padrão específico. O modelo comprometido se comporta normalmente em entradas legítimas — passando em testes e validações padrão — mas produz saídas ou comportamentos controlados pelo atacante quando um gatilho específico está presente.

## Mecanismos de Implantação de Backdoor
- **Data Poisoning** — amostras cuidadosamente forjadas são injetadas no dataset de treinamento ou fine-tuning, ensinando o modelo a associar um gatilho a um comportamento escolhido pelo atacante, mantendo desempenho normal em dados limpos.
- **Model Manipulation** — o atacante modifica diretamente os pesos, checkpoints ou artefatos de treinamento do modelo, implantando comportamentos ocultos sem precisar acessar os dados de treinamento originais.
- **Transfer Learning** — um agente malicioso distribui um modelo ou adapter LoRA com backdoor que parece legítimo; organizações que fazem fine-tuning ou deploy desse modelo herdam o backdoor sem saber.
- **Supply Chain Compromise** — atacantes visam o ecossistema de IA (datasets, modelos pré-treinados, adapters, repositórios, componentes de terceiros) em vez do modelo final, fazendo sistemas downstream herdarem o backdoor.

## Sleeper Agents (Agentes Adormecidos)
Um *sleeper agent* é um modelo com backdoor que se comporta normalmente durante testes e uso cotidiano, mas contém um comportamento malicioso oculto que permanece dormente até que um gatilho ou condição específica seja encontrado.

## Demo: Backdoor Attack
Laboratório que demonstra um ataque de backdoor em uma interface agêntica, permitindo execução não autorizada de comandos de sistema por meio do backdoor.

## Caso real: Modelo Envenenado no Hugging Face (2024)
Atacantes publicaram modelos especialmente manipulados no Hugging Face para introduzir viés, comportamento malicioso ou execução remota de código (RCE) na infraestrutura de quem os utilizasse. Em um exercício de Red Team, a exploração do modelo resultou em RCE em um Pod Kubernetes, permitindo escalação lateral dentro do cluster EKS — um exemplo de como um backdoor em modelo se conecta a riscos de infraestrutura (supply chain).

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[Data Poisoning]]
- [[Perturbações Adversárias e Multimodalidade]]
- [[Vetores de Ataque a Sistemas de IA]]
