# Changelog

## 1.1.0

- 7 skills in `skills/`: `linkedin-prospect-list`, `linkedin-hiring-signal-leads`, `linkedin-candidate-shortlist`, `linkedin-prospect-search`, `linkedin-account-brief`, `linkedin-engagement-leads` and `linkedin-inbox-followup`. They are byte copies of the skills in github.com/linkmcp-io/linkmcp.
- The skills only read, except three: they send a LinkedIn message or invitation only after the user approves its exact text, one at a time.

## 1.0.2

- README: 27 tools only read (8 tools write).

## 1.0.1

- Server URL with the listing tag `?ref=cursor-marketplace`.
- Tool count 35 in the README.

## 1.0.0

- First release: the `linkmcp` MCP server, a URL-only connector to the hosted LinkMCP server at `https://app.linkmcp.io/api/mcp` (Streamable HTTP).
- `"placement": "server"`, so Grok Bot (desktop and mobile) connects through the hosted MCP path.
- Sign-in: OAuth 2.1 with PKCE and Dynamic Client Registration. The server accepts every Cursor redirect URI (`cursor://anysphere.cursor-mcp/oauth/callback`, `https://www.cursor.com/agents/mcp/oauth/callback`, `http://localhost:8787/callback`).
- Logo: the LinkMCP mark on its light plate, 192 x 192 PNG.
