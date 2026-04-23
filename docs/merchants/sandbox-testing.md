# Test in sandbox

## What “sandbox” means here

**Sandbox testing** uses Masarat’s **hosted payment service** together with the **bank’s MITF sandbox** (UAT-style credentials and flows). It is **not** the optional HTTP mock in the public plugin repository, which exists only for developers running Docker locally.

When Masarat provisions your store, you typically receive:

- Sandbox **MITF merchant credentials** (provider ID, user ID, PIN)  
- A **sandbox payment service base URL** and **shared secret** for that environment  

Enter those values in **[Configure checkout](configuration.md)** on a **staging** WordPress site that still uses **HTTPS** end-to-end where the bank expects it.

## Practical checks

1. Complete a small test order with a **sandbox card identity ID** supplied by the bank.  
2. Confirm the order reaches **processing** or **completed** in WooCommerce after OTP, depending on your workflow.  
3. If completion fails, verify the payment service can reach your store’s REST callback (see [Go-live checklist](go-live-checklist.md) — especially store base URL and TLS).

## More help

- [FAQ](faq.md) — checkout block limitations and common configuration mistakes.  
- [Shopper checkout experience](checkout-experience.md) — end-to-end flow.
