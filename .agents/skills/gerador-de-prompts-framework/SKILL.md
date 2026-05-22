---
name: gerador-de-prompts-framework
description: Transforma qualquer pedido simples em um prompt estruturado avançado de nível de produção utilizando o framework completo de 6 etapas.
---

# Roteiro

<roteiro>
Para gerar o prompt estruturado perfeito, siga estritamente este fluxo de execução:
1. Analise o pedido simples enviado pelo usuário e extraia a real intenção e o entregável final desejado.
2. Determine uma Persona especialista de nível sênior que domine completamente o assunto do pedido.
3. Desenhe um Roteiro lógico (Chain-of-Thought) passo a passo para guiar a IA de forma impecável na execução da tarefa.
4. Defina o Objetivo central e desmembre-o em subtarefas cirúrgicas, diretas e acionáveis.
5. Projete o Modelo de Saída ideal para o cenário, priorizando a escaneabilidade, organização visual e clareza.
6. Monte as diretrizes do Panorama, contextualizando o cenário de fundo e criando placeholders ideais para exemplos práticos.
7. Estabeleça os critérios de Transformação com regras estritas sobre o que a IA deve otimizar e, principalmente, o que ela deve evitar.
</roteiro>

---

# Objetivo

<objetivo>
Sua tarefa principal é: Converter instruções vagas ou tarefas soltas em prompts estruturados de alta performance.
Para concluir essa tarefa, você deve:
* Preencher de forma rica, técnica e customizada cada um dos 6 blocos do framework solicitado.
* Manter os comentários explicativos originais em formato de citação (`>`) logo abaixo de cada cabeçalho principal.
* Entregar o prompt pronto com os marcadores de posição preenchidos especificamente para a necessidade do usuário, sem deixar campos genéricos genéricos (ex: em vez de manter "[Inserir Profissão]", preencha com o papel real necessário).
</objetivo>

---

# Modelo

<modelo_saida>
Entregue o resultado final estruturado estritamente no seguinte formato:
* **Formato:** Bloco de código Markdown contendo o prompt estruturado gerado.
* **Estrutura:** 1. Cabeçalho `# Persona` + citação + tag `<persona>`.
  2. Cabeçalho `# Roteiro` + citação + tag `<roteiro>`.
  3. Cabeçalho `# Objetivo` + citação + tag `<objetivo>`.
  4. Cabeçalho `# Modelo` + citação + tag `<modelo_saida>`.
  5. Cabeçalho `# Panorama` + citação + tag `<panorama>`.
  6. Cabeçalho `# Transformar` + citação + tag `<transformar>`.
* **Restrição de Saída:** Vá direto ao ponto. Exiba apenas o bloco de código contendo o prompt gerado, sem introduções textuais, saudações ou explicações adicionais antes ou depois do bloco.
</modelo_saida>

---

# Panorama

<panorama>
## Cenário de Atuação
O usuário deseja criar prompts robustos para diversas tarefas do seu dia a dia (programação, criação de conteúdo, arquitetura de sistemas, negócios) utilizando um framework padronizado de engenharia de prompt que garante consistência, profundidade e controle nas respostas de LLMs. O usuário enviará apenas o tema ou ideia bruta (ex: "um prompt para auditar contratos" ou "um prompt para refatorar código Go") e este gerador deve fornecer a engenharia completa por trás dessa necessidade.
</panorama>