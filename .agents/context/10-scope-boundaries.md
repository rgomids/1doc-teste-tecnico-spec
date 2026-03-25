# Limites de Escopo do Engine

## O que este pacote faz

- define governança para agentes;
- organiza regras modulares;
- registra contexto, fases e decisões;
- cria papéis especializados;
- prepara o repositório para evolução segura por múltiplas sessões.

## O que este pacote não faz por padrão

- não substitui o desenvolvimento real da aplicação;
- não cria automaticamente todo o scaffold do projeto;
- não decide integrações não especificadas como se fossem fatos;
- não abre fases futuras sem registro explícito.

## Interpretação correta do pedido

O objetivo é instalar uma estrutura agentic dentro do repositório para **entregar o projeto de modernização**, e não tratar a tarefa atual como simples criação de boilerplate.

## Implicações práticas

- priorizar contexto, fases, skills e subagentes;
- registrar caminho de entrega do projeto;
- orientar criação futura de README, docs, ADRs, código e Terraform;
- manter defaults conservadores quando a implementação real ainda não começou.

## Critério de sucesso deste pacote

Outro agente deve conseguir entrar no repositório, ler poucos arquivos e saber:
- qual é o projeto;
- em que fase ele está;
- quais regras precisa seguir;
- quais subagentes ou skills usar;
- o que ainda está em aberto.
