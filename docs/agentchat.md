# AgentChat

AI chat interface with 28+ MCP tool integrations. Built on LibreChat.

**URL:** https://chat.agnxxt.com

## Features

- Multi-model support (GPT-4o, Claude, Gemini, local models via Ollama)
- 28+ MCP servers for filesystem, memory, GitHub, WordPress, WhatsApp, and more
- Agent Builder for creating custom AI agents with tool access
- Code Interpreter, Web Search, File Search built-in
- Artifacts for code and document generation

## MCP Tools Available

See [MCP Servers](mcp-servers.md) for the complete list.

## Authentication

Sign in with your AgentNXXT credentials via Logto SSO.

## Configuration

- Config file: `/home/ubuntu/platform/librechat/librechat.yaml`
- Docker compose: `/home/ubuntu/platform/docker-compose.yaml` (service: `librechat`)
- MCP servers are configured in `librechat.yaml` under `mcpServers:`

## API Access

AgentChat exposes an OpenAI-compatible API at `https://chat.agnxxt.com/api/`.

## Admin

- Email: chinmay@openautonomyx.com
- Password: Set during initial registration

## Source

- Upstream: [danny-avila/LibreChat](https://github.com/danny-avila/LibreChat)
- Fork: [OpenSaaSApps/LibreChat](https://github.com/OpenSaaSApps/LibreChat)
- Docs: [github.com/agentnxt/knowledgebase](https://github.com/agentnxt/knowledgebase)
- Issues: [github.com/agentnxt/knowledgebase/issues](https://github.com/agentnxt/knowledgebase/issues)
