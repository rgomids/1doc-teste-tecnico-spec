# 40-documentation

## Objetivo

Manter documentação suficiente para continuidade segura por outros agentes e pessoas.

## Regra base

Mudança relevante em arquitetura, contrato, operação, fase ou decisão deve refletir em documentação adequada.

## O que atualizar e quando

### README
Atualize quando houver mudança em:
- visão geral;
- setup;
- execução local;
- testes;
- deploy;
- estrutura principal;
- status da fundação.

### CHANGELOG
Atualize quando houver mudança relevante para acompanhamento histórico do projeto.

### ADR
Crie ou atualize quando houver:
- decisão arquitetural nova;
- trade-off estrutural;
- substituição de abordagem;
- mudança de fronteira entre módulos.

### Documentação de domínio
Atualize quando mudar:
- responsabilidade do módulo;
- casos de uso;
- integrações;
- limites;
- riscos.

### Contexto do engine
Atualize `.agents/context/` quando mudar:
- fase atual;
- roadmap;
- hipóteses operacionais;
- escopo permitido;
- lacunas abertas.

## Critérios de documentação boa

- curta, específica e acionável;
- alinhada ao estado real;
- sem duplicação extensa;
- com trade-offs claros;
- distinguindo fato, hipótese e decisão.

## Regra adicional

`README` e `CHANGELOG` devem refletir mudanças relevantes do projeto.  
O engine não substitui a documentação do repositório; ele organiza sua evolução.
