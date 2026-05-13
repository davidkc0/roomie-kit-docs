# Hosted Apps

Roomie Kit Hosted creates a live Roomie Kit app on a Roomie-managed subdomain.

```txt
https://your-app.roomiekit.io
```

Use Hosted when you want Roomie to run the app infrastructure instead of connecting your own Supabase, Vercel, and Agora accounts.

## Create An App

From the account dashboard:

1. Choose **Web app** for the fastest launch path.
2. Enter the app name.
3. Keep optional modules off unless you already need them.
4. Select **Create Hosted App**.

The dashboard reserves the subdomain and shows progress while Roomie provisions the app.

Roomie handles:

- Supabase project setup.
- Auth redirect settings.
- Core database migrations.
- Agora token function setup.
- Vercel deployment.
- Roomie Kit subdomain setup.
- Post-deploy health checks.

## Statuses

- `queued`: your app is waiting for the Hosted worker.
- `provisioning`: Supabase, auth, functions, and app config are being prepared.
- `deploying`: Vercel is building and attaching the hosted subdomain.
- `healthy`: the hosted URL is live and passing checks.
- `degraded`: the app deployed, but one check needs attention.
- `failed`: setup stopped before the app was ready.

The dashboard refreshes automatically while setup is active.

## Post-Deploy Checks

After Vercel deploys, Roomie checks:

- The hosted URL loads.
- Required starter assets are reachable.
- The Supabase API responds.
- The Agora token function allows browser calls from the hosted URL.
- Agora token secrets are configured.

If a check fails, the dashboard shows which item needs attention.

## Retry A Failed Setup

If setup fails, the app card shows the last error and recent activity. Use **Retry setup** after the issue is fixed. The app keeps the same subdomain and queues a fresh setup run.

## Starting Over

During beta, each account gets one active Hosted app slot. If you created the wrong app or want to start over, use **Request removal** on the app card.

This removes the app from your dashboard and frees the slot. Provider cleanup, when needed, is handled by Roomie support.

## Mobile Apps

Start with **Web app** unless you specifically need iOS or Android first. Mobile Hosted adds an assisted checklist for app store accounts, RevenueCat, push notifications, bundle IDs, and native review.
