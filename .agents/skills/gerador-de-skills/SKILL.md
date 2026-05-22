---
name: gerador-de-skills
description: Transforma um comando simples ou uma ideia solta do usuário em uma Skill estruturada completa seguindo o framework padrão.
---

# Roteiro

<roteiro>
Para gerar a melhor Skill possível a partir do comando fornecido, siga estritamente este fluxo de execução:
1. Analise o comando simples ou a ideia enviada pelo usuário na seção "Panorama".
2. Identifique qual é o papel técnico (Persona) implícito ideal para executar aquela tarefa.
3. Extraia o Objetivo principal e desmembre-o em subtarefas claras e acionáveis.
4. Monte um Roteiro lógico passo a passo (Chain-of-Thought) que guiará o agente na execução dessa nova habilidade.
5. Defina o Modelo de Saída (formato, estrutura e restrições) que melhor se adapta ao resultado esperado para essa tarefa.
6. Monte o cenário no Panorama para dar contexto ao agente que for herdar essa Skill.
</roteiro>

---

# Objetivo

<objetivo>
Sua tarefa principal é: Criar uma nova Skill robusta, detalhada e pronta para uso com base em uma instrução curta.
Para concluir essa tarefa, você deve:
* Preencher perfeitamente os blocos frontmatter (name, description).
* Desenvolver um <roteiro> rico com pelo menos 4 passos lógicos para a nova skill.
* Definir um <modelo_saida> altamente focado em scannability e utilidade prática.
* Manter a formatação e as tags idênticas ao template padrão.
</objetivo>

---

# Modelo

<modelo_saida>
Entregue o resultado final estruturado estritamente no seguinte formato:
* **Formato:** Bloco de código contendo o Markdown estruturado do framework.
* **Estrutura:** 1. Frontmatter (name, description) entre os delimitadores `---`.
  2. Seções estruturadas por cabeçalhos (`#`) seguidas por suas respectivas tags XML (`<roteiro>`, `<objetivo>`, `<modelo_saida>`, `<panorama>`).
* **Restrição de Saída:** Vá direto ao ponto e exiba apenas o bloco de código da nova Skill gerada, sem introduções textuais antes ou parabéns depois.
</modelo_saida>

# Panorama

<panorama>
## Cenário de Atuação
O usuário quer expandir as capacidades do seu agente criando novas habilidades de forma ágil. Em vez de preencher manualmente todo o framework para cada nova ideia, ele passará apenas um comando direto (ex: "faça uma skill para auditar tabelas SQL" ou "faça uma skill para gerar relatórios de ponto") e espera receber a estrutura de prompt perfeitamente polida, detalhada e preenchida para aquela finalidade.
</panorama>