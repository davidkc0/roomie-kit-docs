# Web Vs Mobile Hosted Apps

Roomie Kit Hosted has two creation paths.

## Web App

Choose **Web app** when you want the fastest hosted launch path.

Web Hosted deploys:

- A Roomie Kit web app at `https://<app-slug>.roomiekit.io`.
- Supabase auth, database, migrations, and core Edge Functions.
- Agora room voice, video chat, and livestream token support.
- Managed starter assets and health checks.

Payments and push are off by default for Web Hosted. This keeps the first deployment focused on getting rooms and media live. Web monetization can be added later with Stripe Checkout or Billing.

## Mobile App Beta

Choose **Mobile app beta** when you need iOS or Android.

Mobile Hosted creates the same web/backend foundation, then tracks a native setup checklist:

- Bundle ID and Android package name.
- Apple Developer account.
- Google Play account.
- App Store Connect IAP products.
- Google Play Billing products.
- RevenueCat project and app API keys.
- OneSignal app with APNs and FCM configured.

Native publishing is assisted during beta. Store accounts, certificates, app review, APNs, FCM, and billing products still require owner approval and cannot be fully automated safely.

## Payments

Roomie Kit subscriptions are billed by Roomie through Stripe.

Your hosted app monetization is separate:

- Web apps should start with Stripe Checkout or Billing when monetization is needed.
- Mobile apps should use RevenueCat for iOS and Android in-app purchases.
- Cross-platform entitlements can use RevenueCat later if the same customer account needs purchases across web and mobile.

Roomie does not act as merchant of record for your app users in v1. Stripe Connect and creator payouts are deferred until a customer needs marketplace payouts.

## Push

Push is disabled by default.

For Mobile Hosted beta, OneSignal is the default push provider. The hosted worker only enables push when the app requests push and Roomie has the OneSignal app ID and REST key configured for that hosted app.

## Recommended Path

Start with Web Hosted unless the first release must be in the App Store or Google Play. It proves the room, media, auth, and admin loop first. Move to Mobile Hosted once the app experience is stable and the native account setup is ready.
