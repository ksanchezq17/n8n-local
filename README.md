# n8n-local

Local n8n + local LLMs (GPU) via Docker Compose.

## Folder structure

- `docker/compose.yaml`: main compose file
- `docker/.env`: your local environment values (create from `docker/.env.example`)
- `data/n8n/`: n8n persisted data
- `data/ollama/`: Ollama models & state
- `data/hf-cache/`: Hugging Face cache for vLLM models

## Quick start

1) Create env file:

- Copy `docker/.env.example` to `docker/.env`
- Set `N8N_ENCRYPTION_KEY` to a real secret

2) Start:

```bash
docker compose --env-file docker/.env -f docker/compose.yaml up -d
```

3) Open:

- n8n: `http://localhost:5678`
- Ollama API: `http://localhost:11434`
- vLLM (OpenAI-compatible): `http://localhost:8000/v1`

