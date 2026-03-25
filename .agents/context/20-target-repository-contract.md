# Contrato de Repositório-Alvo

## Estrutura-alvo prevista para o projeto

Esta estrutura deve orientar a entrega futura, sem obrigar scaffold imediato completo:

```text
/README.md
/AGENTS.md
/docs
  /architecture
    /solution.md
    /c4-container.md
  /adr
    /0001-foundation-serverless-modernization.md
  /domains
    /attachments.md
    /contacts.md
    /users.md
    /processes.md
/src
  /entrypoints
    /lambda
      /http
        /health
        /attachments
        /contacts
        /users
        /processes
      /async
        /attachments
        /audit
  /modules
    /attachments
    /contacts
    /users
    /processes
    /tenants
    /audit
    /auth
  /shared
/tests
  /unit
  /integration
  /contract
/terraform
  /environments
    /dev
    /hml
    /prd
  /modules
    /api_gateway
    /lambda
    /iam
    /s3
    /dynamodb
    /sqs
    /waf
    /kms
    /cloudwatch
    /secrets_manager
```

## Regra

Esta estrutura é referência de entrega futura.  
Não assuma que todos esses diretórios já existem no repositório no momento da instalação do engine.

## Mapeamento de responsabilidade

- `docs/`: visão, arquitetura, ADR e domínio;
- `src/entrypoints/`: portas de entrada;
- `src/modules/`: vertical slices e fronteiras de negócio;
- `src/shared/`: transversal mínimo;
- `tests/`: validação por camada;
- `terraform/`: infraestrutura modular por ambiente.

## Uso deste documento

Consulte este arquivo antes de:
- propor novos módulos;
- criar slices;
- planejar Terraform;
- revisar fronteiras de diretório.
