# Diretrizes Globais de Desenvolvimento de Software

Este ambiente é regido por padrões rigorosos de Engenharia de Software, Test-Driven Development (TDD), controle de versão Git e gestão estruturada de planos de tarefas.

---

## Arquitetura e stack do sistema

Ao iniciar esse defina a stack do projeto e estrutura/arquitetura para conseguir utilizar as skills e regras. Sempre utilize a skill `antigravity-pair-programmer` para auxiliar no desenvolvimento.

## 1. Fluxo de Trabalho e Git Branching

1. **Criação de Branch**:
   - Todo novo desenvolvimento, correção ou refatoração deve iniciar criando uma nova branch a partir da branch `develop` (ex: `feature/nome-da-feature`, `fix/descricao-do-bug`).

2. **Desenvolvimento Orientado a Testes (TDD)**:
   - **Fase 1 (Red)**: Escreva o teste automatizado primeiro e execute para garantir que ele falha.
   - **Fase 2 (Green)**: Escreva o código mínimo necessário para fazer o teste passar.
   - **Fase 3 (Refactor)**: Refatore o código mantendo os testes passando. Caso os testes falhem após a refatoração, ajuste o código até que todos os testes passem com 100% de sucesso.

3. **Commits Profissionais**:
   - Cada entrega lógica deve ser commitada utilizando a convenção de commits profissionais via a skill `commit-profissional`.

4. **Pull Requests**:
   - Ao concluir a funcionalidade e garantir que todos os testes passaram, deve ser aberto um Pull Request direcionado para a branch `develop`.
   - O PR deve incluir um resumo detalhado de cada commit realizado.

---

## 2. Gestão de Planos em `.agents/plans/`

- Todo trabalho complexo ou multi-etapas deve ter um plano criado e armazenado no diretório [`.agents/plans/`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/antigravity-cli/.agents/plans/).
- Cada plano deve desmembrar as tarefas em passos menores, declarando explicitamente a aplicação das regras de TDD e a execução da skill `commit-profissional` para cada entrega efetuada.

---

## 3. Governança de Skills Locais

- [`tdd-workflow`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/antigravity-cli/.agents/skills/tdd-workflow/SKILL.md): Execução estrita do ciclo de testes TDD.
- [`commit-profissional`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/antigravity-cli/.agents/skills/commit-profissional/SKILL.md): Padronização de mensagens de commit no padrão Conventional Commits.
- [`pull-request-creator`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/antigravity-cli/.agents/skills/pull-request-creator/SKILL.md): Criação de PRs com documentação e histórico de commits.
- [`plan-generator`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/antigravity-cli/.agents/skills/plan-generator/SKILL.md): Geração de planos de desenvolvimento armazenados em `.agents/plans/`.
