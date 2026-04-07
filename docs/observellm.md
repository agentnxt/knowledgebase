# ObserveLLM

LLM observability, tracing, and evaluation platform. Built on Langfuse.

**URL:** https://observellm.agnxxt.com

## Features

- LLM call tracing with latency, cost, and token tracking
- Prompt management with versioning
- Evaluation framework for LLM outputs
- Dataset management for testing
- Dashboard with usage analytics

## Authentication

NextAuth with Logto OIDC provider.

- Logto Client ID: `sso-langfuse`
- Issuer: `https://auth.agnxxt.com/oidc`
- "Sign in with Logto" button on login page

## Admin

- Email: `chinmay@openautonomyx.com`
- Admin flag: `true`

## Integration

All platform services send traces to ObserveLLM:

| Service | Integration |
|---------|-------------|
| AgentChat | `LANGFUSE_BASE_URL=http://observellm:3000` |
| AgentStudio | `LANGFUSE_HOST=http://observellm:3000` |
| AgentFlow | `LANGFUSE_HOST=http://observellm:3000` |
| LLM Gateway | `LANGFUSE_HOST=http://observellm:3000` |

## API Keys

Generate API keys at `https://observellm.agnxxt.com/settings` → API Keys.

- Public key: Used in `LANGFUSE_PUBLIC_KEY` env var
- Secret key: Used in `LANGFUSE_SECRET_KEY` env var

## Configuration

- Docker compose: `/home/ubuntu/platform/docker-compose.yaml` (service: `observellm`)
- Database: PostgreSQL `observellm` on shared `platform-db-1`
- Port: 3150 (host), 3000 (internal)

## Source

- Upstream: [langfuse/langfuse](https://github.com/langfuse/langfuse)
- Version: 2.x
- Docs: [github.com/agentnxt/knowledgebase](https://github.com/agentnxt/knowledgebase)
