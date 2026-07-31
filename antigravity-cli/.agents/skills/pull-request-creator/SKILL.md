---
name: pull-request-creator
description: Cria e formata Pull Requests para a branch develop, contendo a lista completa de commits realizados e seus detalhes. Deve ser ativada ao finalizar uma feature ou conjunto de alterações.
---

# Roteiro

<roteiro>
Siga o fluxo para abertura de um Pull Request estruturado:
1. Obtenha a lista de todos os commits realizados na branch atual em relação à `develop`:
   ```bash
   git log origin/develop..HEAD --oneline
   ```
2. Monte a descrição do Pull Request estruturada em Markdown:
   - **Título**: Resumo claro da proposta do PR.
   - **Descrição Geral**: O que a branch resolve ou implementa.
   - **Resumo dos Commits**: Lista detalhada de cada commit incluído, explicando seu propósito.
   - **Garantia de Qualidade**: Confirmação de que os testes TDD foram executados e aprovados.
3. Suba as alterações para o repositório remoto:
   ```bash
   git push origin <nome-da-branch>
   ```
4. Apresente o modelo final do Pull Request ou utilize a CLI correspondente (`gh pr create`).
</roteiro>

---

# Objetivo

<objetivo>
Gerar a documentação completa de um Pull Request direcionado para `develop`, detalhando cada commit do histórico.
* Listar os commits da branch.
* Formatar a descrição com comentários de cada commit.
* Garantir direcionamento para a branch `develop`.
</objetivo>

---

# Modelo de Saída

<modelo_saida>
* **Formato:** Documento Markdown do Pull Request com tabela ou lista formatada dos commits.
* **Estrutura:**
  - Título do PR
  - Visão Geral
  - Tabela / Lista de Commits
  - Validação TDD
</modelo_saida>

---

# Panorama

<panorama>
A equipe de desenvolvimento realiza code reviews com base nos Pull Requests enviados para a branch `develop`. A rastreabilidade dos commits é fundamental.
</panorama>

---

# Transformar

<transformar>
* **O que EVITAR:** PRs sem descrição, PRs direcionados para a branch incorreta ou sem compilação prévia dos commits.
* **O que OTIMIZAR:** Rastreabilidade dos commits e clareza na intenção de cada modificação.
</transformar>
