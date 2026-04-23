# Shopper checkout experience

This page describes what **customers** see when they pay with **MITF (Masarat)** on your store.

## At checkout

1. The shopper selects **MITF** (or the custom **title** you set in gateway settings).  
2. They see your **description** text (for example that they will confirm with a one-time password).  
3. They enter the **card identity ID** in the field labelled **Card identity ID**.  
   - **Digits only.**  
   - **9 digits** for most banks; **10 digits** for Trade and Development Bank.  
4. They place the order.

## Redirect and OTP

1. If the payment service accepts the request, the shopper is **redirected** to Masarat’s **hosted payment page** to complete **OTP** (or the bank’s equivalent step).  
2. In WooCommerce, the order is typically set to **pending** with a note that the customer was redirected and completion is awaited.

## After payment

1. When the bank flow completes successfully, the payment service notifies your store so the order can move to **processing** or **completed**, depending on your WooCommerce settings and workflows.  
2. The shopper should land on the normal **order received / thank you** page for your store.

## If something fails

- **Validation errors** (wrong length, non-numeric ID) appear as WooCommerce notices on checkout.  
- **Unreachable payment service** or **HTTP errors** show a message that the payment could not start; see [FAQ](faq.md) and confirm the **payment service base URL** and hosting connectivity.  
- If the shopper finishes OTP but the order **stays unpaid**, that usually points to **callback** or **URL** issues on the store or payment service — your bank or Masarat support can trace this with logs; the [Go-live checklist](go-live-checklist.md) lists common causes.
