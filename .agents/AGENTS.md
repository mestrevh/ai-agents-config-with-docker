# AI Agents & Docker Hub - Regras & Diretrizes do Workspace

Este repositório serve para **isolamento, configuração, padronização e execução de Agentes de Inteligência Artificial CLI via containers Docker**, além de gerenciar **prompts estruturados e habilidades (skills)** reutilizáveis.

---

## Visão Geral dos Agentes Suportados

| Agente | Diretório | Descrição / Imagem | Casos de Uso Principais |
| :--- | :--- | :--- | :--- |
| **Antigravity CLI** | [`antigravity-cli/`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/antigravity-cli) | Imagem `ubuntu:latest` com instalador `antigravity.google/cli` | Pair programming, tarefas autônomas multi-ferramentas e automações avançadas. |
| **Claude Code** | [`claude-code/`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/claude-code) | Imagem `ubuntu:latest` + Node.js 20 com `@anthropic-ai/claude-code` | Refatoração de código, navegação em repositórios complexos e suporte a LiteLLM / OpenRouter. |
| **Gemini CLI** | [`gemini-cli/`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/gemini-cli) | Imagem `ubuntu:latest` + Node.js 20 com `@google/gemini-cli` | Tarefas de raciocínio rápido, contextos extensos e chamadas de modelos Gemini. |
| **Hermes Agent** | [`hermes/`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/hermes) | Imagem `ubuntu:latest` com instalador `hermes-agent.nousresearch.com` | Agente open-source personalizável e integrações via OpenRouter. |

---

## Padrões de Isolamento e Docker

Ao criar ou atualizar configurações de agentes de IA neste repositório, siga rigorosamente as regras:

1. **Base Limpa e Reprodutível**:
   - Utilize imagens base leves e consistentes (`ubuntu:latest` ou imagens oficiais específicas).
   - Defina `ENV DEBIAN_FRONTEND=noninteractive` em Dockerfiles para instalações não interativas.
   - Limpe os caches do gerenciador de pacotes (`rm -rf /var/lib/apt/lists/*`) após instalações `apt-get`.

2. **Diretório de Trabalho (`WORKDIR`)**:
   - O volume padrão de montagem e trabalho dentro dos containers DEVE ser `/workspace`.
   - Monte os projetos locais no container mapeando o diretório atual: `-v ${PWD}:/workspace`.

3. **Segurança e Variáveis de Ambiente**:
   - **NUNCA** inclua chaves de API (`OPENAI_API_KEY`, `ANTHROPIC_API_KEY`, `GEMINI_API_KEY`, `OPENROUTER_API_KEY`) diretamente em Dockerfiles ou commite arquivos `.env` sensíveis.
   - Trate as credenciais via variáveis de ambiente injetadas no momento do `docker run` ou `docker compose` (`-e VAR=VAL` ou arquivo `.env` ignorado no `.gitignore`).

4. **Proxies e Tradução de API**:
   - Para provedores não nativos (ex: usar Gemini/OpenAI com Claude Code), priorize o uso de `LiteLLM` ou `OpenRouter` conforme documentado em [`claude-code/README.md`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/claude-code/README.md) e [`hermes/README.md`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/hermes/README.md).

---

## Framework Standard de Prompts (6 Etapas)

Todo prompt ou agente construído/executado neste ambiente deve respeitar a estrutura estipulada em [`prompts/model.md`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/prompts/model.md):

1. **`<persona>`**: Papel, senioridade, tom de voz e especialidade da IA.
2. **`<roteiro>`**: Fluxo de pensamento em cadeia (Chain-of-Thought) estrito que o agente deve seguir.
3. **`<objetivo>`**: Tarefa central e sub-tarefas explícitas.
4. **`<modelo_saida>`**: Estrutura exata da resposta (formato, lista, código, sem introduções/conclusões desnecessárias).
5. **`<panorama>`**: Contexto de fundo, estado atual e exemplos few-shot de entrada/saída.
6. **`<transformar>`**: Regras de lapidação, restrições negativas (o que evitar) e critérios de qualidade.

---

## Governança de Skills e Regras

### Habilidades (`.agents/skills/`)
- Cada nova habilidade deve residir em seu próprio diretório em [`.agents/skills/`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/.agents/skills/).
- O arquivo principal deve obrigatoriamente se chamar `SKILL.md` e conter cabeçalho YAML com `name` e `description`.
- Exemplo de estrutura existente:
  - [`gerador-de-prompts-framework`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/.agents/skills/gerador-de-prompts-framework/SKILL.md)
  - [`gerador-de-skills`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/.agents/skills/gerador-de-skills/SKILL.md)

### Regras do Projeto (`.agents/rule/`)
- Mantenha especificações técnicas e de arquitetura em [`.agents/rule/`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/.agents/rule/).
- Respeite as tags `<persona>`, `<arquitetura>` e `<transformar>` descritas em [`architecture.md`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/.agents/rule/architecture.md).

---

## Dashboard Visual e Documentação

- Qualquer alteração na estrutura de agentes ou adição de novas configurações deve ser refletida na interface visual [`index.html`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/index.html).
- O arquivo [`README.md`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/README.md) deve manter comandos rápidos de `docker compose` / `docker run` atualizados.
