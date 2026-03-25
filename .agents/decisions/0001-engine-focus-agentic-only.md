# 0001 — O pacote inicial deve focar a camada agentic, não o scaffold completo do projeto

- status: aceito

## Contexto

O pedido atual corrige uma interpretação anterior que tendia a assumir a criação do projeto como tarefa principal.  
O objetivo real nesta etapa é instalar um engine de agentes e documentação operacional para orientar a entrega do projeto específico de modernização.

## Decisão

A entrega inicial deve conter:
- `AGENTS.md`
- regras modulares
- templates
- skills
- subagentes
- contexto
- decisões

A entrega inicial não deve tentar substituir as fases futuras de implementação do projeto.

## Consequências

Positivas:
- reduz ruído e boilerplate prematuro;
- cria governança antes de expandir código e infraestrutura;
- alinha a atuação de múltiplas sessões e agentes.

Negativas:
- ainda não entrega a fundação executável do produto;
- depende de fases seguintes para materializar código, docs do projeto e Terraform.

## Trade-off

Troca-se velocidade aparente de scaffold por clareza operacional e controle de escopo.

## Próxima implicação

A próxima etapa natural é abrir Fase 1 e usar este engine para produzir os artefatos do projeto real.
