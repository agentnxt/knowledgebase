# AgentNxt DIY

Prompt-to-agent builder with built-in RAG pipeline and conversation memory. Open-source LLMOps platform.

**URL:** https://diy.agnxxt.com
**API:** https://diy-api.agnxxt.com

## Features

- Visual prompt IDE with real-time testing
- RAG pipeline with document upload and indexing
- Conversation memory and context management
- Workflow builder for multi-step agent logic
- API endpoints for each Dify app
- Plugin ecosystem

## Architecture

| Component | Container | Port |
|-----------|-----------|------|
| API server | `dify-api` | 5001 |
| Web frontend | `dify-web` | 3000 |
| PostgreSQL | `dify-db` | 5432 |
| Redis | `dify-redis` | 6379 |

## Authentication

Protected by oauth2-proxy → Logto SSO.

- Logto Client ID: `sso-dify`
- Redirect URI: `https://diy.agnxxt.com/oauth2/callback`

## MCP Integration

Dify is available as an MCP server in AgentNxt Chat via the `dify` entry (`@tonlab/dify-mcp-server`).

## First Setup

1. Navigate to `https://diy.agnxxt.com`
2. Sign in via Logto
3. Create your admin account on first login

## Source

- Upstream: [langgenius/dify](https://github.com/langgenius/dify)
- Version: 0.15.3
- Docs: [github.com/agentnxt/knowledgebase](https://github.com/agentnxt/knowledgebase)
