# Install tips33 in your AI

## One command (any coding agent)

```bash
npx skills add inf-opc/tips33-skills
```

Skills included: `find-deals` · `price-check` · `gift-finder`

---

## Claude Cowork

1. Claude desktop app → Settings → Connectors → Add custom connector.
2. Name `tips33`, URL `https://tips33.vercel.app/mcp`, authentication: none.
3. In a Cowork task, ask: *"best trail running shoes under $200"*.

Optional, the skills too: Settings → Capabilities → Skills → upload a zip of `skills/find-deals` (same for `price-check`, `gift-finder`).

## Codex (CLI, desktop app, IDE extension)

```bash
codex mcp add tips33 --url https://tips33.vercel.app/mcp
```

The CLI, app and IDE extension share the same config (`~/.codex/config.toml`), so one command covers all three. Add the skills with `npx skills add inf-opc/tips33-skills` and pick Codex.

## Works with every AI

| AI | Install |
|---|---|
| **ChatGPT** | Connector (Developer mode) or Custom GPT: [guide](integrations/chatgpt.md) |
| **Claude.ai / Desktop** | Settings → Connectors → Add custom connector → `https://tips33.vercel.app/mcp` |
| **Claude Code** | `claude mcp add --transport http tips33 https://tips33.vercel.app/mcp` |
| **Gemini CLI** | `gemini extensions install https://github.com/inf-opc/tips33-skills` |
| **OpenAI Codex CLI** | `codex mcp add tips33 --url https://tips33.vercel.app/mcp` |
| **Cursor** | [One-click install](cursor://anysphere.cursor-deeplink/mcp/install?name=tips33&config=eyJ1cmwiOiJodHRwczovL3RpcHMzMy52ZXJjZWwuYXBwL21jcCJ9) |
| **VS Code (Copilot)** | `code --add-mcp '{"name":"tips33","type":"http","url":"https://tips33.vercel.app/mcp"}'` |
| **Mistral Le Chat** | Connectors → Add connector → Custom MCP → `https://tips33.vercel.app/mcp` |
| **Windsurf, Cline, Zed, Goose, LM Studio** | Add an HTTP MCP server: `https://tips33.vercel.app/mcp` |
| **OpenAI / Anthropic APIs** | [code samples](integrations/apis.md) |
| **Any agent or script** | `curl "https://tips33.vercel.app/api/recommend?q=trail+running+shoes&country=US&deals=1"` |

Claude Code plugin (MCP + skill in one step):

```
/plugin marketplace add inf-opc/tips33-skills
/plugin install tips33@tips33
```

Coding agents (Codex, Cursor, Copilot, Jules) read [`AGENTS.md`](AGENTS.md). Agent Skills runtimes load [`skills/find-deals`](skills/find-deals).

---

