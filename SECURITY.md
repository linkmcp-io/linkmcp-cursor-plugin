# Security policy

Report a security problem in the LinkMCP service, the MCP endpoint or this plugin to **info@linkmcp.io** with "Security" in the subject. Include the steps to reproduce. Do not open a public issue for it.

We confirm each report and keep you informed until the problem is fixed.

This plugin holds configuration and documentation only. It contains no code and no credentials. It points Cursor and Grok Bot at `https://app.linkmcp.io/api/mcp`. The MCP server signs in each user with OAuth 2.1 (PKCE, Dynamic Client Registration). Access tokens expire after one hour. Refresh tokens rotate on every use.

Security overview of the service: [app.linkmcp.io/security](https://app.linkmcp.io/security)
