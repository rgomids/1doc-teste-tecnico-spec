# Skill: create-adr

## Quando usar

Use esta skill quando uma escolha estrutural afetar arquitetura, fronteiras, infraestrutura, estratégia de integração ou fluxo operacional importante.

## Leituras mínimas

- `.agents/rules/10-architecture.md`
- `.agents/rules/40-documentation.md`
- `.agents/decisions/*.md` relacionados
- ADRs existentes do projeto, quando já existirem

## Estrutura obrigatória

- título
- status
- contexto
- decisão
- consequências
- trade-offs
- alternativas consideradas

## Passos

1. Explicitar o problema.
2. Registrar restrições reais.
3. Descrever a decisão de forma verificável.
4. Documentar impacto positivo e negativo.
5. Ligar a decisão às fases afetadas.
6. Atualizar docs correlatas.

## Feito quando

- outro agente consegue entender por que a decisão foi tomada;
- a decisão reduz reabertura de discussão sem contexto novo.
