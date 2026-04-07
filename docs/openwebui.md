# OpenWebUI

Local LLM chat interface with model management and RAG support.

**URL:** https://openwebui.agnxxt.com

## Features

- Chat with local models via Ollama
- Chat with cloud models via LLM Gateway
- Document upload and RAG
- Model management and switching
- Conversation history and search

## Authentication

Native OIDC integration with Logto SSO.

- Logto Client ID: `sso-openwebui`
- Provider name: `AgentNXXT`
- Redirect URI: `https://openwebui.agnxxt.com/oauth/oidc/callback`
- "Sign in with AgentNXXT" button on login page

## Admin

- First registered user becomes admin
- Email: `chinmay@openautonomyx.com`

## Configuration

Standalone Docker container (not in platform compose):

```bash
docker run -d --name openwebui \
  --network platform_frontend \
  -p 3080:8080 \
  -v openwebui-data:/app/backend/data \
  -e ENABLE_OAUTH_SIGNUP=true \
  -e OAUTH_PROVIDER_NAME=AgentNXXT \
  -e OPENID_PROVIDER_URL=https://auth.agnxxt.com/oidc/.well-known/openid-configuration \
  -e OAUTH_CLIENT_ID=sso-openwebui \
  -e OAUTH_CLIENT_SECRET=OpenWebUISSO2026Secret \
  ghcr.io/open-webui/open-webui:main
```

## Source

- Upstream: [open-webui/open-webui](https://github.com/open-webui/open-webui)
- Docs: [github.com/agentnxt/knowledgebase](https://github.com/agentnxt/knowledgebase)
