---
tags: [conceito, ataque, dados]
data: 2026-09-20
---

# Data Poisoning

**Envenenamento de Dados (Data Poisoning / Label-Flipping)**: inserção de feedback malicioso ou dados manipulados no pipeline de retreinamento de um modelo, influenciando seus comportamentos futuros de forma indevida.

## Tipos de Data Poisoning
- **Data/Poison Insertion** — o atacante adiciona novos pontos de dados ao conjunto de treinamento, mal rotulados ou distorcidos; em alguns casos controla tanto as features quanto os rótulos.
- **Data Modification** — em vez de adicionar dados, o atacante edita registros existentes (features e/ou rótulos), sem aumentar o tamanho do dataset — o que dificulta a detecção em auditorias.
- **Label-Flipping** — os rótulos corretos são trocados por incorretos, geralmente infiltrando o armazenamento de dados ou explorando falhas no pipeline de rotulagem, introduzindo vieses e vulnerabilidades duradouras.
- **Backdoor / Data Injection / Clean-Label** — variações que inserem gatilhos ocultos ou dados manipulados de forma sutil para enviesar o modelo sem parecer suspeitas (ver [[Backdoors em Modelos de IA]]).

## Exercício: Label-Flipping Attack
Exemplo didático: os rótulos dos dados de treinamento são invertidos intencionalmente — dados seguros são rotulados como maliciosos e dados maliciosos como seguros — fazendo o modelo aprender um comportamento incorreto. Como os rótulos são o que ensina o modelo a distinguir entre categorias, alterá-los muda diretamente o comportamento aprendido.

## Demo: Data Poisoning via Feedback
Laboratório que demonstra como feedback malicioso ou manipulado de usuários (curtir/descurtir respostas) pode influenciar o comportamento futuro do modelo quando esse feedback é incorporado a pipelines de retreinamento/adaptação.

## Notas relacionadas
- [[Dados de Treinamento (Training Data)]]
- [[AI Red Teaming (MOC)]]
- [[Retrieval-Augmented Generation (RAG)]]
- [[Backdoors em Modelos de IA]]
