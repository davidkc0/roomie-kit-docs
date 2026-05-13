# Account And Billing

Start from `https://roomiekit.io`.

Recommended customer flow:

1. Choose **Roomie Kit Cloud** or **Roomie Kit Hosted** from the plans section.
2. Complete Stripe Checkout.
3. Return to the Roomie Kit login page.
4. Log in with the same email used at Stripe Checkout.
5. Open the account dashboard.
6. Copy the browser login command:

```bash
npx roomie-kit-host login
```

7. Approve the activation code in the browser.
8. Manage billing from the dashboard when needed.

If checkout succeeds but the dashboard still shows Free, wait a moment and refresh. Stripe webhooks can take a short time to sync subscription state.

Manual license keys are available from the dashboard as an advanced fallback, but browser login is the recommended path.

Hosted accounts also include the **Hosted Apps** dashboard section. Choose **Web app** for the fastest hosted launch. Choose **Mobile app beta** only when you are ready to work through the native setup checklist for app stores, RevenueCat, and OneSignal.

If you are already on Roomie Kit Cloud and choose Hosted, the checkout upgrades your existing subscription instead of creating a second subscription.

For billing help, email `support@roomiekit.io`.
