# FAQ

## Why don’t I see MITF fields at checkout?

The gateway targets **classic checkout**. If your checkout page uses only the **Cart & Checkout block**, the MITF fields may not appear. Use the **`[woocommerce_checkout]`** shortcode (or another layout that renders classic gateway fields). See **[Configure checkout](configuration.md)**.

## What base URL should I use for the payment service?

Use the **HTTPS base URL with no path** that your **web server** can reach when calling `/api/initiate`. That is often your public Masarat payment hostname. Do **not** paste a URL that only works inside your own laptop browser (for example `http://localhost:3000`) unless WordPress actually runs there and the bank agrees. For Docker-style lab setups, use the **service hostname on the Docker network** (for example `http://payment:3000` in the plugin repository’s sample compose file).

## Does the order-complete callback use the same secret as initiate?

**Yes, in the current plugin:** completion HMAC uses the same **shared secret** as signed initiate. Keep payment service configuration aligned with what WordPress validates. Your bank or Masarat can confirm the exact deployment profile.

## Where do I get MITF credentials?

From **your bank** as part of the MITF merchant agreement. Masarat does not publish live or sandbox bank secrets in this documentation site.

## Can I use the GitHub mock for my store?

The repository mock is for **developers** validating the integration in Docker. Merchants should follow Masarat’s **sandbox / production** endpoints and secrets instead. See **[Test in sandbox](sandbox-testing.md)**.

## Card identity ID length errors

The field accepts **9** or **10** digits only (10 for Trade and Development Bank). Strip spaces and non-numeric characters; shoppers should enter digits only.
