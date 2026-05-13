# Codex Plugin

Use the Roomie Kit Codex plugin to set up, customize, and diagnose Roomie Kit apps from inside Codex.

The plugin uses the same Roomie Kit Cloud login as the CLI. Installing the plugin is public, but managed tools require an active Roomie Kit Cloud account.

## Requirements

- Node.js 20 or newer
- Codex with plugin support
- An active Roomie Kit Cloud account

## Install

Add the Roomie Kit marketplace:

```bash
codex plugin marketplace add davidkc0/roomie-kit-plugins
```

Then open the Codex Plugins UI and enable **Roomie Kit**.

## Sign In

Run browser login once per machine:

```bash
npx roomie-kit-host login
```

You can also ask Codex:

```text
Use Roomie Kit to start login.
```

Login opens a Roomie Kit activation page and stores auth locally in `.roomie-host/auth.local.json`.

## What You Can Ask Codex

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

If Codex cannot find the plugin, update the marketplace:

```bash
codex plugin marketplace upgrade roomie-kit
```

If managed tools fail, run:

```bash
npx roomie-kit-host whoami
```

If login has expired, run `npx roomie-kit-host login` again.

## Security

Customer Supabase, Vercel, Agora, and asset secrets stay local. They are not sent to Roomie Kit Cloud.
