# 70-phase-governance

## Objetivo

Controlar evolução incremental do projeto sem colapso de escopo.

## Regra central

Sempre exista uma **fase ativa** registrada em `.agents/context/current-phase.md`.

## Fases sugeridas

### Fase 0 — Engine agentic e governança
Escopo:
- AGENTS.md
- regras
- templates
- skills
- subagentes
- contexto e decisões
- definição do roadmap inicial

Não iniciar:
- implementação ampla de aplicação;
- Terraform completo;
- integrações reais com legado.

### Fase 1 — Fundação do repositório e infraestrutura base
Escopo:
- README e docs iniciais do projeto;
- estrutura de diretórios;
- Terraform base;
- convenções de execução, teste e deploy;
- baseline de observabilidade e segurança.

### Fase 2 — Runtime compartilhado mínimo
Escopo:
- bootstrap;
- erro padronizado;
- logging estruturado;
- resolução de tenant;
- autenticação/autorização base;
- auditoria mínima transversal.

### Fase 3 — Attachments
Escopo:
- init-upload-session;
- confirm-upload;
- upload status;
- S3 presigned URL;
- fila e DLQ relacionadas;
- trilha de auditoria do fluxo.

### Fase 4 — Read models via legado
Escopo:
- contacts;
- users;
- processes;
- adapter de legado;
- contratos de leitura e testes correspondentes.

### Fase 5 — Hardening operacional
Escopo:
- alarmes;
- métricas;
- refinamento de IAM;
- WAF base;
- retenção;
- revisão de segurança e observabilidade.

### Fase 6+ — Expansão incremental
Escopo:
- novos slices;
- novos contratos;
- substituição progressiva do legado;
- ajustes estruturais sustentados por ADR.

## Critério para mudar de fase

Só avance quando:
- entregáveis da fase estiverem completos;
- riscos e pendências estiverem registrados;
- a próxima fase tiver objetivo explícito;
- a documentação refletir o estado atual.

## Registro obrigatório

Ao concluir ou abrir fase:
- atualizar `.agents/context/current-phase.md`;
- atualizar `.agents/context/30-phase-roadmap.md` se necessário;
- refletir o marco em README/CHANGELOG quando o repositório principal existir ou for alterado.
