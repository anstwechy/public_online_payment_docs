# Go-live checklist

Use this list before you accept **real customer** payments. It is written for **merchants** and store operators; your bank or Masarat may add items.

## Store & checkout

- [ ] **WooCommerce** and this **MITF** plugin are active on the **production** site.  
- [ ] Checkout uses **classic** fields — **`[woocommerce_checkout]`** or equivalent — not only the Cart & Checkout block.  
- [ ] **HTTPS** is enabled for the storefront where the bank expects it.

## Gateway settings

- [ ] **Enable** is on when you intend to accept payments.  
- [ ] **Payment service base URL** is the **production** base URL (no path), reachable **from your WordPress server** (firewall / DNS / TLS).  
- [ ] **Shared secret** matches the **production** payment service.  
- [ ] **MITF provider ID, user ID, PIN** are the **live** values from your bank.

## Callbacks and URLs

- [ ] The payment service can call your store’s completion endpoint (your Masarat or bank runbook usually validates `WOO_URL` / REST reachability).  
- [ ] You ran at least one **end-to-end test** in **sandbox** before switching to live credentials.

## Operations

- [ ] Staff know how to interpret **pending** vs **completed** orders — see [Day-to-day operations](daily-operations.md).  
- [ ] You have a support path with your **bank** or **Masarat** for production incidents.

!!! note "Deeper technical review"

    Architecture notes for engineering teams remain in the plugin repository documentation. This public site focuses on merchant-facing steps.
