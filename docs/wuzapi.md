# WuzAPI

WhatsApp REST API service using the Whatsmeow library. Communicates directly with WhatsApp WebSocket servers.

**URL:** https://wuzapi.agnxxt.com
**Dashboard:** https://wuzapi.agnxxt.com/dashboard

## Features

- Multi-device support with concurrent sessions
- Send text, images, audio, video, documents, locations, contacts, polls
- Group management (create, invite, manage participants)
- Webhook callbacks for incoming messages
- HMAC-based webhook signature verification

## Authentication

- **User token:** `mcp-wuzapi-token-2026` (for MCP agent)
- **Admin token:** `wuzapi-admin-2026-agnxxt`
- Header: `token: <your-token>`

## WhatsApp Chatbot

A WhatsApp AI chatbot is configured using n8n:

1. Incoming WhatsApp message → WuzAPI webhook
2. Webhook → n8n at `https://n8n-bot.agnxxt.com/webhook/whatsapp-bot`
3. n8n → LLM Gateway (`gateway.agnxxt.com`) → GPT-4o
4. LLM response → WuzAPI → WhatsApp reply

**n8n Workflow:** WhatsApp AI Chatbot (ID: `imHA91fZTp39zBvC`)

## Pairing

1. Go to https://wuzapi.agnxxt.com/dashboard
2. Login with token: `mcp-wuzapi-token-2026`
3. Click Connect
4. Scan QR code with WhatsApp (Settings → Linked Devices → Link a Device)

## MCP Server

The WuzAPI MCP server exposes 35 WhatsApp tools in AgentChat. Source: [agentnxt/mcpservers/wuzapi-mcp-server](https://github.com/agentnxt/mcpservers)

## API Endpoints

| Category | Endpoints |
|----------|-----------|
| Session | connect, disconnect, logout, status, qr, pairphone |
| Messaging | send text/image/audio/video/document/location/contact/poll, react, delete, edit |
| Users | check, info, avatar, contacts, presence |
| Groups | create, list, info, invite link, manage participants, set name/topic |
| Webhooks | set, get, update, delete |
| Status | set status message |

## Source

- Upstream: [asternic/wuzapi](https://github.com/asternic/wuzapi)
- Docs: [github.com/agentnxt/knowledgebase](https://github.com/agentnxt/knowledgebase)
