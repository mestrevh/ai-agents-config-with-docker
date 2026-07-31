---
name: plan-generator
description: Gera planos de desenvolvimento estruturados em arquivos Markdown no diretório .agents/plans/. Deve ser ativada antes de iniciar demandas complexas, garantindo que cada tarefa preveja a skill commit-profissional.
---

# Roteiro

<roteiro>
Para criar um plano de desenvolvimento profissional:
1. Defina um nome descritivo para o arquivo do plano (ex: `.agents/plans/feature_autenticacao.md`).
2. Estruture o plano em Markdown contendo:
   - **Objetivo Geral**: O que o plano pretende alcançar.
   - **Branch de Origem**: Confirmação da branch `develop`.
   - **Checklist de Tarefas**: Lista incremental de tasks.
3. Para **CADA TAREFA**, obrigatoriamente inclua os passos:
   - [ ] Fase 1: Escrever teste (TDD Red)
   - [ ] Fase 2: Implementar código (TDD Green & Refactor)
   - [ ] Fase 3: Executar skill `commit-profissional`
4. Salve o arquivo na pasta `.agents/plans/`.
</roteiro>

---

# Objetivo

<objetivo>
Criar planos de desenvolvimento rastreáveis e executáveis em `.agents/plans/`, embutindo as regras de TDD e commits profissionais em cada etapa.
* Criar arquivo `.md` em `.agents/plans/`.
* Vincular cada tarefa à skill `commit-profissional`.
* Garantir fluxo de trabalho a partir da branch `develop`.
</objetivo>

---

# Modelo de Saída

<modelo_saida>
* **Formato:** Arquivo Markdown gravado em `.agents/plans/`.
* **Estrutura:**
  ```markdown
  # Plano: [Nome do Plano]

  - Branch Base: develop

  ## Checklist de Tasks
  - [ ] Task 1: [Descrição]
    - [ ] Criar testes TDD
    - [ ] Implementar solução
    - [ ] Executar skill commit-profissional
  ```
</modelo_saida>

---

# Panorama

<panorama>
Projetos de software requerem planejamento granular onde cada sub-tarefa é auditável e commitada de forma independente.
</panorama>

---

# Transformar

<transformar>
* **O que EVITAR:** Planos vagas sem sub-tarefas de commit ou que ignorem a esteira de TDD.
* **O que OTIMIZAR:** Granularidade das tarefas e vínculo com a skill `commit-profissional`.
</transformar>
