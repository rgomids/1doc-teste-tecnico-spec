# Skill: scaffold-vertical-slice

## Quando usar

Use esta skill para adicionar ou revisar um vertical slice de negócio.

## Leituras mínimas

- `AGENTS.md`
- `.agents/context/20-target-repository-contract.md`
- `.agents/rules/10-architecture.md`
- `.agents/rules/20-coding.md`
- `.agents/rules/30-testing.md`
- `.agents/rules/50-security.md`

## Entradas esperadas

- domínio
- nome do caso de uso
- contrato de entrada/saída
- integrações envolvidas
- fase atual

## Passos

1. Verificar se o slice pertence à fase ativa.
2. Definir input, output e validator.
3. Definir caso de uso e portas necessárias.
4. Posicionar implementação por camada.
5. Garantir handler fino, se houver endpoint/trigger.
6. Definir testes mínimos.
7. Atualizar documentação de domínio e handoff.

## Checklist rápido

- domínio não depende de AWS;
- infraestrutura não vaza para aplicação;
- logs não expõem dados sensíveis;
- contrato público está documentado;
- testes cobrem comportamento crítico.

## Saída esperada

- estrutura do slice;
- regras de validação;
- pontos de teste;
- docs impactadas.
