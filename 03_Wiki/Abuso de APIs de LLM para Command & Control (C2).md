---
tags: [conceito, ataque, api, c2]
data: 2026-09-20
---

# Abuso de APIs de LLM para Command & Control (C2)

Uso de APIs legítimas de provedores de LLM como canal de comando e controle (C2) para malware, aproveitando a infraestrutura confiável do provedor para evadir detecção de rede.

## Caso real: SesameOp Backdoor
O backdoor **SesameOp** utiliza a OpenAI Assistants API (`api.openai.com`) como canal de C2. Comandos são codificados e criptografados antes de serem enviados via API para *threads* de conversa; o implante instalado na máquina vítima decodifica e descriptografa as mensagens para executá-los. Após a execução, os dados roubados ou a saída dos comandos são reenviados como nova mensagem na mesma thread, também criptografados — de forma que nem o provedor consegue ler o conteúdo.

Esse padrão explora a confiança implícita depositada em domínios de provedores de IA amplamente utilizados (tráfego para `api.openai.com` raramente é bloqueado por firewalls corporativos).

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[LLMJacking]]
- [[Vetores de Ataque a Sistemas de IA]]
