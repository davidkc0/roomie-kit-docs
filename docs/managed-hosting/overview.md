# Roomie Kit Cloud And Hosted Overview

Roomie Kit has two paid paths. See the [plans section](https://roomiekit.io/#pricing) for current pricing.

## Roomie Kit Cloud

Roomie Kit Cloud is the assisted deployment layer for teams that want to keep Vercel, Supabase, and Agora in their own accounts.

Cloud provides:

- `roomie-kit-host` CLI access.
- Codex and Claude Code plugins.
- Guided onboarding and deployment.
- Starter asset defaults.
- Health checks.
- Update tooling.
- Support.
- Billing management through the Roomie Kit account portal.

With Cloud, customers own their infrastructure:

- Vercel hosts the web app.
- Supabase hosts auth, database, realtime, and Edge Functions.
- Agora powers media and livestreaming.

Roomie Kit Cloud only handles account state, licenses, entitlements, release metadata, and cloud CLI access.

## Roomie Kit Hosted

Roomie Kit Hosted is the managed beta path for teams that want Roomie to run the app infrastructure.

Hosted provides:

- A Roomie-owned subdomain such as `https://your-app.roomiekit.io`.
- Supabase project provisioning and hosted auth configuration.
- Vercel deployment from the managed Roomie Kit app repo.
- Agora token setup for rooms, video chat, and livestreaming.
- Health checks, updates, and support.

Web Hosted is the default launch path. Mobile Hosted is a separate assisted beta path because native billing, push notifications, bundle IDs, app stores, APNs, FCM, and store review require additional owner setup.
