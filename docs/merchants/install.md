# Install the plugin

## Requirements

- **WordPress** 6.0 or newer  
- **PHP** 7.4 or newer  
- **WooCommerce** 8.0 or newer (tested up to 9.x)

## Get the plugin ZIP

### Option A — ZIP from Masarat or your bank

If you received **`online-payment-plugin-….zip`** from **Masarat** or your **bank onboarding** team, use that file and skip the build step.

### Option B — Build from the public plugin repository

From a checkout of the plugin repository [**anstwechy/mitf-online-payment**](https://github.com/anstwechy/mitf-online-payment), run from the **repository root**:

=== "Windows (PowerShell)"

    ```powershell
    pwsh -File scripts/build-plugin-zip.ps1
    ```

=== "macOS / Linux"

    If your checkout includes an equivalent shell script, run it from the repo root; otherwise use the ZIP provided by Masarat.

This produces **`online-payment-plugin-<version>.zip`** with clean paths for Linux hosting.

## Install in WordPress

1. In **wp-admin** go to **Plugins → Add New → Upload Plugin**.  
2. Choose the ZIP file, click **Install Now**, then **Activate Plugin**.  
3. Confirm **WooCommerce** is installed and **active**.

## Right after activation

1. Open **[Configure checkout](configuration.md)** and fill in the payment service URL, shared secret, and **MITF** credentials from your bank.  
2. Confirm your checkout page uses **classic checkout** (not only the Cart & Checkout block). Details are in the configuration guide.

## Documentation updates

Merchant guides are maintained in [**public_online_payment_docs**](https://github.com/anstwechy/public_online_payment_docs) on GitHub and published via **GitLab Pages**.
