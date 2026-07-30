# AI Agents & Docker Hub

Repositório para isolamento, padronização e execução de Agentes de IA via containers Docker.

## Visão Geral dos Agentes

| Agente | Diretório | Comando de Build |
| :--- | :--- | :--- |
| **Antigravity CLI** | [`antigravity-cli/`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/antigravity-cli) | `docker build -t antigravity-cli ./antigravity-cli` |
| **Claude Code** | [`claude-code/`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/claude-code) | `docker build -t claude-code ./claude-code` |
| **Gemini CLI** | [`gemini-cli/`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/gemini-cli) | `docker build -t gemini-cli ./gemini-cli` |
| **Hermes Agent** | [`hermes/`](file:///c:/Users/Victo/Desktop/Pessoal/ai-agents-config-with-docker/hermes) | `docker build -t hermes-agent ./hermes` |

---

## Como Executar (Mapeamento de Volume Obrigatório)

Para que o container acesse os arquivos do seu projeto local, é **obrigatório** utilizar a flag `-v` para montar a pasta atual em `/workspace`.

### Linux / WSL / Bash
```bash
docker run -it --rm -v $(pwd):/workspace <NOME_DA_IMAGEM>
```

### PowerShell (Windows)
```powershell
docker run -it --rm -v ${PWD}:/workspace <NOME_DA_IMAGEM>
```

---

## Comandos Rápidos por Agente

### 1. Antigravity CLI
```bash
docker build -t antigravity-cli ./antigravity-cli
docker run -it --rm -v $(pwd):/workspace antigravity-cli
```

### 2. Claude Code
```bash
docker build -t claude-code ./claude-code
docker run -it --rm -v $(pwd):/workspace claude-code
```

### 3. Gemini CLI
```bash
docker build -t gemini-cli ./gemini-cli
docker run -it --rm -v $(pwd):/workspace gemini-cli
```

### 4. Hermes Agent
```bash
docker build -t hermes-agent ./hermes
docker run -it --rm -e OPENROUTER_API_KEY="sua-chave" -v $(pwd):/workspace hermes-agent
```