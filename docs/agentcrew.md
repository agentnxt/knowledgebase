# AgentNxt Crew

Multi-agent orchestration framework for building teams of AI agents. Built on CrewAI with Streamlit UI.

**URL:** https://agentcrew.agnxxt.com

## Features

- Define agent roles, goals, and backstories
- Create tasks with expected outputs and dependencies
- Sequential and hierarchical process execution
- Tool integration (web search, file operations, APIs)
- Streamlit-based web interface

## Architecture

| Component | Container |
|-----------|-----------|
| Streamlit UI | `platform-agentcrew-1` |
| Nginx proxy | `platform-agentcrew-proxy-1` |

## Authentication

Streamlit built-in auth. No SSO integration (Streamlit limitation).

## MCP Integration

AgentNxt Crew is available as an MCP server in AgentNxt Chat. A standalone CrewAI MCP server runs at `crewai-mcp:8080` with two pre-configured agents:

- **Research Analyst** — finds and analyzes information
- **Content Writer** — creates content from research

## Configuration

- Docker compose: `/home/ubuntu/platform/docker-compose.yaml` (service: `agentcrew`)
- Streamlit config: `/app/.streamlit/config.toml` (inside container)

## Source

- Upstream: [crewAIInc/crewAI](https://github.com/crewAIInc/crewAI)
- Fork: [OpenSaaSApps/agentcrew](https://github.com/OpenSaaSApps/agentcrew)
- Docs: [github.com/agentnxt/knowledgebase](https://github.com/agentnxt/knowledgebase)
