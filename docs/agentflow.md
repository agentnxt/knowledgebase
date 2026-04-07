# AgentNxt Flow

Low-code AI pipeline designer for building RAG, multi-agent, and tool-augmented workflows. Built on Langflow.

**URL:** https://agentflow.agnxxt.com

## Features

- Visual flow builder with drag-and-drop components
- Pre-built components for LLMs, vector stores, embeddings, tools
- Export flows as Python code or API endpoints
- Multi-model support via AgentNxt Gateway
- RAG pipeline builder with document loaders and vector stores
- MCP server support for external tool integration

## Authentication

- Auto-login enabled (`LANGFLOW_AUTO_LOGIN=true`)
- Superuser: `admin` / `admin`
- Database: PostgreSQL `agentflow` on shared `platform-db-1`

## Configuration

- Docker compose: `/home/ubuntu/platform/docker-compose.yaml` (service: `agentflow`)
- Config dir: `/app/langflow` (inside container)
- Port: 7860 (internal), proxied via Caddy

## API

AgentNxt Flow exposes a REST API for programmatic flow execution:

```bash
curl -X POST "https://agentflow.agnxxt.com/api/v1/run/<flow_id>" \
  -H "Content-Type: application/json" \
  -d '{"input_value": "your input"}'
```

## MCP Integration

AgentNxt Flow is available as an MCP server in AgentNxt Chat via the `langflow` MCP entry, allowing agents to execute flows programmatically.

## Source

- Upstream: [langflow-ai/langflow](https://github.com/langflow-ai/langflow)
- Fork: [OpenSaaSApps/langflow](https://github.com/OpenSaaSApps/langflow)
- Docs: [github.com/agentnxt/knowledgebase](https://github.com/agentnxt/knowledgebase)
