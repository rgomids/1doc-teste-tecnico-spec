# Questões em Aberto

## Produto e integração

1. Qual será o mecanismo de autenticação/autorização para clientes externos?
2. A resolução de tenant virá por domínio, token, header assinado, mTLS ou combinação?
3. O adapter com legado acessará banco, API interna existente ou ambos?
4. Como será a trilha de auditoria de ponta a ponta: síncrona, assíncrona ou híbrida?
5. Qual será a política detalhada de retenção e classificação de logs/auditoria?

## Infra e operação

6. O backend Terraform terá qual estratégia por ambiente?
7. Há naming convention corporativa para recursos AWS e tags obrigatórias?
8. Haverá política formal de WAF já na fundação ou baseline mínima evolutiva?

## Engenharia

9. Qual framework HTTP/Lambda será adotado, se algum?
10. Qual biblioteca de validação será preferida?
11. Qual runner de testes será adotado?
12. Haverá padrão interno para CHANGELOG, versionamento e branching?

## Regra

Não resolva essas questões por suposição silenciosa.  
Registre como hipótese temporária ou abra ADR quando a resposta afetar arquitetura ou operação.
