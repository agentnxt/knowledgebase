# Auth (Logto)

SSO and identity management for the AgentNXXT platform.

**URL:** https://auth.agnxxt.com
**Admin Console:** https://auth-admin.agnxxt.com

## OIDC Configuration

- **Issuer:** `https://auth.agnxxt.com/oidc`
- **Authorization:** `https://auth.agnxxt.com/oidc/auth`
- **Token:** `https://auth.agnxxt.com/oidc/token`
- **Userinfo:** `https://auth.agnxxt.com/oidc/me`
- **JWKS:** `https://auth.agnxxt.com/oidc/jwks`
- **Discovery:** `https://auth.agnxxt.com/oidc/.well-known/openid-configuration`

## SSO-Enabled Services

| Service | Method | Client ID |
|---------|--------|-----------|
| AgentNxt WebUI | Native OIDC | `sso-openwebui` |
| Langfuse/AgentNxt Observe | NextAuth + Logto | `sso-langfuse` |
| Dify/Studio | oauth2-proxy | `sso-dify` |
| AgentNxt Kube | Caddy forward_auth | `sso-agentkube` |
| AgentNxt Studio | Better Auth + Logto | `kakuwqj69teoec1vbetdb` |

## Admin

- Username: `chinmay`
- Email: `chinmay@openautonomyx.com`

## Database

- Host: `platform-db-1` (shared PostgreSQL)
- Database: `auth`
- User: `platform`

## Source

- Upstream: [logto-io/logto](https://github.com/logto-io/logto)
- Docs: [github.com/agentnxt/knowledgebase](https://github.com/agentnxt/knowledgebase)
