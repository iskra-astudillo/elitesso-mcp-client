# Empire Cloud SSO MCP client examples

Single sign-on you add to your own SaaS, with a free tier. Free $0, Pro $25, Business $99, Enterprise $399 a month.

This repository holds small, working examples for the hosted **Empire Cloud SSO** MCP server. It is maintained by Elite AI Empire. The server itself is hosted; nothing here runs it.

- Product: https://cloud.eliteaiempire.com/sso/
- MCP endpoint (streamable HTTP): `https://elitesso.eliteaiempire.com/mcp`
- OpenAPI: https://cloud.eliteaiempire.com/sso/openapi.json
- Pricing, machine readable: https://cloud.eliteaiempire.com/sso/pricing.json
- Discovery file: https://cloud.eliteaiempire.com/sso/.well-known/mcp.json

## Tools

| Tool | What it does |
|---|---|
| `get_company_info` | What this company sells, who it is for, and every agent/API entry point. No account needed. |
| `list_pricing` | Current plans and prices in USD: plan, interval, amount_usd, currency, what_you_get. No account needed. |
| `get_checkout_link` | Checkout URL for a plan. With no arguments: the main paid plan. Where the site supports it the URL is a Stripe-hosted Checkout session (created unpaid; a human  |
| `search_site` | Find pages on this site by keyword; returns url, title and summary. |

## Try it

```bash
bash examples/initialize.sh
python3 examples/client.py
```

`examples/client.py` uses only the Python standard library. It sends `initialize` and `tools/list` and prints the result. No key is needed for the public read tools. Tools that need an account say so in their description.

## Registry

Listed in the official MCP registry. Server manifest: `server.json`.

## Licence

MIT. See `LICENSE`.
