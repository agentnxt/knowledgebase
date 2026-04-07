# AgentKube

AI agent control plane for managing, monitoring, and orchestrating agents at scale. Built on AgentField.

**URL:** https://agentkube.agnxxt.com
**Health:** https://agentkube.agnxxt.com/api/v1/health

## Features

- Agent lifecycle management (create, deploy, monitor, stop)
- Built-in SQLite + BoltDB (no external database needed)
- REST API for programmatic agent management
- React/TypeScript dashboard UI
- Runs as non-root user (UID 65532) in distroless container

## Architecture

- **Runtime:** Go 1.24 binary + React frontend
- **Storage:** SQLite (metadata) + BoltDB (key-value)
- **Container:** `gcr.io/distroless/static-debian12` (minimal attack surface)
- **Port:** 8080 (internal), 9091 (host), proxied via Caddy

## Authentication

Protected by Caddy `forward_auth` → oauth2-proxy → Logto SSO.

- Logto Client ID: `sso-agentkube`

## API

```bash
# Health check
curl https://agentkube.agnxxt.com/api/v1/health

# Response
{
  "status": "healthy",
  "checks": {
    "cache": {"status": "healthy"},
    "storage": {"status": "healthy"}
  },
  "version": "1.0.0"
}
```

## Deployment

Deployed via Docker directly (not Coolify):

```bash
docker run -d --name agentkube \
  --restart unless-stopped \
  -p 9091:8080 \
  -v agentkube-data:/data \
  agentkube:latest
```

Built from source at `/opt/agentkube` using `deployments/docker/Dockerfile.control-plane`.

## Source

- Upstream: [Agent-Field/agentfield](https://github.com/Agent-Field/agentfield)
- Fork: [agentnxt/agentkube](https://github.com/agentnxt/agentkube)
- Docs: [github.com/agentnxt/knowledgebase](https://github.com/agentnxt/knowledgebase)
