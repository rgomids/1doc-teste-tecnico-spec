# 30-testing

## Objetivo

Garantir que mudanças venham acompanhadas de validação proporcional ao risco.

## Regra principal

Antes de propor implementação relevante, proponha ou identifique a estratégia de teste correspondente.

## Mínimo esperado por tipo de mudança

### Casos de uso
- testes unitários de comportamento;
- testes de ramificações críticas;
- testes de erro quando existirem regras relevantes.

### Validação e mapeamento
- testes de schema/validator;
- testes de serialização ou mapeamento quando houver contrato público.

### Handlers
- testes do caminho feliz;
- testes de erro padronizado;
- testes de extração de contexto relevante.

### Integrações
- preparar testes de integração ou contract tests;
- usar fakes/stubs quando a integração real ainda não estiver disponível;
- documentar o que ficou simulado.

### Terraform e infraestrutura
- validar formatação e consistência;
- revisar inputs, outputs e dependências;
- documentar recursos críticos impactados.

## Estratégia recomendada

- unitário para regras e orquestração;
- integração para adaptadores e infraestrutura;
- contrato para APIs e integrações relevantes;
- validação manual só quando automatização não couber ainda, com evidência explícita.

## Evidência mínima de validação

Toda entrega deve registrar pelo menos:
- o que foi validado;
- como foi validado;
- o que não foi validado;
- risco residual.

## Proibições

- concluir feature sem evidência;
- usar mock demais a ponto de esconder comportamento real;
- ignorar testes de borda em contratos públicos;
- misturar teste unitário com dependência externa real sem necessidade.
