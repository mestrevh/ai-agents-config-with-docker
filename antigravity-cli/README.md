# Antigravity CLI - Docker Setup

Ambiente de containerização isolado para o **Antigravity CLI**.

## Build da Imagem

```bash
docker build -t antigravity-cli ./antigravity-cli
```

## Execução Interativa (com Mapeamento de Volume)

Para acessar seus arquivos locais no container na pasta `/workspace`:

### Linux / WSL / Bash
```bash
docker run -it --rm -v $(pwd):/workspace antigravity-cli
```

### PowerShell (Windows)
```powershell
docker run -it --rm -v ${PWD}:/workspace antigravity-cli
```
