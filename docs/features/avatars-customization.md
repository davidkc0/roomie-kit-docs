# Avatars And Customization

Roomie Kit has a customization layer for changing the starter without rewriting app code.

Built in:

- `web/roomie.config.json` for app name, theme template, colors, and asset aliases.
- Local override folders under `web/public/roomie-local`.
- Avatar base model, texture, skin, outfit, hair, shoes, and thumbnail conventions.
- Branding overrides for logos, icons, lobby cards, and app imagery.
- Room, furniture, wall, floor, animation, emote, SFX, and general asset overrides.

Local files win when present. Missing files fall back to the configured starter asset base URL.

Related docs:

- [Customization](../customization.md)
- [Asset naming conventions](../reference/asset-naming.md)
- [Asset folders](../assets.md)
