<div align="center">

# tips33 · find-deals

**Your AI tells you what to buy. tips33 tells it where to pay less.**

One MCP server for ChatGPT, Claude, Gemini, Copilot, Cursor, Mistral and any AI agent.
Live offers from partner retailers, ranked by what you actually pay. No API key.

[![MCP](https://img.shields.io/badge/MCP-ready-111)](https://tips33.vercel.app/mcp)
[![Agent Skill](https://img.shields.io/badge/Agent%20Skill-find--deals-111)](skills/find-deals/SKILL.md)
[![License: MIT](https://img.shields.io/badge/license-MIT-111)](LICENSE)

</div>

---

## Install in 1 step

**In a terminal** (Claude Code, Cursor, Codex, Gemini CLI, Copilot):

```bash
npx skills add inf-opc/tips33-skills
```

**In a chat app** (ChatGPT, Claude, Claude Cowork, Le Chat): add a custom connector with this URL

```
https://tips33.vercel.app/mcp
```

**In Codex** (CLI, app or IDE):

```bash
codex mcp add tips33 --url https://tips33.vercel.app/mcp
```

Then ask: *"best trail running shoes under $200"*

Step-by-step for each AI: [INSTALL.md](INSTALL.md)

---

## Example

```
You > trail running shoes under $200

AI  > Craft Pure Trail Pro, $171 at Miles District (save $19 vs list).
      Also check current prices on Amazon.com.
      Links are affiliate (#ad).
```

Real response from the live API, October 2026.

## What it does

- Searches live partner offers (CJ, Awin, Impact, Sovrn feeds) plus a tagged Amazon.com search
- Ranks by price to pay now, then by verified savings
- Flags suspicious strikethrough discounts (above 60%)
- Returns only real data: no invented product, price, coupon or link
- Covers the US and English-speaking APAC (SG, AU, IN, PH, MY, HK)

## MCP tools

| Tool | Returns |
|---|---|
| `find_deals` | Priced offers for a query, ranked by savings |
| `search_products` | Wider product search |
| `recommend_hops` | Partner programmes when no product matches |
| `list_hops` | All live partners |

More prompts: [`examples/prompts.md`](examples/prompts.md)

## Transparency

tips33 earns an affiliate commission when you buy through its links. Your price stays the same.
Every answer says so (#ad). As an Amazon Associate, tips33 earns from qualifying purchases.
You always check out on the merchant's own site.

## Developers

- OpenAPI: https://tips33.vercel.app/openapi.json
- llms.txt: https://tips33.vercel.app/llms.txt
- MCP manifest: https://tips33.vercel.app/.well-known/mcp.json

Ideas and PRs welcome: new skills (gift finder, travel gear, back-to-school), new countries, better ranking.

If tips33 saved you money, star the repo so others find it.
