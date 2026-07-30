# Claude Code - Docker Setup

Ambiente de containerização isolado para o **Claude Code** (`@anthropic-ai/claude-code`).

## Build da Imagem

```bash
docker build -t claude-code ./claude-code
```

## Execução Interativa (com Mapeamento de Volume)

Para que os arquivos locais do seu projeto apareçam em `/workspace`:

### Linux / WSL / Bash
```bash
docker run -it --rm -v $(pwd):/workspace claude-code
```

### PowerShell (Windows)
```powershell
docker run -it --rm -v ${PWD}:/workspace claude-code
```

---

# Funcionamento com chave de API externa

## OpenRouter

```bash
export ANTHROPIC_BASE_URL="https://openrouter.ai/api/v1"
export ANTHROPIC_API_KEY="sk-or-sua-chave-openrouter"
claude --model google/gemini-2.5-pro
```

## LiteLLM Proxy

O LiteLLM age como um tradutor universal entre o Claude Code e qualquer provedor de LLM, convertendo o formato das APIs automaticamente.

**Instalar e configurar**
```bash
pip install litellm
```

Crie o arquivo `litellm-config.yaml`:

```yaml
model_list:
  # Gemini
  - model_name: gemini-2.5-pro
    litellm_params:
      model: gemini/gemini-2.5-pro
      api_key: os.environ/GEMINI_API_KEY

  # OpenAI
  - model_name: gpt-4o
    litellm_params:
      model: openai/gpt-4o
      api_key: os.environ/OPENAI_API_KEY

  # DeepSeek
  - model_name: deepseek-chat
    litellm_params:
      model: deepseek/deepseek-chat
      api_key: os.environ/DEEPSEEK_API_KEY
```

**Subir o proxy**
```bash
export GEMINI_API_KEY="sua-chave"
litellm --config litellm-config.yaml --port 4000
```

**Apontar o Claude Code para o proxy**
```bash
export ANTHROPIC_BASE_URL="http://localhost:4000"
export ANTHROPIC_API_KEY="qualquer-coisa"   # necessário mas ignorado
claude --model gemini-2.5-pro
```