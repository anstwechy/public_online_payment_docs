# Day-to-day operations

How to **run** the MITF gateway after it is installed and configured.

## Turn payments on or off

1. Go to **WooCommerce → Settings → Payments**.  
2. Use **MITF (Masarat)** — toggle **Enable** or use the **Manage** screen.  
3. Save changes.

Use this for maintenance windows, catalog freezes, or when your bank asks you to pause card acceptance temporarily.

## Update texts shoppers see

Under the same gateway settings, edit **Title** and **Description**. These appear at checkout; keep them short and in your customers’ language.

## Rotate MITF PIN or other bank credentials

When your bank issues a new **PIN** or merchant identifiers:

1. Open **WooCommerce → Settings → Payments → MITF (Masarat)**.  
2. Update **provider ID**, **user ID**, and/or **PIN** as instructed.  
3. For **PIN only**: if you leave the PIN field **blank** and save, the plugin **keeps** the previous PIN (useful when changing unrelated settings). To set a new PIN, enter the new value explicitly.

## Payment service URL and shared secret

Change these only when Masarat or your bank moves you to a new environment (for example sandbox → production) or rotates the **shared secret**.

- **Payment service base URL** must remain a **base URL with no path**, reachable **from your WordPress server**.  
- **Shared secret** must match the payment service configuration.

After changes, run a **small test order** in the appropriate environment before heavy traffic.

## Orders in WooCommerce

- **Pending** — common right after redirect to OTP, until completion is confirmed.  
- **Processing / completed** — success paths depend on your WooCommerce order settings and any automation you use.

If status seems wrong after OTP succeeds, see [FAQ](faq.md) and [Go-live checklist](go-live-checklist.md) (callback URL, HTTPS, firewall).

## What merchants should not do

- Do not share **MITF PIN**, **shared secret**, or **payment service** admin details in chat or social media.  
- Do not point the **payment service base URL** at a developer **mock** or **localhost** URL in production.  
- Do not rely on the **Cart & Checkout block** without classic fields — see [Configure checkout](configuration.md).

## Support

For **bank credentials**, **sandbox**, and **production** endpoints, contact your **bank** or **Masarat** onboarding channel. For **WordPress / WooCommerce** behavior (themes, other plugins), your web agency or host may need to help alongside this guide.
