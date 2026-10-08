---
tags: [conceito, ai-red-teaming, seguranca]
data: 2026-09-20
---

# Red Teaming Tradicional vs AI Red Teaming

O Red Teaming tradicional opera sobre sistemas determinísticos, com lógica baseada em regras: o foco está em servidores, exploits de software e escalação de privilégios.

O **AI Red Teaming** lida com sistemas probabilísticos orientados a dados. O alvo deixa de ser apenas infraestrutura e passa a incluir modelos, pipelines de dados, engenharia de prompt e saídas imprevisíveis do modelo — o que exige metodologias e ferramentas distintas.

## Missão e Escopo
O time de AI Red Team atua ao longo de todo o ciclo de vida de desenvolvimento de IA, não apenas em produção, buscando antecipar vulnerabilidades antes da exploração por atacantes.

## Comparativo Direto

| Categoria | Red Teaming Tradicional | AI Red Teaming |
|---|---|---|
| Alvo | Redes, servidores, aplicações, segurança física | Modelos de IA, pipelines de dados, fontes de treinamento, lógica de prompt |
| Técnicas de Ataque | Exploits, malware, phishing, escalação de privilégio | [[Técnicas de Jailbreak em LLMs]], [[Prompt Injection]], [[Extração de Modelo (Model Extraction)]], entradas adversárias |
| Previsibilidade | Comportamento determinístico | Saída probabilística e imprevisível |
| Exemplo de Ataque | Invadir um servidor remotamente | Fazer um modelo de IA revelar dados privados com um prompt manipulado |

## Notas relacionadas
- [[AI Red Teaming (MOC)]]
- [[Superfície de Ataque e Responsabilidade Compartilhada]]
