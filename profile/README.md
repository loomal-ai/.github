# Loomal

**Identity infrastructure for AI agents.**

Loomal gives every AI agent its own real identity — an email address it can send and receive on, a vault for credentials and TOTP, a calendar, and an audit log. Agents act as themselves, not as you.

[loomal.ai](https://loomal.ai) · [Docs](https://docs.loomal.ai) · [Console](https://console.loomal.ai)

---

## What's in the box

- **Email** — every identity gets an inbox at `name@loomal.ai`. Send, reply, label, thread.
- **Vault** — password-manager-style storage for API keys, payment cards, shipping addresses, and TOTP secrets. AES-256-GCM at rest.
- **Calendar** — schedule, share, and resolve events under the agent's identity.
- **DID** — every identity is resolvable as a [decentralized identifier](https://www.w3.org/TR/did-core/), so other agents can verify who they're talking to.
- **Audit log** — every action the agent takes is recorded and queryable.

## Get started

Grab an API key from the [console](https://console.loomal.ai), then plug it into whatever you're building with:

| | Install | Repo |
|---|---|---|
| **MCP server** | `npx -y @loomal/mcp` | [loomal-mcp](https://github.com/loomal-ai/loomal-mcp) |
| **Node SDK** | `npm install @loomal/sdk` | [loomal-node](https://github.com/loomal-ai/loomal-node) |
| **Python SDK** | `pip install loomal-sdk` | [loomal-python](https://github.com/loomal-ai/loomal-python) |
| **CLI** | `npm install -g @loomal/cli` | [loomal-cli](https://github.com/loomal-ai/loomal-cli) |

## In practice

Drop the MCP server into Claude, Cursor, or any MCP-aware client:

```json
{
  "mcpServers": {
    "loomal": {
      "command": "npx",
      "args": ["-y", "@loomal/mcp"],
      "env": { "LOOMAL_API_KEY": "YOUR_API_KEY" }
    }
  }
}
```

Then ask your agent:

> Send an onboarding email to the new client.
> Store my Stripe API key in the vault.
> Get the TOTP code for my AWS account.
> Book a 30-minute slot with their team for next Tuesday.

## Links

- Website — [loomal.ai](https://loomal.ai)
- Docs — [docs.loomal.ai](https://docs.loomal.ai)
- Console — [console.loomal.ai](https://console.loomal.ai)
