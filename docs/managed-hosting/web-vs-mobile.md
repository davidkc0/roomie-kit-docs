# Web Vs Mobile Hosted Apps

Roomie Kit Hosted has two creation paths. Choose the simplest path that matches the first version you want to ship.

## Web App

Choose **Web app** when you want the fastest launch.

Web Hosted deploys:

- A Roomie Kit web app at `https://<app-slug>.roomiekit.io`.
- Supabase auth, database, migrations, and core Edge Functions.
- Agora room voice, video chat, and livestream token support.
- Managed starter assets.
- Post-deploy checks.

Payments and push are off by default. This keeps the first deployment focused on rooms, auth, and media. Web monetization can be added later.

## Mobile App Beta

Choose **Mobile app beta** when the first release needs iOS or Android.

Mobile Hosted creates the same web/backend foundation, then tracks a native setup checklist:

- Bundle ID and Android package name.
- Apple Developer account.
- Google Play account.
- App Store Connect IAP products.
- Google Play Billing products.
- RevenueCat project and app API keys.
- OneSignal app with APNs and FCM configured.

Native publishing is assisted during beta. Store accounts, certificates, app review, APNs, FCM, and billing products still require owner approval.

## Payments

Roomie Kit subscriptions are billed by Roomie through Stripe.

Your hosted app monetization is separate:

- Web apps can use Stripe Checkout or Billing when monetization is needed.
- Mobile apps should use RevenueCat for iOS and Android in-app purchases.
- Cross-platform entitlements can use RevenueCat later if the same customer account needs purchases across web and mobile.

Roomie does not act as merchant of record for your app users in v1.

## Push

Push is disabled by default.

For Mobile Hosted beta, OneSignal is the default push provider. Push is only enabled when the app requests it and the required OneSignal keys are configured.

## Recommended Path

Start with Web Hosted unless the first release must be in the App Store or Google Play. It proves the room, media, auth, and admin loop first. Move to Mobile Hosted once the product is stable and the native accounts are ready.
