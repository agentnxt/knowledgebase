# Grafana

Unified monitoring dashboards for the AgentNXXT platform.

**URL:** https://grafana.agnxxt.com

## Features

- Pre-built dashboards for all platform services
- Prometheus data source for metrics
- Alert rules and notification channels
- Custom dashboard creation

## Data Sources

- **Prometheus:** `http://prometheus:9090` (metrics)

## Configuration

- Docker compose: `/home/ubuntu/platform/docker-compose.yaml` (service: `grafana`)
- Port: 3000 (internal)

## MCP Integration

Available as an MCP server in AgentNxt Chat via the `grafana` entry (`mcp-grafana` uvx). Requires `GRAFANA_SERVICE_ACCOUNT_TOKEN` env var.

## Source

- Upstream: [grafana/grafana](https://github.com/grafana/grafana)
- Docs: [github.com/agentnxt/knowledgebase](https://github.com/agentnxt/knowledgebase)
