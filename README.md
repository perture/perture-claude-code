# Perture Claude Code Plugin Marketplace

Private source marketplace for the Perture thin-client plugin.

This release candidate adds the explicit Perture Integration Gateway v1 adapter
and keeps the remote MCP configuration as a compatibility fallback. It contains
no Perture prompts, scoring logic, customer rules, credentials, or customer
project data. Authentication, permissions, entitlements, memory, and validation
remain server-side on `app.perture.co`.

The gateway URL in this branch is a release target. This branch does not prove
that the corresponding Perture app release has been deployed, and it should not
replace the current compatible `main` package until that release is verified.

## Structure

```text
.claude-plugin/marketplace.json
plugins/perture/
  .claude-plugin/plugin.json
  .mcp.json
  assets/
  scripts/
  skills/perture/SKILL.md
  README.md
```

## Local test

From the parent directory:

```bash
claude plugin validate ./perture-claude-code
claude plugin marketplace add ./perture-claude-code
```

Then inside Claude Code:

```text
/plugin install perture@perture
```

## Authentication

The compatibility MCP connection points to `https://app.perture.co/mcp`.
The gateway adapter points to
`https://app.perture.co/api/integrations/v1` and requires a token issued for
the Claude Code gateway client and audience. Keep the token only in the local
process environment:

```bash
PERTURE_ACCESS_TOKEN=pto_...
```

Do not put tokens, API keys, brand rules, prompts, or customer data in this
repository.
