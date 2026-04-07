# LLM Gateway

Unified LLM API proxy that routes requests to multiple AI providers. Built on LiteLLM.

**URL:** https://gateway.agnxxt.com

## Features

- OpenAI-compatible API (`/v1/chat/completions`)
- Route to 100+ LLM providers (OpenAI, Anthropic, Google, Ollama, etc.)
- Per-model routing, fallbacks, and load balancing
- Request/response logging to ObserveLLM (Langfuse)
- API key management and rate limiting
- Cost tracking per model and per user

## Usage

```bash
curl -X POST "https://gateway.agnxxt.com/v1/chat/completions" \
  -H "Authorization: Bearer sk-master" \
  -H "Content-Type: application/json" \
  -d '{
    "model": "gpt-4o",
    "messages": [{"role": "user", "content": "Hello"}]
  }'
```

## Configured Models

Models are configured in `/home/ubuntu/platform/gateway/config.yaml`. All platform services use the gateway as their LLM backend.

## Integration

| Service | Connection |
|---------|-----------|
| AgentChat | `OPENAI_REVERSE_PROXY=http://gateway:4000/v1` |
| AgentStudio | `OPENAI_API_BASE=http://gateway:4000/v1` |
| AgentFlow | Via LLM components |
| n8n Bot | `https://gateway.agnxxt.com/v1/chat/completions` |

## Configuration

- Docker compose: `/home/ubuntu/platform/docker-compose.yaml` (service: `gateway`)
- Model config: `/home/ubuntu/platform/gateway/config.yaml`
- Port: 4000 (internal and external)
- Master key: `sk-master` (set via `LITELLM_MASTER_KEY`)

## Source

- Upstream: [BerriAI/litellm](https://github.com/BerriAI/litellm)
- Docs: [github.com/agentnxt/knowledgebase](https://github.com/agentnxt/knowledgebase)
