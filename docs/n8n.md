# n8n Bot

Workflow automation platform for building event-driven integrations and chatbots.

**URL:** https://n8n-bot.agnxxt.com

## Features

- Visual workflow builder with 400+ integrations
- Webhook triggers for event-driven automation
- Code nodes (JavaScript) for custom logic
- HTTP Request nodes for API calls
- AI/LLM integration nodes

## Active Workflows

### WhatsApp AI Chatbot

**ID:** `imHA91fZTp39zBvC`

Flow: WhatsApp message → WuzAPI webhook → n8n → LLM Gateway (GPT-4o) → WuzAPI reply

| Node | Purpose |
|------|---------|
| WhatsApp Webhook | Receives POST from WuzAPI at `/webhook/whatsapp-bot` |
| Extract Message | Parses sender phone and message text from WuzAPI payload |
| Filter Valid Messages | Skips non-text messages and self-messages |
| Call LLM | Sends message to `gateway.agnxxt.com` → GPT-4o |
| Send WhatsApp Reply | Posts LLM response back via WuzAPI |

## Authentication

- Email: `chinmay@openautonomyx.com`
- Password: `Static@12`
- API Key: Generated at Settings → n8n API

## Configuration

Standalone Docker container:

```bash
docker run -d --name n8n-bot \
  --network platform_frontend \
  -p 5678:5678 \
  -v n8n-bot-data:/home/node/.n8n \
  -e WEBHOOK_URL=https://n8n-bot.agnxxt.com \
  n8nio/n8n:latest
```

## MCP Integration

Available as an MCP server in AgentChat via the `n8n` entry (`@leonardsellem/n8n-mcp-server`).

## Source

- Upstream: [n8n-io/n8n](https://github.com/n8n-io/n8n)
- Version: 2.14.2
- Docs: [github.com/agentnxt/knowledgebase](https://github.com/agentnxt/knowledgebase)
