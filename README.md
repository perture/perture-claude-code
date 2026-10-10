# Perture for Claude Code

Official public marketplace for the Perture Design Agent package.

The package combines Perture's authenticated remote MCP server with a local
Build/Review/Fix and Pro Brand Editor skills, repository inspection, deterministic source checks and
rendered desktop/mobile validation. The current package requires Frontend Contract
protocol `1.3` and fails closed when an approved Interface System component is
missing, unavailable or bypassed by a hand-built control. Its `interface-evidence.v1`
protocol and signed `isv3` receipt bind source, component instances, rendered pixels,
route, commit and build. A changed source, artifact or build invalidates approval.

An owner with an active Pro plan can ask the plugin to add or edit Brand Page
colors, typography, logos, fonts, illustrations, spacing and rounding. These
changes require an active brand lock and explicit user request. Reconnect an
existing Perture account after updating so the consent screen can grant the
new write scopes; existing read-only tokens do not gain them automatically.

The package contains no credentials, customer data or private brand rules.
Repository source remains local; protected brand context and authorization
remain on Perture infrastructure.

## Install

Add the public marketplace:

```text
/plugin marketplace add perture/perture-claude-code
```

Then install Perture:

```text
/plugin install perture@perture
```

Complete the browser sign-in when Claude Code requests authorization. All
protected behavior remains on Perture infrastructure and is authorized on
every request.

For an existing installation, open `/plugin`, choose Installed, and update
Perture. Reload plugins or start a new session. Installation or opening a
tutorial does not by itself establish an authenticated account connection.
