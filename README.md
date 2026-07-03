# Perture Claude Code Plugin Marketplace

Private Claude Code marketplace for the Perture thin-client plugin.

This package is intentionally small. It does not contain Perture prompts, scoring,
brand-rule logic, validation logic, or local generation code. The plugin only
registers a remote Perture MCP server and short usage guidance. All privileged
work runs on `https://app.perture.co`.

## Structure

```text
.claude-plugin/marketplace.json
plugins/perture/
  .claude-plugin/plugin.json
  .mcp.json
  assets/
  skills/
  README.md
```

## Local Test

From the parent directory:

```bash
claude plugin validate ./perture-claude-plugin
claude plugin marketplace add ./perture-claude-plugin
```

Then inside Claude Code:

```text
/plugin install perture@perture
```

## GitHub Publishing

Push this folder as its own repository. Users can add it as a marketplace:

```bash
claude plugin marketplace add <owner>/<repo>
```

Then install:

```text
/plugin install perture@perture
```

## Authentication

The plugin points Claude Code at `https://app.perture.co/mcp`. If the MCP
connection handles OAuth, users should connect with their Perture account during
plugin setup. For local fallback testing only, set:

```bash
PERTURE_ACCESS_TOKEN=pto_...
```

Do not put tokens, API keys, brand rules, prompts, or customer data in this
repository.
