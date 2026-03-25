# 00-global

## Objetivo

Definir comportamento padrão para qualquer agente atuando neste repositório.

## Regras universais

1. Trabalhe sobre o **projeto real**, não sobre um projeto hipotético.
2. Não transforme falta de contexto em invenção. Marque lacunas como **hipótese** ou **pendência**.
3. Diferencie sempre:
   - **Fato**: confirmado em arquivo, código ou decisão registrada.
   - **Hipótese**: assumido temporariamente por falta de dado.
   - **Decisão**: escolha explícita registrada.
4. Prefira mudanças pequenas, reversíveis e fáceis de revisar.
5. Antes de alterar estrutura, confirme impacto em fase, arquitetura, segurança, testes e documentação.
6. Não expanda escopo silenciosamente.
7. Não reescreva documentos estáveis sem necessidade objetiva.
8. Registre riscos e pendências quando não puder resolvê-los no mesmo ciclo.
9. Preserve consistência de nomenclatura entre código, docs, Terraform e ADRs.
10. Considere o legado como fonte de restrições, não como modelo a ser copiado.

## Modo de execução

Para cada tarefa, produza internamente esta sequência:

1. identificar a fase ativa;
2. identificar artefatos e regras relevantes;
3. explicitar restrições;
4. executar a menor mudança útil;
5. validar;
6. atualizar documentação e handoff quando necessário.

## Critérios de qualidade

- Clareza operacional.
- Baixo acoplamento.
- Mínimo contexto carregado.
- Segurança por padrão.
- Documentação suficiente para continuidade por outro agente.
- Ausência de boilerplate sem função clara.

## Proibições

- criar abstrações genéricas sem caso real;
- usar `shared` como depósito genérico;
- ignorar limites da fase atual;
- fechar tarefa sem evidência de validação;
- tratar hipótese como fato.
