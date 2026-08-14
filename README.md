# Perture for Claude Code

Official public marketplace for the Perture thin connection package.

The package registers Perture's authenticated remote MCP server and a minimal
user-approved-work reminder. It contains no credentials, customer data,
business rules, scoring, prompts, validators, request clients, or proprietary
implementation logic.

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
