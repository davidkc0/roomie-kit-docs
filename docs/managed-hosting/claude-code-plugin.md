# Claude Code Plugin

The Claude Code plugin connects Claude Code to Roomie Kit Cloud tools through the same MCP server used by the CLI and Codex plugin.

## Install

```txt
/plugin marketplace add davidkc0/roomie-kit-plugins
/plugin install roomie-kit@roomie-kit
/reload-plugins
```

## Login

Use browser login once per machine:

```bash
npx roomie-kit-host login
```

Claude can also start login through the `roomie_login_start` MCP tool.

## Available tools

- Account check
- Project bootstrap
- App customization
- Doctor checks
- Health checks
- Docs lookup

Deploy execution remains a CLI command for now:

```bash
npx roomie-kit-host deploy --execute --resume
```

Security note: installing the plugin is public. Managed tools require Roomie Kit Cloud login. Customer Supabase, Vercel, Agora, and asset secrets stay local and are not sent to Roomie Kit Cloud.
