# Perture for Claude Code

Official public marketplace for the Perture Design Agent package.

The package combines Perture's authenticated remote MCP server with a local
Build/Review/Fix skill, repository inspection, deterministic source checks and
rendered desktop/mobile validation. Version `0.8.5` requires Frontend Contract
protocol `1.3` and fails closed when an approved Interface System component is
missing, unavailable or bypassed by a hand-built control.

The package contains no credentials, customer data or private brand rules.
Repository source remains local; protected brand context and authorization
remain on Perture infrastructure.

## Install

Add the public marketplace:

```text
claude plugin marketplace add perture/perture-claude-code
```

Then install Perture:

```text
/plugin install perture@perture
```

Complete the browser sign-in when Claude Code requests authorization. All
protected behavior remains on Perture infrastructure and is authorized on
every request.
