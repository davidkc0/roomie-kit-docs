# Browser Login And Manual Keys

Roomie Kit Cloud uses browser login for the CLI and agent plugins.

```bash
npx roomie-kit-host login
```

The command opens `roomiekit.io/activate` with a short activation code. Log in with the email tied to your Roomie Kit Cloud subscription, approve the device, and return to the terminal.

After login, confirm the local account:

```bash
npx roomie-kit-host whoami
```

Browser login works for:

- Roomie Kit CLI
- Codex plugin
- Claude Code plugin

## Manual license key fallback

Manual keys are only needed for support, headless environments, or fallback login.

To get a manual key:

1. Open `https://roomiekit.io/login`.
2. Log in with the Stripe Checkout email.
3. Open the account dashboard.
4. Open **Need a manual license key?**
5. Generate or regenerate a manual key.
6. Copy the login command.

```bash
npx roomie-kit-host login --token <license-key>
```

The full manual license key is shown once when generated or regenerated. Roomie Kit stores only a hash and prefix after that.

If you lose the key, regenerate it from the account dashboard and run the login command again.

## Plugin install

Claude Code:

```txt
/plugin marketplace add davidkc0/roomie-kit-plugins
/plugin install roomie-kit@roomie-kit
/reload-plugins
```

Codex:

```bash
codex plugin marketplace add davidkc0/roomie-kit-plugins
```

Then enable or install **Roomie Kit** from the Codex Plugins UI.
