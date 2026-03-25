# Roadmap de Fases

## Fase 0 — Engine agentic
Objetivo:
- instalar AGENTS.md;
- instalar regras, templates, skills, subagentes, contexto e decisões;
- definir governança inicial do projeto.

Saída esperada:
- engine operacional pronto para uso.

## Fase 1 — Fundação documental e estrutural do projeto
Objetivo:
- README inicial;
- documentação de arquitetura;
- ADR inicial;
- estrutura-alvo do repositório;
- plano de validação e convenções base.

## Fase 2 — Infraestrutura base e runtime compartilhado mínimo
Objetivo:
- Terraform base;
- configuração de ambientes;
- logging estruturado;
- erro padronizado;
- resolução de tenant;
- autenticação/autorização base;
- auditoria mínima.

## Fase 3 — Attachments
Objetivo:
- init-upload-session;
- confirm-upload;
- get-upload-status;
- fluxo S3 presigned URL;
- fila e DLQ associadas.

## Fase 4 — Read APIs via adapter de legado
Objetivo:
- contacts/list-contacts;
- users/list-users;
- processes/get-process;
- adapter de legado desacoplado;
- testes e documentação de integração.

## Fase 5 — Hardening
Objetivo:
- alarmes;
- métricas;
- IAM refinado;
- WAF base;
- revisão de segurança;
- revisão de observabilidade.

## Fase 6 — Expansão incremental
Objetivo:
- novos slices;
- novas capacidades;
- substituições graduais do legado;
- ADRs adicionais.

## Regra de uso

O roadmap pode evoluir, mas toda mudança de fase ou escopo deve refletir em:
- `.agents/context/current-phase.md`
- handoff correspondente
- documentação principal do projeto quando ela existir
