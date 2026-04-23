# Contributing and repository access

**Canonical repository:** [github.com/anstwechy/public_online_payment_docs](https://github.com/anstwechy/public_online_payment_docs)

This project is **public** so merchants and partners can **read** the documentation. **Write access** is limited to maintainers.

## For maintainers (GitHub settings)

To keep the repo public but stop unvetted pushes:

1. **Visibility** — **Settings → General**: ensure **Visibility** is **Public** (anyone can read clone and browse).
2. **Collaborators** — **Settings → Collaborators and teams**: do **not** grant **Write** or **Admin** to people who should not change `main`. Only trusted accounts get **Write**.
3. **Branch protection** — **Settings → Branches** (or **Rules → Rulesets**): protect **`main`** with:
   - **Require a pull request before merging** (optional but recommended).
   - **Restrict who can push to matching branches** — limit to yourself / your org team (so random accounts cannot push even if mis-added).
   - **Do not allow bypass** for roles that should not ship directly (tune to your org policy).

Forks and pull requests from the public are normal on GitHub; merging remains under your control if you protect `main` and review PRs.

## Suggested changes from non-maintainers

Open a **GitHub Issue** describing the doc fix, or fork and open a **Pull Request** if you accept external contributions. Masarat may route editorial changes through an internal process.
