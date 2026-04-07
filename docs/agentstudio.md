# AgentNxt Studio

Visual AI workflow builder and agent orchestration platform. Built on SimStudio.

**URL:** https://studio.agnxxt.com
**Realtime:** https://studio-realtime.agnxxt.com

## Features

- Visual drag-and-drop workflow builder
- Multi-agent orchestration with parallel execution
- Built-in copilot for workflow assistance
- Real-time collaboration via WebSocket
- LLM tracing via AgentNxt Observe (Langfuse)
- Integration with AgentNxt Gateway (LiteLLM)

## Architecture

| Component | Container | Port |
|-----------|-----------|------|
| Frontend (branding) | `platform-agentstudio-branding-1` | 3500 |
| Backend API | `platform-agentstudio-1` | 3000 |
| Realtime server | `platform-agentstudio-realtime-1` | 3002 |
| Database | `platform-agentstudio-db-1` | 5432 |

## Authentication

Uses Better Auth with Logto OIDC integration.

- Logto Client ID: `kakuwqj69teoec1vbetdb`
- Logto Issuer: `https://auth.agnxxt.com/oidc`
- `BETTER_AUTH_SECRET` and `BETTER_AUTH_URL` must be set on both main and realtime containers

## Connected Services

- **AgentNxt Gateway:** `http://gateway:4000/v1` (OpenAI-compatible)
- **AgentNxt Observe:** `http://observellm:3000` (Langfuse tracing)
- **SearXNG:** `http://searxng:8080` (web search tool)
- **Qdrant:** `http://qdrant:6333` (vector store)
- **Skyvern:** `http://skyvern:8000` (browser automation)

## Admin

- Email: `admin@agnxxt.com` / `chinmay@openautonomyx.com`

## Configuration

- Docker compose: `/home/ubuntu/platform/docker-compose.yaml`
- Custom branding: `/home/ubuntu/platform/agentstudio/custom/`
- Database: PostgreSQL `simstudio` on `platform-agentstudio-db-1`

## Source

- Upstream: [simstudioai/sim](https://github.com/simstudioai/sim)
- Docs: [github.com/agentnxt/knowledgebase](https://github.com/agentnxt/knowledgebase)
