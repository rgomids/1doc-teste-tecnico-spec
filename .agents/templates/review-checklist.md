# Review Checklist

## Arquitetura
- [ ] A fase ativa foi respeitada.
- [ ] O handler continua fino.
- [ ] O domínio não depende de AWS.
- [ ] Não houve acoplamento indevido entre módulos.
- [ ] O adapter de legado continua encapsulado.

## Código e Infra
- [ ] A mudança é pequena e verificável.
- [ ] Não há abstração genérica sem necessidade.
- [ ] `shared` não recebeu conteúdo indevido.
- [ ] Terraform permaneceu modular.
- [ ] Inputs, outputs e tags foram tratados adequadamente.

## Segurança
- [ ] Não há segredos ou dados sensíveis expostos.
- [ ] Tenant isolation foi considerado.
- [ ] Logging segue política segura.
- [ ] IAM/KMS/WAF/Secrets não foram ampliados sem justificativa.

## Testes e validação
- [ ] Existe evidência de validação compatível com o risco.
- [ ] Lacunas de validação foram registradas.
- [ ] Risco residual foi explicitado.

## Documentação
- [ ] README foi revisado se necessário.
- [ ] CHANGELOG foi revisado se necessário.
- [ ] ADR/contexto/documentação de domínio foram atualizados quando aplicável.
- [ ] Handoff foi preparado quando a sessão exigia continuidade.

## Conclusão
- [ ] A entrega está pronta para continuidade segura por outro agente.
