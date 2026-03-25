# AGENTS.md

## Missão

Este repositório usa um engine operacional para orientar agentes de IA e humanos na **entrega incremental** da nova API de modernização do legado PHP + MySQL em AWS.  
O foco deste engine é **conduzir o trabalho do projeto específico**, não criar um starter genérico nem um scaffold paralelo.

## Escopo deste engine

- guiar a execução por fases;
- reduzir contexto carregado por tarefa;
- preservar coerência entre arquitetura, código, Terraform, segurança e documentação;
- permitir handoff curto entre sessões;
- registrar hipóteses, decisões e pendências relevantes.

## Ordem mínima de leitura

1. `AGENTS.md`
2. `.agents/context/current-phase.md`
3. `.agents/context/00-project-brief.md`
4. `.agents/context/10-scope-boundaries.md`
5. `.agents/rules/00-global.md`
6. regras específicas da tarefa:
   - arquitetura: `.agents/rules/10-architecture.md`
   - implementação: `.agents/rules/20-coding.md`
   - testes: `.agents/rules/30-testing.md`
   - documentação: `.agents/rules/40-documentation.md`
   - segurança: `.agents/rules/50-security.md`
   - entrega: `.agents/rules/60-delivery.md`
   - fase: `.agents/rules/70-phase-governance.md`
7. `.agents/decisions/*.md` e `.agents/context/*.md` relevantes ao escopo

## Política de contexto mínimo

Carregue apenas o necessário para a tarefa atual.

- Não leia todo o diretório `.agents/` por padrão.
- Use `.agents/context/` para entender o projeto.
- Use `.agents/decisions/` para evitar reabrir decisões já estabilizadas.
- Use `.agents/skills/` quando houver workflow repetitivo.
- Use `.agents/subagents/` apenas quando houver benefício claro de especialização.

## Como usar `.agents/`

- `rules/`: guardrails permanentes.
- `templates/`: formatos obrigatórios de handoff, fase, task brief e revisão.
- `skills/`: playbooks operacionais reutilizáveis.
- `subagents/`: papéis especializados.
- `context/`: contexto de projeto, escopo, roadmap, hipóteses e estado atual.
- `decisions/`: decisões arquiteturais e operacionais já tomadas.

## Convenção de fases

Este projeto deve avançar por fases explícitas.  
Antes de iniciar uma mudança, valide a fase ativa em `.agents/context/current-phase.md` e as regras em `.agents/rules/70-phase-governance.md`.

## Regra de handoff

Ao encerrar uma sessão relevante, registre um handoff usando `.agents/templates/handoff.md`.  
O handoff deve cobrir:
- objetivo;
- escopo trabalhado;
- arquivos afetados;
- decisões;
- pendências;
- riscos;
- evidências de validação.

## Regra de validação antes de concluir tarefa

Nenhuma tarefa deve ser marcada como concluída sem:
- aderência à fase ativa;
- evidência de validação compatível com o tipo de mudança;
- atualização de documentação afetada;
- registro explícito de lacunas, riscos e hipóteses.

## Quando consultar o restante do projeto

Consulte código-fonte, Terraform, README, CHANGELOG, ADRs e docs do projeto quando:
- a tarefa tocar diretórios já existentes;
- houver risco de conflito com convenções reais do repositório;
- uma decisão depender de integração com legado, segurança, observabilidade ou deploy;
- a mudança alterar contrato público, fluxo operacional ou arquitetura.

## Defaults operacionais

Na ausência de definição explícita:
- prefira mudanças pequenas, reversíveis e verificáveis;
- não habilite automações agressivas;
- não assuma paralelização multiagente;
- não assuma MCP obrigatório;
- trate segurança, tenant isolation, auditoria e observabilidade como requisitos de base.

## Arquivos para revisar primeiro ao evoluir o engine

- `AGENTS.md`
- `.agents/context/current-phase.md`
- `.agents/context/30-phase-roadmap.md`
- `.agents/rules/10-architecture.md`
- `.agents/rules/70-phase-governance.md`
