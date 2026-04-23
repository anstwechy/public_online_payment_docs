# public_online_payment_docs

Merchant-facing documentation for the **Masarat MITF WooCommerce** payment plugin: install, configure, operate, sandbox testing, and go-live.

- **Company:** [Masarat — مسارات](https://masarat.ly/)  
- **Canonical Git repo:** [https://github.com/anstwechy/public_online_payment_docs](https://github.com/anstwechy/public_online_payment_docs)  
- **Plugin source:** [anstwechy/mitf-online-payment](https://github.com/anstwechy/mitf-online-payment)  

The repository is **public** for reading; **write** access on GitHub is limited to maintainers.

## Local preview

```bash
pip install -r requirements.txt
mkdocs serve
```

Open `http://127.0.0.1:8000`.

## GitLab Pages

This repo includes **`.gitlab-ci.yml`**. After you push to GitLab:

1. Wait for the **pages** job on the default branch.  
2. Open **Deploy → Pages** for the **Pages URL**.  
3. Optionally set **`site_url`** in `mkdocs.yml` to that URL so canonical links and search behave correctly.

## Mirror with GitHub

You can keep **GitHub** as a public mirror (edit links, issues, PRs) and use **GitLab** only for **CI/Pages**, or vice versa — just keep `repo_url` / remotes aligned with where you want “Edit this page” to point.

## License

Documentation © Masarat unless otherwise stated. Refer to repository license if one is added for contributions.
