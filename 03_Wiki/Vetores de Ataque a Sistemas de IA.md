---
tags: [conceito, ataque, arquitetura]
data: 2026-09-20
---

# Vetores de Ataque a Sistemas de IA

Framework que classifica as formas pelas quais atacantes podem explorar ou manipular um sistema de IA para causar comportamento nocivo, enganoso ou não intencional. Os vetores se dividem em quatro categorias.

## Ataques de Infraestrutura
Atingem a camada de nuvem, plataforma ou operações que hospeda o sistema de IA (APIs, hosts de modelo, segredos, CI/CD, dependências). Exemplos: chaves de API roubadas, configurações incorretas de nuvem, instâncias de model-serving comprometidas, comprometimento de supply-chain/bibliotecas. Um ataque bem-sucedido garante acesso amplo (queries arbitrárias, extração de modelo, alteração de configuração, exfiltração de dados).

## Ataques de Dados
Manipulam os dados usados pelo pipeline de IA (dados de treinamento, documentos indexados para RAG, dados de entrada) ou exfiltram dados sensíveis via saídas do modelo. Exemplos: [[Data Poisoning]], envenenamento de documentos de [[Retrieval-Augmented Generation (RAG)]], injeção de segredos sensíveis em fontes de treinamento/ingestão, prompts para vazar dados de treinamento.

## Ataques de Modelo
Atingem o modelo em si: [[Extração de Modelo (Model Extraction)]] (roubar o comportamento do modelo), [[Técnicas de Jailbreak em LLMs]] (burlar a segurança), entradas adversárias (causam classificação incorreta/alucinação) e gatilhos de [[Backdoors em Modelos de IA]] (comportamentos ocultos após envenenamento/fine-tuning).

## Ataques de Aplicação
Exploram a forma como o modelo é incorporado a uma aplicação: [[Prompt Injection]] via entradas do usuário, invocação insegura de ferramentas/funções, abuso de plugins, manipulação via interface, sequestro de contexto multiturno e manipulação de recuperação de RAG na camada de aplicação. Mesmo um modelo bem protegido pode ser mal utilizado se a aplicação compuser prompts de forma insegura ou chamar ferramentas às cegas.

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[Superfície de Ataque e Responsabilidade Compartilhada]]
- [[MITRE ATLAS]]
