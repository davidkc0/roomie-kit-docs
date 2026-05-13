# Hosted Apps

Roomie Kit Hosted creates a live Roomie Kit app on a Roomie-managed subdomain:

```txt
https://your-app.roomiekit.io
```

Hosted is the lowest-friction path when you want Roomie to run the production app infrastructure for you.

## Create An App

From the account dashboard:

1. Choose **Web app** for the fastest launch path.
2. Enter the app name.
3. Leave optional modules off unless you already know you need them.
4. Select **Create Hosted App**.

The dashboard reserves the subdomain, queues provisioning, and shows progress as the worker creates the Supabase project, deploys Edge Functions, deploys Vercel, attaches the subdomain, and runs health checks.

## Statuses

- `queued`: your app is waiting for the Hosted worker.
- `provisioning`: Supabase, auth, functions, and app config are being prepared.
- `deploying`: Vercel is building and attaching the hosted subdomain.
- `healthy`: the hosted URL is live and passing checks.
- `failed`: Roomie support needs to retry after the reported issue is fixed.

The dashboard refreshes automatically while setup is active.

## Retry A Failed Setup

If setup fails, the app card shows the last worker error and recent activity. Use **Retry setup** after the issue has been fixed. The app keeps the same subdomain and queues a fresh provisioning job.

## Starting Over

During beta, each account gets one active Hosted app slot. If you created the wrong app or want to start over, use **Request removal** on the app card. This removes the app from your dashboard and frees the slot.

Provider cleanup, when needed, is handled by Roomie support.

## Mobile Apps

Start with **Web app** unless you specifically need iOS or Android first. Mobile Hosted adds an assisted checklist for app store accounts, RevenueCat, push notifications, bundle IDs, and native review.
