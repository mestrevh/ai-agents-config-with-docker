# Funcionamento do hermes

Configuração do hermes ao iniciar:

```bash
hermes setup
```

Caso não se conecte nos modelos utilize esse comando e escolha com `/model`:
```bash
export OPENROUTER_API_KEY="sua-chave-aqui"
hermes
```

Outra maneira de fazer essa **configuração**
```bash
hermes config set model anthropic/claude-opus-4.6
hermes config set OPENROUTER_API_KEY sua-chave-aqui
hermes
```