# 10-architecture

## Objetivo

Preservar a arquitetura-alvo do projeto de modernização progressiva em AWS serverless.

## Arquitetura mandatória

- **Estratégia**: Strangler Fig sobre legado PHP + MySQL.
- **Estilo**: modular monolith.
- **Organização**: vertical slices por capacidade/caso de uso.
- **Execução**: múltiplos handlers Lambda finos.
- **Infraestrutura**: Terraform modular.
- **Upload de arquivos**: S3 via presigned URL.
- **Assíncrono**: SQS.
- **Metadados transversais**: DynamoDB.
- **Auditabilidade e observabilidade**: desde a fundação.

## Estrutura lógica obrigatória

Cada módulo deve respeitar, quando aplicável:

- `application/`: casos de uso, orquestração, contratos de entrada/saída.
- `domain/`: regras de negócio e modelos de domínio sem dependência de AWS.
- `infrastructure/`: integrações, SDKs, bancos, filas, serviços externos.
- `presentation/`: DTOs, schemas, validação, mapeadores, contratos de exposição.

## Handler Lambda

Handler é apenas porta de entrada e saída.

Handler pode:
- receber evento;
- extrair contexto;
- validar payload;
- chamar caso de uso;
- mapear resposta/erro.

Handler não pode:
- conter regra de negócio;
- conhecer detalhes internos do legado;
- conhecer detalhes de persistência além do necessário para composição;
- misturar observabilidade com lógica de domínio.

## Organização por domínio inicial

Domínios iniciais previstos:
- attachments
- contacts
- users
- processes
- tenants
- auth
- audit

## Vertical slices iniciais esperados

- `attachments/init-upload-session`
- `attachments/confirm-upload`
- `attachments/get-upload-status`
- `contacts/list-contacts`
- `contacts/get-contact`
- `users/list-users`
- `users/get-user`
- `processes/get-process`
- `processes/list-processes`
- `tenants/resolve-tenant-context`
- `audit/register-audit-event`

## Integração com legado

A integração com legado deve passar por **adapter/anti-corruption layer**.

Regras:
- não vazar modelo do legado para fora do adapter;
- expor contratos orientados ao novo domínio;
- manter implementação substituível;
- começar stubado quando a integração real ainda não estiver disponível;
- registrar limitações conhecidas em docs de contexto ou ADR.

## Shared mínimo

O diretório `shared` só pode conter:
- kernel mínimo;
- tipos realmente transversais;
- componentes de observabilidade e erro padronizados;
- utilitários pequenos e comprovadamente reutilizados.

Não mova código para `shared` apenas para “evitar duplicação” prematuramente.

## Regras de expansão

Só extraia novo módulo, novo subagente ou nova skill quando houver:
- repetição clara;
- ganho operacional real;
- fronteira estável.

## Sinais de violação arquitetural

- handler espesso;
- domínio importando SDK AWS;
- acoplamento direto entre módulos de negócio;
- adapter de legado espalhado por múltiplos módulos;
- repositórios compartilhados sem contrato claro;
- Terraform gigante e não modularizado.
