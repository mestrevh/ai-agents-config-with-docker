---
name: commit-profissional
description: Formata e executa commits git seguindo o padrão profissional Conventional Commits. Deve ser ativada sempre que concluir uma tarefa, funcionalidade, correção ou etapa de plano.
---

# Roteiro

<roteiro>
Para gerar um commit profissional, siga a estrutura estrita:
1. Identifique a natureza da alteração:
   - `feat`: Nova funcionalidade
   - `fix`: Correção de bug
   - `test`: Adição ou ajuste de testes
   - `refactor`: Refatoração de código sem alterar comportamento externo
   - `docs`: Alteração em documentação
   - `style`: Formatação, ponto e vírgula, espaços
   - `chore`: Atualização de tarefas de build, pacotes, configs
2. Defina o escopo opcional entre parênteses (ex: `feat(auth): ...`).
3. Escreva o título no imperativo, em letras minúsculas, sem ponto final no cabeçalho (máximo 50 caracteres).
4. Adicione um corpo detalhado se necessário, explicando o **porquê** da alteração e **o que** foi modificado.
5. Execute os comandos git de stage e commit:
   ```bash
   git add .
   git commit -m "tipo(escopo): descrição concisa" -m "Detalhamento explícito das alterações."
   ```
</roteiro>

---

# Objetivo

<objetivo>
Padronizar o histórico do repositório Git com mensagens claras, semânticas e profissionais.
* Agrupar arquivos modificados.
* Formatar mensagem segundo o Conventional Commits.
* Registrar o commit no Git.
</objetivo>

---

# Modelo de Saída

<modelo_saida>
* **Formato:** Saída do comando git commit e mensagem formatada.
* **Restrição de Saída:** Sem mensagens informais ou emojis.
</modelo_saida>

---

# Panorama

<panorama>
O repositório requer histórico limpo para auditoria, automação de changelog e facilidade de rastreamento de alterações.
</panorama>

---

# Transformar

<transformar>
* **O que EVITAR:** Mensagens genéricas como "update", "fix bug", "ajustes", ou commits com erros de sintaxe.
* **O que OTIMIZAR:** Semântica Clara, uso do imperativo e escopo correto.
</transformar>
