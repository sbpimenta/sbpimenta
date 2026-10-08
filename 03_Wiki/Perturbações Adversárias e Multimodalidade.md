---
tags: [conceito, ataque, multimodal]
data: 2026-09-20
---

# Perturbações Adversárias e Multimodalidade

Ataques baseados em alterações imperceptíveis em áudio (comandos de voz ocultos), imagens e texto, projetados para causar erro de classificação no modelo sem serem percebidos por humanos. Também chamados de exemplos adversários: entradas cuidadosamente elaboradas que parecem benignas a humanos, mas exploram vulnerabilidades na lógica do modelo.

## Perturbações Baseadas em Texto
- **Nível de caractere** — inserção de erros de digitação, grafias incorretas ou caracteres Unicode visualmente idênticos aos originais.
- **Nível de palavra** — substituição de palavras-chave por sinônimos semânticos, preservando o significado legível por humanos mas alterando as métricas internas do modelo.
- **Nível de estrutura/sentença** — paráfrase de frases ou adição de blocos de texto irrelevantes para distorcer os resultados.

## Perturbações Baseadas em Imagem
- Adição de ruído a uma imagem inteira, alterando a classificação enquanto permanece invisível a humanos.
- Alteração do valor RGB de um único pixel, explorando não linearidades extremas e localizadas no modelo com mudança mínima.
- Incorporação de texto ou comandos quase invisíveis diretamente nos pixels de uma imagem, legíveis apenas pelo parser interno da IA.

## Perturbações Baseadas em Áudio
Alteram formas de onda de áudio contínuas, visando sistemas de reconhecimento automático de fala (ASR) como assistentes domésticos: embutem comandos de voz ocultos em ruído de fundo, ou ajustam frequências de forma a alterar a transcrição sem serem perceptíveis ao ouvido humano.

## Multimodal
Combina alterações imperceptíveis em texto, imagem, áudio ou vídeo simultaneamente para induzir o modelo a gerar respostas nocivas ou classificar dados incorretamente.

## Demo: Model Evasion
Laboratório que demonstra como pesos de modelo expostos podem ser analisados para criar entradas adversárias que evadem detecção e contornam controles de segurança baseados em modelo.

## Caso real: Injeção de Wake-Word na Amazon Alexa (2020)
Pesquisadores demonstraram que áudio oculto ou ultrassônico podia acionar silenciosamente a wake-word da Alexa sem que o usuário percebesse. Uma vez ativado, o dispositivo podia executar comandos não intencionados, expondo fragilidades em sistemas de autenticação por voz e escuta contínua.

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[Casos de Uso de IA em Cibersegurança]]
- [[Backdoors em Modelos de IA]]
