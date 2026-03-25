# 20-coding

## Objetivo

Guiar implementação com baixa fricção e alta consistência.

## Linguagem e estilo

- Linguagem principal: TypeScript.
- Runtime-alvo: Node.js.
- Prefira funções e objetos simples antes de classes.
- Crie interfaces apenas quando houver desacoplamento real.
- Evite herança desnecessária.
- Prefira composição.

## Convenções

- nomeie casos de uso pelo verbo de negócio;
- mantenha arquivos próximos ao slice que atendem;
- use nomes explícitos em vez de abreviações obscuras;
- diferencie contratos de entrada, saída e erros.

## Regras para casos de uso

Cada slice deve ter, quando fizer sentido:
- input model;
- output model;
- validator;
- use case;
- portas/repositórios;
- implementação de infraestrutura;
- testes.

## Validação

- valide input externo na borda;
- valide variáveis de ambiente no bootstrap apropriado;
- normalize erros em categorias coerentes:
  - domínio;
  - aplicação;
  - infraestrutura;
  - autorização/autenticação;
  - validação.

## Logging e observabilidade

Logs devem ser estruturados em JSON e incluir, sempre que houver:
- `requestId`
- `tenantId`
- `useCase`
- `status`
- `latencyMs`
- `errorType`

Nunca logue:
- tokens;
- segredos;
- payloads sensíveis;
- PII desnecessária.

## Configuração

- segredos só via Secrets Manager ou mecanismo seguro equivalente;
- nenhuma credencial hardcoded;
- nenhuma configuração implícita crítica.

## Terraform

Para alterações em Terraform:
- mantenha módulos pequenos e objetivos;
- prefira variáveis explícitas;
- padronize tags;
- exponha outputs úteis;
- evite copiar e colar recursos.

## Critério para concluir mudança de código

Só conclua quando:
- o design respeitar as camadas;
- não houver dependência indevida do domínio em AWS;
- os handlers permanecerem finos;
- a documentação afetada tiver sido atualizada.
