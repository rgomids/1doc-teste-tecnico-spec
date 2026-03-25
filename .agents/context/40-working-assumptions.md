# Hipóteses de Trabalho

## Hipóteses atualmente assumidas

1. O repositório-alvo já existe ou existirá em breve, mas ainda pode não conter toda a estrutura final.
2. A camada agentic deve ser instalada primeiro para orientar a execução futura.
3. O projeto seguirá TypeScript/Node.js, Terraform e AWS serverless como decisões já definidas.
4. Não há, neste momento, definição fechada de mecanismo de autenticação para clientes externos.
5. A integração real com o legado pode começar por stub ou adapter simulado.
6. Paralelização multiagente não está habilitada por padrão.
7. Autoevolução de regras/skills não está habilitada por padrão.
8. MCP não é obrigatório; CLI/skills locais podem ser preferidos caso o fluxo real do repositório favoreça isso.

## Como tratar estas hipóteses

- use até que fatos do repositório ou decisões novas as substituam;
- quando uma hipótese virar decisão, registre em `.agents/decisions/`;
- quando uma hipótese se provar incorreta, atualize este arquivo e o roadmap afetado.
