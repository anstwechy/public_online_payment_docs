# Configure checkout

## Use classic checkout (required)

This gateway is built for **classic checkout** fields. The **Cart & Checkout block** is **not** compatible: MITF fields may not appear there.

Use the checkout **shortcode** on your checkout page, for example:

```text
[woocommerce_checkout]
```

If the page uses only the block editor checkout block, switch to the shortcode (or a theme flow that exposes classic payment fields) so shoppers can enter the **card identity ID** and complete payment.

## Gateway settings

In **wp-admin** go to **WooCommerce → Settings → Payments → MITF (Masarat)** (or use **Settings** on the plugin row under **Plugins**).

| Setting | What to enter |
|--------|----------------|
| **Enable** | Turn on when you are ready to accept traffic per your Masarat / bank agreement (sandbox or live). |
| **Title / Description** | Shown at checkout; use clear language for shoppers. |
| **MITF provider ID / user ID / PIN** | From your bank (`MITF_PROVIDER_ID`, `MITF_USER_ID`, `MITF_PIN`). The PIN field can be left **blank** on save to **keep** the previous PIN. |
| **Payment service base URL** | **HTTPS** base URL with **no path** — the URL your **WordPress server** uses to call `/api/initiate`. It must be reachable from your hosting (not only from the shopper’s browser). In production this is usually your public Masarat payment host. |
| **Shared secret** | Must match `INITIATE_SHARED_SECRET` on the payment service. Used for signed initiate and for the order-complete callback in the current plugin. |

!!! warning "Protect secrets"

    Never commit production credentials or shared secrets to version control, email them in plain text to untrusted parties, or paste them into public tickets.

## Related guides

- [Shopper checkout experience](checkout-experience.md)  
- [Test in sandbox](sandbox-testing.md)  
- [FAQ](faq.md)  
- [Go-live checklist](go-live-checklist.md)  
