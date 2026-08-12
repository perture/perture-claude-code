# Perture for Claude Code

This is the Perture thin-client package for Claude Code.

The standalone adapter calls the versioned Perture Integration Gateway and is
bound to the `claude-code` platform. The remote MCP server remains a
compatibility path for clients that have not adopted the gateway. Brand rules,
memory, validation, permissions, and entitlements remain server-side on
`https://app.perture.co`.

## Contents

- Claude Code manifest in `.claude-plugin/plugin.json`.
- Compatibility remote MCP config in `.mcp.json`.
- Standalone gateway adapter in `scripts/perture-integration.mjs`.
- Minimal operating guidance in `skills/perture/SKILL.md`.
- Public Perture icon and logo assets.

The package contains no API keys, bearer tokens, customer data, proprietary
prompts, scoring rules, or local authorization logic.

## Authentication

Set the token only in the local environment:

```bash
PERTURE_ACCESS_TOKEN=pto_...
```

The token must be issued for the Claude Code gateway client and
`/api/integrations/v1` audience. A token issued only for `/mcp` is rejected
by the gateway.

The gateway URL is a release target and does not prove that the matching app
release has already been deployed.
