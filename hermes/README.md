# Hermes Agent - Docker Setup

Ambiente de containerização isolado para o **Hermes Agent** (Nous Research).

## Build da Imagem

```bash
docker buildx build -t hermes-agent ./hermes
```

## Execução Interativa (com Mapeamento de Volume)

Para que os arquivos locais do seu projeto apareçam em `/workspace`:

### Linux / WSL / Bash
```bash
docker run -it --rm -e OPENROUTER_API_KEY="sua-chave" -v $(pwd):/workspace hermes-agent
```

### PowerShell (Windows)
```powershell
docker run -it --rm -e OPENROUTER_API_KEY="sua-chave" -v ${PWD}:/workspace hermes-agent
```

---

# Configurações Internas do Hermes

Ao iniciar no container, configure o Hermes:

```bash
hermes setup
```

Caso queira definir a chave de API do OpenRouter e alterar o modelo:

```bash
export OPENROUTER_API_KEY="sua-chave-aqui"
hermes
```

Ou via comandos de configuração:

```bash
hermes config set model anthropic/claude-opus-4.6
hermes config set OPENROUTER_API_KEY sua-chave-aqui
hermes
```