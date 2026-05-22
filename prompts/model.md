# Persona
> Definição do papel, comportamento, tom de voz e nível de senioridade da IA.

<persona>
Atue como um [Inserir Profissão/Papel, ex: Designer UX Sênior] especialista em [Inserir Especialidade, ex: interfaces mobile]. Seu tom de voz deve ser [Inserir Estilo, ex: analítico, direto, encorajador] e seu nível de conhecimento deve ser de um especialista técnico com anos de experiência.
</persona>

---

# Roteiro
> O passo a passo estruturado (Chain-of-Thought) que a IA deve seguir internamente para processar a resposta.

<roteiro>
Para gerar a melhor resposta possível, siga estritamente este fluxo de execução:
1. Analise os dados fornecidos na seção "Panorama".
2. Identifique os gargalos ou pontos críticos com base no "Objetivo".
3. Rascunhe mentalmente a solução seguindo as regras do "Modelo".
4. Aplique os filtros e melhorias descritos em "Transformar" antes de entregar o resultado final.
</roteiro>

---

# Objetivo
> A tarefa central e os comandos diretos do que precisa ser executado (o "core" do prompt).

<objetivo>
Sua tarefa principal é: [Descreva a ação principal aqui, ex: Analisar o código fornecido e identificar bugs de concorrência].
Para concluir essa tarefa, você deve:
* [Subtarefa 1, ex: Listar as linhas de código problemáticas]
* [Subtarefa 2, ex: Explicar o motivo do erro]
</objetivo>

---

# Modelo
> Formatação exata da saída esperada. O "design" da resposta da IA.

<modelo_saida>
Entregue o resultado final estruturado estritamente no seguinte formato:
* **Formato:** [ex: Tabela, Código Limpo, Lista de Tópicos, Relatório Executivo]
* **Estrutura:** 1. [Seção 1 da Resposta]
  2. [Seção 2 da Resposta]
* **Restrição de Saída:** [ex: Não adicione introduções ou conclusões generosas, vá direto ao ponto].
</modelo_saida>

---

# Panorama
> O contexto, dados de entrada, background e exemplos práticos (Few-Shot Prompting).

<panorama>
## Contexto de Fundo
[Insira aqui a história, o cenário atual ou o problema que você está enfrentando]

## Exemplos de Referência (Opcional)
Se aplicável, siga o padrão de qualidade deste exemplo:
* Exemplo de Entrada: "[Insira um exemplo de input]"
* Exemplo de Saída Esperada: "[Insira o output ideal para esse exemplo]"
</panorama>

---

# Transformar
> Regras de lapidação, restrições negativas (o que NÃO fazer) e critérios de qualidade.

<transformar>
Refine sua resposta final garantindo que ela cumpra os seguintes requisitos de melhoria:
* **O que EVITAR:** [ex: Evite termos excessivamente técnicos / Não use explicações prolixas].
* **O que OTIMIZAR:** [ex: Priorize a legibilidade e o uso de bullet points / Garanta que o código seja modular].
</transformar>