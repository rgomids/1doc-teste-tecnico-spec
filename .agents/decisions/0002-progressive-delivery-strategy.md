# 0002 — A entrega do projeto será guiada por fases incrementais

- status: aceito

## Contexto

O projeto possui múltiplas frentes: arquitetura, documentação, Terraform, runtime compartilhado, slices de negócio, integração com legado, segurança e observabilidade.

## Decisão

A evolução será controlada por fases explícitas:
1. engine agentic;
2. fundação documental e estrutural;
3. infraestrutura base e runtime compartilhado;
4. attachments;
5. leituras via legado;
6. hardening e expansão incremental.

## Consequências

Positivas:
- reduz risco de sobrecarga de contexto;
- melhora governança;
- facilita handoff;
- permite validação progressiva.

Negativas:
- exige disciplina de atualização de fase;
- pode parecer mais lento se o time tentar fazer tudo de uma vez.

## Trade-off

Prioriza previsibilidade, segurança de mudança e continuidade entre sessões em vez de execução ampla sem controle.

## Regra associada

Toda troca de fase deve atualizar `.agents/context/current-phase.md` e refletir em handoff/documentação relevante.
