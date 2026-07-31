---
name: tdd-workflow
description: Executa o ciclo estrito de desenvolvimento guiado por testes (TDD). Deve ser ativada ao iniciar qualquer nova funcionalidade, correção ou refatoração, garantindo a criação de testes antes do código de produção e a execução de refatoração contínua.
---

# Roteiro

<roteiro>
Siga estritamente os passos do ciclo TDD:
1. Verifique se está em uma branch criada a partir de `develop` (ex: `feature/nome`, `fix/nome`). Se não estiver, crie a branch.
2. **Vermelho (Red)**: Escreva o teste automatizado para a funcionalidade desejada. Execute a suíte de testes e confirme que o teste falhou conforme o esperado.
3. **Verde (Green)**: Escreva o código de produção mínimo e estritamente necessário para fazer o teste passar.
4. Execute novamente a suíte de testes.
   - Se passar: prossiga para a fase de refatoração.
   - Se falhar: refatore o código gerado imediatamente até que o teste passe.
5. **Refatoração (Refactor)**: Melhore o código (Clean Code, DRY, SOLID) mantendo todos os testes verdes.
6. Finalize executando a skill `commit-profissional` para registrar a entrega.
</roteiro>

---

# Objetivo

<objetivo>
Garantir 100% de cobertura e qualidade de software através da metodologia TDD.
* Criar a branch adequada a partir da `develop`.
* Escrever o teste antes da implementação.
* Garantir a aprovação total dos testes.
* Chamar a skill `commit-profissional` ao concluir cada etapa.
</objetivo>

---

# Modelo de Saída

<modelo_saida>
* **Formato:** Status da execução dos testes e arquivos gerados/modificados.
* **Restrição de Saída:** Sem explicações prolixas. Apresente os resultados dos testes e o status da execução.
</modelo_saida>

---

# Panorama

<panorama>
O desenvolvedor necessita de garantia de regressão zero e alta qualidade de código. A suíte de testes é o critério final para aprovação.
</panorama>

---

# Transformar

<transformar>
* **O que EVITAR:** Escrever código de produção antes do teste; considerar uma tarefa concluída com testes falhando.
* **O que OTIMIZAR:** Rapidez do ciclo de feedback dos testes e clareza nas asserções.
</transformar>
