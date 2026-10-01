<div align="center">

# tips33 · find-deals

**Your AI finds the right product. Now it finds the best price too.**

One skill. One MCP server. Zero API keys.
Ask Claude, Cursor or any agent *"best X under $Y"* and get live offers ranked by real savings.

[![MCP](https://img.shields.io/badge/MCP-ready-111)](https://tips33.vercel.app/mcp)
[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-find--deals-111)](skills/find-deals/SKILL.md)
[![License: MIT](https://img.shields.io/badge/license-MIT-111)](LICENSE)

</div>

---

## 30-second install

**Claude Code**

```bash
claude mcp add --transport http tips33 https://tips33.vercel.app/mcp
```

Or install the full plugin (MCP + skill):

```
/plugin marketplace add Lilouoz/tips33-skills
/plugin install tips33@tips33
```

**Claude.ai / Claude Desktop**
Settings → Connectors → Add custom connector → `https://tips33.vercel.app/mcp` → No authentication.

**Cursor / Windsurf / any MCP client**

```json
{ "mcpServers": { "tips33": { "type": "http", "url": "https://tips33.vercel.app/mcp" } } }
```

**Any agent with Agent Skills**
Copy [`skills/find-deals`](skills/find-deals) into your skills folder.

**No MCP at all?** Plain HTTP works:

```bash
curl "https://tips33.vercel.app/api/recommend?q=standing+desk&country=US&deals=1&max_price=300"
```

---

## What you get

```
You  > best noise cancelling headphones under $200

AI   > 3 picks for travel + calls, under $200:
       1. Brand A ANC — $149 at Merchant X (save $50) · best battery
       2. Brand B Pro — $179 at Merchant Y · best mic for calls
       3. Search on Amazon.com → check current price
       Verdict: take #1 unless you live on Zoom.
       Links are affiliate (#ad).
```

- **Live offers** from partner retailers, not stale training data
- **Ranked by what you pay now**, with real savings only
- **Fake discounts filtered** (strikethrough > 60% is flagged)
- **Never invents** a coupon, price or link
- **US + English-speaking APAC** (SG, AU, IN, PH, MY, HK, JP, KR)

## Tools

| Tool | Does |
|---|---|
| `find_deals` | Priced offers for a query, ranked by real savings |
| `search_products` | Broader product search |
| `recommend_hops` | Partner programmes when no SKU matches |
| `list_hops` | All live partners |

## Prompts to try

See [`examples/prompts.md`](examples/prompts.md). Start with:
*"I need a standing desk for a small apartment, budget $300."*

## How it stays honest

tips33 earns an affiliate commission when you buy through its links. **Your price stays the same.**
Every answer discloses it (#ad). As an Amazon Associate, tips33 earns from qualifying purchases.
tips33 is a discovery layer: you always check out on the merchant's own site.

## Build on it

- OpenAPI: https://tips33.vercel.app/openapi.json
- llms.txt: https://tips33.vercel.app/llms.txt
- MCP manifest: https://tips33.vercel.app/.well-known/mcp.json

PRs welcome: new skills (gift finder, back-to-school, travel gear), better ranking, more countries.

If it saved you money, **star the repo** so other people find it.
