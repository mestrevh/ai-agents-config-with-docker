# Gemini CLI - Docker Setup

Ambiente de containerização isolado para o **Gemini CLI** (`@google/gemini-cli`).

## Build da Imagem

```bash
docker buildx build -t gemini-cli ./gemini-cli
```

## Execução Interativa (com Mapeamento de Volume)

Para acessar seus arquivos locais no container na pasta `/workspace`:

### Linux / WSL / Bash
```bash
docker run -it --rm -v $(pwd):/workspace gemini-cli
```

### PowerShell (Windows)
```powershell
docker run -it --rm -v ${PWD}:/workspace gemini-cli
```

### Execução via Docker Compose
```bash
docker compose -f docker-compose-gemini.yml run --rm gemini
```
