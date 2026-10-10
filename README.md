# LinkMCP for Cursor

**Your own LinkedIn account, as tools for Cursor and Grok Bot.**

LinkMCP is a hosted MCP server for LinkedIn. You connect your LinkedIn account once in the LinkMCP web app. Then the agent can research people and companies, search LinkedIn (also Sales Navigator, with your own seat), read and answer your LinkedIn messages, post, comment and react (as yourself or as a company page that you administer), manage invitations, and find work emails and mobile numbers.

This plugin adds one remote MCP server to Cursor and Grok Bot:

```
https://app.linkmcp.io/api/mcp?ref=cursor-marketplace
```

Nothing runs on your computer. The plugin contains no code. It contains only configuration (the plugin manifest and the MCP server address), documentation and a logo.

LinkMCP is not affiliated with, endorsed by or sponsored by LinkedIn Corporation. LinkedIn is a trademark of LinkedIn Corporation.

## Install in Cursor

1. Open **Cursor Settings > Plugins**, search for **LinkMCP** and click **Install**. Or run `/add-plugin linkmcp` in chat.
2. When Cursor asks you to sign in, a browser window opens. Sign in to LinkMCP with an email code or with Google. If you are already signed in, click **Authorize**. You do not need an API key or a client ID.
3. Ask the agent, for example: "Look up the company linkedin.com/company/stripe on LinkedIn and give me a short brief."

## Install in Grok Bot

1. Open **Marketplace** in the sidebar. In the mobile app, tap your avatar, then **Plugins**.
2. Find **LinkMCP** and choose **Add**.
3. When Grok Bot asks you to **Authorize**, sign in to LinkMCP in your browser.
4. In chat, type `@` and pick LinkMCP.

No LinkMCP account yet? The sign-in window creates one. The free trial runs 7 days and needs no card.

### Without the Marketplace

Add this to `~/.cursor/mcp.json` (all projects) or `.cursor/mcp.json` (one project). Then restart Cursor and approve the sign-in window:

```json
{
  "mcpServers": {
    "linkmcp": { "url": "https://app.linkmcp.io/api/mcp?ref=cursor-marketplace" }
  }
}
```

## What works in the free trial

Profile and company lookups, the posts and comments of people and companies, and email and phone finding work at once. To act as yourself on LinkedIn (people search, inbox, invitations, posting, company pages), subscribe and connect your LinkedIn account once in the web app at [app.linkmcp.io](https://app.linkmcp.io).

## Example prompts

These work in the free trial:

```
Look up the LinkedIn profile <profile URL> and give me a short brief: role, company,
time in the role, and what they posted in the last month.
```

```
Find the work email of <full name> at <company domain> and validate it.
```

These need a paid plan, with your LinkedIn account connected:

```
List my LinkedIn conversations with no reply in 7 days. Check what each person
posted recently and draft a reply for each. Show me the drafts before you send
anything.
```

```
Find heads of RevOps at Series B SaaS companies in the Netherlands. Summarise what
each one posted in the last month.
```

## Tools

35 tools. 27 tools only read. 8 tools write: send a message, send a connection request, manage a connection request, create a post, comment, react, mark a conversation as read, and send feedback. Each tool is marked as read-only or as a write, so your client can ask for your approval before each write. Full list: [Tool reference](https://app.linkmcp.io/docs/tool-reference).

## How sign-in and data work

- Sign-in is OAuth 2.1 with PKCE. Cursor registers itself with LinkMCP (Dynamic Client Registration) and opens the LinkMCP sign-in page. LinkMCP never sees your Cursor or Grok Bot credentials.
- You connect your LinkedIn account in the LinkMCP web app, not in Cursor.
- Each tool call goes from Cursor to `https://app.linkmcp.io/api/mcp` over HTTPS. LinkMCP runs the action on your connected LinkedIn account and returns the result.
- To stop access, remove the plugin in Cursor or Grok Bot. To stop all LinkedIn actions from every client, disconnect your LinkedIn account in the LinkMCP web app.

## Safety

LinkMCP applies daily limits and spacing to every action that reaches LinkedIn, to protect your LinkedIn account. Read more: [Will my LinkedIn get banned?](https://app.linkmcp.io/guides/will-my-linkedin-get-banned) and [Security](https://app.linkmcp.io/security).

## Pricing

Free trial: 7 days, no card. Starter $19 per month, Pro $49 per month, Max $199 per month. Every paid plan includes every tool. Higher plans include more monthly usage. Current prices: [app.linkmcp.io/#pricing](https://app.linkmcp.io/#pricing)

## Support, privacy and terms

- Support: [info@linkmcp.io](mailto:info@linkmcp.io) or [GitHub issues](https://github.com/linkmcp-io/linkmcp-cursor-plugin/issues)
- Privacy Policy: [app.linkmcp.io/legal/PP-STD.pdf](https://app.linkmcp.io/legal/PP-STD.pdf)
- Terms of Service: [app.linkmcp.io/legal/TOS-STD.pdf](https://app.linkmcp.io/legal/TOS-STD.pdf)
- All legal documents: [app.linkmcp.io/legal](https://app.linkmcp.io/legal)

LinkMCP is a service of Third Person Systems LLC. Setup guides for other AI clients: [github.com/linkmcp-io/linkmcp](https://github.com/linkmcp-io/linkmcp).

## License

The files in this plugin are MIT licensed. The LinkMCP service itself is a hosted, closed-source service.
