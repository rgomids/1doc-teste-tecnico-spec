# 1doc-teste-tecnico-spec

Repositório de especificação e governança para a modernização incremental de um legado **PHP + MySQL** para uma nova API em **TypeScript/Node.js** na **AWS**.

> Estado atual (25/03/2026): **Fase 0 ativa — engine agentic e governança**.

## 1) Objetivo do projeto

Este projeto existe para orientar a entrega progressiva de uma nova API, sem _big bang rewrite_, usando a estratégia **Strangler Fig**.

A fundação contempla:
- direcionamento por fases;
- documentação operacional para agentes e humanos;
- guardrails de arquitetura, segurança, testes e entrega;
- trilha de decisões para continuidade entre sessões.

## 2) Objetivo do repositório nesta etapa

Neste momento, o repositório prioriza a **camada agentic** (regras, contexto, templates, skills e decisões) para preparar o desenvolvimento da aplicação real nas próximas fases.

### Em escopo na fase ativa
- governança de execução;
- contexto mínimo para handoff;
- regras modulares por tema (arquitetura, coding, testes, segurança etc.);
- roadmap incremental de evolução.

### Fora de escopo imediato
- scaffold completo da aplicação;
- implementação ampla de código de produto;
- Terraform completo;
- integração real com legado.

## 3) Arquitetura-alvo (visão macro)

A arquitetura planejada para as próximas fases é:

- **estratégia**: Strangler Fig sobre legado PHP + MySQL;
- **estilo**: modular monolith com vertical slices;
- **runtime**: múltiplos handlers Lambda finos;
- **upload**: S3 com presigned URL;
- **assíncrono**: SQS (+ DLQ nas filas críticas);
- **metadados transversais**: DynamoDB;
- **infra**: Terraform modular;
- **segurança**: isolamento multitenant, least privilege e auditoria desde a base.

## 4) Fases de entrega

O roadmap operacional está em `.agents/context/30-phase-roadmap.md` e hoje segue este macrofluxo:

1. **Fase 0** — Engine agentic e governança (ativa);
2. **Fase 1** — Fundação documental e estrutural do projeto;
3. **Fase 2** — Infraestrutura base e runtime compartilhado mínimo;
4. **Fase 3** — Attachments (upload session, confirm, status);
5. **Fase 4** — Read APIs via adapter de legado;
6. **Fase 5** — Hardening (observabilidade e segurança);
7. **Fase 6+** — Expansão incremental.

## 5) Estrutura atual do repositório

```text
.
├── AGENTS.md
├── README.md
└── .agents/
    ├── context/
    ├── decisions/
    ├── rules/
    ├── skills/
    ├── subagents/
    └── templates/
```

## 6) Como trabalhar neste repositório

### Leitura mínima obrigatória para iniciar uma tarefa

1. `AGENTS.md`
2. `.agents/context/current-phase.md`
3. `.agents/context/00-project-brief.md`
4. `.agents/context/10-scope-boundaries.md`
5. `.agents/rules/00-global.md`
6. regras específicas da tarefa em `.agents/rules/`

### Fluxo padrão de entrega

1. identificar fase ativa;
2. validar escopo permitido;
3. executar a menor mudança útil e reversível;
4. validar proporcionalmente ao risco;
5. atualizar documentação impactada;
6. registrar handoff da sessão.

## 7) Contrato da estrutura-alvo (fases futuras)

A referência de estrutura futura está em:

- `.agents/context/20-target-repository-contract.md`

Esse contrato orienta a evolução para `docs/`, `src/`, `tests/` e `terraform/`, sem forçar scaffold completo antecipado.

## 8) Segurança e qualidade (requisitos de base)

- não vazar segredos ou credenciais;
- não logar PII desnecessária;
- manter segregação por tenant como requisito estrutural;
- validar mudanças com evidência explícita;
- registrar pendências, hipóteses e risco residual quando aplicável.

## 9) Estado atual e próximos passos recomendados

### Estado atual
- engine agentic instalado e ativo;
- regras de governança e qualidade definidas;
- contexto, decisões e templates prontos para uso.

### Próximos passos recomendados (abertura da Fase 1)
1. consolidar documentação de arquitetura em `docs/architecture`;
2. criar ADR inicial da fundação serverless;
3. definir estrutura inicial de diretórios (`src`, `tests`, `terraform`) com convenções de execução e validação;
4. iniciar README operacional da aplicação (setup, testes, deploy).

## 10) Referências principais

- `AGENTS.md`
- `.agents/context/current-phase.md`
- `.agents/context/30-phase-roadmap.md`
- `.agents/context/20-target-repository-contract.md`
- `.agents/rules/70-phase-governance.md`
