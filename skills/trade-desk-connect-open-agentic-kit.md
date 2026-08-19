---
name: Connect an agent to The Trade Desk Open Agentic Kit (OAK)
description: Configure an MCP client against The Trade Desk's remote MCP server, choose an auth method, and understand what OAK can and cannot do today.
api: mcp/trade-desk-mcp.yml
operations: []
generated: '2026-08-13'
method: generated
source: https://open.thetradedesk.com/advertiser/docsApp/Foundations/resources/doc/McpOpenAgenticKitGettingStarted
---

# Connect an agent to Open Agentic Kit

## Access is gated

OAK entered private beta on 10 August 2026 and is available to selected partners only. Register interest through your Trade Desk account representative. Without an approved credential every call to the endpoint returns `401 Unauthorized` from the gateway — including `tools/list`, so an unapproved client cannot even enumerate the surface.

## Configure the client

OAK is a **remote** MCP server. There is nothing to install.

```json
{
  "mcpServers": {
    "ttd-platform": {
      "url": "https://api.thetradedesk.com/mcp/platform-management",
      "headers": {
        "TTD-Auth": "<your Platform API token>"
      }
    }
  }
}
```

## Choose an auth method

| Method | When to use |
|---|---|
| Token (`TTD-Auth` header) | Default. Generate the token in OpenTTD Access Management, same token type as the REST and GraphQL APIs. |
| OAuth | No manual token management. The resource publishes RFC 9728 metadata at `https://api.thetradedesk.com/.well-known/oauth-protected-resource/mcp/platform-management`, naming `https://auth.thetradedesk.com` as the authorization server and `openid profile email offline_access ttdapi` as the supported scopes. |
| OIDC | For teams building their own applications on top of OAK. Available on request. |

## What you can do today

Read-only and safe to enable broadly: **Knowledge Search**, **Data Retrieval**, **Reporting**.

Arriving in H2 2026: **Configuration & Management**, **Insights**, **Troubleshooting**.

## Guardrails that already exist

- Every request runs through The Trade Desk's standard authorization layer. The agent sees exactly what the human operator would see in the platform UI — no more.
- Tokens can be scoped, so a data-access agent need not carry modification permissions.
- When Configuration & Management ships, writes follow a propose-confirm-execute flow enforced **at the platform level**, not only in the client. Client-side approval settings are an additional layer, not the only one.

## What this skill does not cover

There is no published tool inventory and no published input schemas — the capability table above is the whole of what the provider documents. Do not assume tool names. Let the client discover them at connect time.
