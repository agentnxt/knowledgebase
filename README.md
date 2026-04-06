# AgentNXXT Knowledge Base

Documentation and guides for the AgentNXXT AI Platform.

## Platform Services

| Service | URL | Description |
|---------|-----|-------------|
| [AgentChat](docs/agentchat.md) | `chat.agnxxt.com` | AI chat interface with MCP tools |
| [AgentStudio](docs/agentstudio.md) | `agentstudio.agnxxt.com` | Visual AI workflow builder |
| [AgentFlow](docs/agentflow.md) | `agentflow.agnxxt.com` | Low-code agent pipeline designer |
| [AgentCrew](docs/agentcrew.md) | `agentcrew.agnxxt.com` | Multi-agent orchestration |
| [AgentKube](docs/agentkube.md) | `agentkube.agnxxt.com` | Agent control plane |
| [AgentSearch](docs/agentsearch.md) | `search.agnxxt.com` | Privacy-respecting meta search |
| [Dify Studio](docs/dify.md) | `studio.agnxxt.com` | Prompt-to-agent builder |
| [OpenWebUI](docs/openwebui.md) | `openwebui.agnxxt.com` | Local LLM chat interface |
| [ObserveLLM](docs/observellm.md) | `observellm.agnxxt.com` | LLM observability & tracing |

## Infrastructure

| Service | URL | Description |
|---------|-----|-------------|
| [LLM Gateway](docs/gateway.md) | `gateway.agnxxt.com` | Unified LLM API proxy (LiteLLM) |
| [Auth (Logto)](docs/auth.md) | `auth.agnxxt.com` | SSO & identity management |
| [n8n Bot](docs/n8n.md) | `n8n-bot.agnxxt.com` | Workflow automation |
| [WuzAPI](docs/wuzapi.md) | `wuzapi.agnxxt.com` | WhatsApp REST API |
| [Grafana](docs/grafana.md) | `grafana.agnxxt.com` | Monitoring dashboards |
| [Prometheus](docs/prometheus.md) | `prometheus.agnxxt.com` | Metrics collection |
| [Temporal](docs/temporal.md) | `temporal.agnxxt.com` | Workflow orchestration |
| [Camunda](docs/camunda.md) | `camunda.agnxxt.com` | Decision automation |

## MCP Servers

AgentChat includes 28+ MCP (Model Context Protocol) servers. See [MCP Servers](docs/mcp-servers.md) for the full list.

## Getting Started

1. Sign in at [auth.agnxxt.com](https://auth.agnxxt.com) with your Logto credentials
2. Access any service — SSO keeps you logged in across all `*.agnxxt.com` services
3. Start with [AgentChat](https://chat.agnxxt.com) to chat with AI using all available tools

## Source Code

| Repository | Description |
|-----------|-------------|
| [agentnxt/agentkube](https://github.com/agentnxt/agentkube) | Agent control plane (Go) |
| [agentnxt/agent-skills](https://github.com/agentnxt/agent-skills) | Custom agent skills |
| [agentnxt/mcpservers](https://github.com/agentnxt/mcpservers) | Custom MCP servers (Logto, Ghost, Liferay, WuzAPI) |
| [agentnxt/knowledgebase](https://github.com/agentnxt/knowledgebase) | This documentation |

## Support

- Issues: [github.com/agentnxt/knowledgebase/issues](https://github.com/agentnxt/knowledgebase/issues)
- Email: chinmay@openautonomyx.com
