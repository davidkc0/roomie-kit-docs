# Claude Code Plugin

Use the Roomie Kit Claude Code plugin to set up, customize, and diagnose Roomie Kit apps from inside Claude Code.

The plugin uses the same Roomie Kit Cloud login as the CLI. Installing the plugin is public, but managed tools require an active Roomie Kit Cloud account.

## Requirements

- Node.js 20 or newer
- Claude Code
- An active Roomie Kit Cloud account

## Install

Add the Roomie Kit marketplace and install the plugin:

```txt
/plugin marketplace add davidkc0/roomie-kit-plugins
/plugin install roomie-kit@roomie-kit
/reload-plugins
```

## Sign In

Run browser login once per machine:

```bash
npx roomie-kit-host login
```

You can also ask Claude Code:

```text
Use Roomie Kit to start login.
```

Login opens a Roomie Kit activation page and stores auth locally in `.roomie-host/auth.local.json`.

## What You Can Ask Claude Code

- `Use Roomie Kit to check who I am.`
- `Use Roomie Kit to bootstrap this project. Use app name Acme Live.`
- `Use Roomie Kit to customize this app with the stream-dark theme.`
- `Use Roomie Kit to run doctor on this project.`
- `Use Roomie Kit to look up the livestreaming docs.`

Production deploy execution is currently handled by the CLI:

```bash
npx roomie-kit-host deploy --execute --resume
```

## Troubleshooting

If Claude Code still shows an old plugin version, update the marketplace and plugin:

```bash
claude plugin marketplace update roomie-kit
claude plugin update roomie-kit@roomie-kit
```

Restart Claude Code after updating.

If managed tools fail, run:

```bash
npx roomie-kit-host whoami
```

If login has expired, run `npx roomie-kit-host login` again.

## Security

Customer Supabase, Vercel, Agora, and asset secrets stay local. They are not sent to Roomie Kit Cloud.
