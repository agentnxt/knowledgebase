# MCP Servers

AgentChat includes the following Model Context Protocol servers, available as tools when creating agents.

## Official Anthropic Reference Servers

| Server | Package | Tools |
|--------|---------|-------|
| **filesystem** | `@modelcontextprotocol/server-filesystem` | Read/write files |
| **memory** | `@modelcontextprotocol/server-memory` | Persistent knowledge graph |
| **fetch** | `mcp-server-fetch` (uvx) | Web content fetching |
| **git** | `mcp-server-git` (uvx) | Git repo operations |
| **sequential-thinking** | `@modelcontextprotocol/server-sequential-thinking` | Step-by-step problem solving |
| **time** | `mcp-server-time` (uvx) | Time/timezone queries |
| **github** | `@modelcontextprotocol/server-github` | GitHub API (repos, issues, PRs) |

## Platform Integrations

| Server | Package | Tools |
|--------|---------|-------|
| **wordpress** | `@automattic/mcp-wordpress-remote` | WordPress CMS operations |
| **woocommerce** | `woocommerce-mcp-server` | WooCommerce store management |
| **meta-ads** | `meta-ads-mcp-server` | Facebook/Instagram Ads |
| **meta-pages** | `mcp-facebook` | Facebook Pages management |
| **dify** | `@tonlab/dify-mcp-server` | Dify AI workflows |

## AgentNXXT Custom MCP Servers

Built by AgentNXXT, source at [agentnxt/mcpservers](https://github.com/agentnxt/mcpservers).

| Server | Tools |
|--------|-------|
| **logto** | Auth & user management (Logto Management API) |
| **wuzapi** | WhatsApp messaging (35 tools: send text/image/video, groups, contacts) |
| **ghost** | Ghost CMS (posts, pages, members, tags) |
| **liferay** | Liferay CMS (web content, structures, categories) |

## Observability & Databases

| Server | Package | Tools |
|--------|---------|-------|
| **grafana** | `mcp-grafana` (uvx) | Dashboards, PromQL queries, alerts |
| **qdrant** | `better-qdrant-mcp-server` | Vector database operations |
| **surrealdb** | `surrealdb-mcp-server` | SurrealDB queries |

## Workflow & Automation

| Server | Package | Tools |
|--------|---------|-------|
| **n8n** | `@leonardsellem/n8n-mcp-server` | Workflow management |
| **temporal** | `@vreme/temporal-mcp` | Temporal intelligence |

## Internal Platform

| Server | Connection | Tools |
|--------|-----------|-------|
| **simstudio** | `http://agentstudio:3000` | AgentStudio workflow execution |
| **langflow** | `http://agentflow:7860` | AgentFlow pipeline execution |

## Configuration

All MCP servers are configured in `/home/ubuntu/platform/librechat/librechat.yaml`.

Servers using `npx` download packages on first use. Servers using `uvx` require Python. Both are available in the LibreChat container.

## Environment Variables

Many MCP servers require API keys set as environment variables in the LibreChat docker-compose service. See each server's section for required env vars.
