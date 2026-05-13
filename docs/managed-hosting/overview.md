# Roomie Kit Cloud And Hosted Overview

Roomie Kit has two paid paths. See the [plans section](https://roomiekit.io/#pricing) for current pricing.

## Roomie Kit Cloud

Roomie Kit Cloud is for teams that want help deploying the open-source starter while keeping their own Vercel, Supabase, and Agora accounts.

Cloud provides:

- `roomie-kit-host` CLI access.
- Codex and Claude Code plugins.
- Guided setup and deployment.
- Starter asset defaults.
- Deployment health checks.
- Update tooling.
- Support.
- Account and billing tools.

With Cloud, customers own their infrastructure:

- Vercel hosts the web app.
- Supabase hosts auth, database, realtime, and Edge Functions.
- Agora powers media and livestreaming.

Roomie Kit Cloud does not store your provider secrets. Setup runs from your machine or agent environment.

## Roomie Kit Hosted

Roomie Kit Hosted is for teams that want Roomie to run the app infrastructure.

Hosted provides:

- A Roomie-owned subdomain such as `https://your-app.roomiekit.io`.
- Supabase project provisioning and hosted auth configuration.
- Vercel deployment from the managed Roomie Kit app repo.
- Agora token setup for rooms, video chat, and livestreaming.
- Post-deploy checks, updates, and support.

Web Hosted is the default launch path. Mobile Hosted is a separate assisted beta path because native billing, push notifications, bundle IDs, app stores, APNs, FCM, and store review require additional owner setup.
