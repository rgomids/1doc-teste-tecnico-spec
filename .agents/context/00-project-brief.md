# Contexto do Projeto

## Objetivo

Entregar a fundação e a evolução incremental de uma nova API em **TypeScript/Node.js** para modernização progressiva de um legado **PHP + MySQL** em AWS, sem big bang rewrite.

## Restrições principais

- abordagem Strangler Fig;
- AWS serverless;
- modular monolith + vertical slices;
- múltiplos handlers Lambda finos;
- upload direto para S3 via presigned URL;
- SQS para processamento assíncrono;
- DynamoDB para metadados transversais;
- Terraform modular;
- isolamento multitenant;
- auditabilidade e conformidade desde a base.

## Capacidades iniciais previstas

- healthcheck;
- resolução de tenant;
- autenticação/autorização base;
- criação e confirmação de sessão de upload;
- leitura inicial de contatos;
- leitura inicial de usuários;
- leitura inicial de processos via adapter;
- registro de auditoria.

## Entidades e áreas de negócio

- processos
- anexos
- contatos
- usuários

## Não funcionais relevantes

- 2 milhões de requisições por dia;
- pico de 100 mil requisições em 15 minutos;
- 200 mil uploads por dia;
- tamanho médio de arquivo de 5 MB;
- persistência eterna dos arquivos;
- logs estruturados;
- observabilidade e alarmes básicos;
- segurança e segregação por tenant mandatórias.

## Nota operacional

Este engine deve guiar a entrega do projeto específico.  
Não usar este contexto para gerar um starter genérico desconectado do repositório-alvo.
