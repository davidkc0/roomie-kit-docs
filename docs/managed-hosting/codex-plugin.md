# Codex Plugin

The Codex plugin connects Codex to Roomie Kit Cloud tools for setup, customization, diagnostics, and docs lookup.

## Install

Add the public Roomie Kit plugin marketplace:

```bash
codex plugin marketplace add davidkc0/roomie-kit-plugins
```

Then open the Codex Plugins UI and enable or install **Roomie Kit**.

## Login

Use browser login once per machine:

```bash
npx roomie-kit-host login
```

You can also ask Codex to start Roomie Kit login; the plugin calls `roomie_login_start` and opens the activation page.

## Available tools

- `roomie_login_start`
- `roomie_whoami`
- `roomie_bootstrap_project`
- `roomie_customize_app`
- `roomie_doctor`
- `roomie_health_check`
- `roomie_docs_lookup`

Deploy execution remains a CLI command for now:

```bash
npx roomie-kit-host deploy --execute --resume
```

Security note: installing the plugin is public. Managed tools require Roomie Kit Cloud login. Customer Supabase, Vercel, Agora, and asset secrets stay local and are not sent to Roomie Kit Cloud.
