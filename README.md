# Study Spaces — public site

Legal documents and account help for the Study Spaces Android app, served at
`[PLACEHOLDER — domain]` via GitHub Pages.

**This repository is public.** Only publishable text belongs here. Internal material — the
placeholder register, the compliance reasoning, security and paywall audits, architecture notes —
stays in the private app repository.

## Why a separate repo

Enabling Pages on the app repository's `docs/` folder would publish its security audit and Firestore
rule reasoning. Free-tier Pages also requires a public repo. The boundary is the point.

## The URLs are load-bearing

The app builds its Legal links from `legal_base_url` plus fixed paths in `strings.xml`:

| Path | Page |
|---|---|
| `/privacy` | `docs/privacy.md` |
| `/terms` | `docs/terms.md` |
| `/refunds` | `docs/refunds.md` |

`/delete-account` and `/support` are reached from the web and from Play Console, not from the app.

Do not rename these files. MkDocs' `use_directory_urls` publishes `/privacy/`; the app requests
`/privacy` and Pages redirects. Once a URL is in the Play listing, changing it means re-submitting.

## Local preview

```bash
pip install -r requirements.txt
mkdocs serve
```

## Deploying

Push to `main`. `.github/workflows/deploy.yml` builds with `--strict` and publishes to Pages.
Repository **Settings → Pages → Source** must be set to **GitHub Actions**.

## Status

Every document is a **draft** carrying `[PLACEHOLDER — …]` values and is not lawyer-reviewed. The
sequence for making them publishable is in the app repository at `docs/legal/site-plan.md`, and every
placeholder resolves from `docs/legal/PLACEHOLDERS.md` there. Neither of those files belongs in this
repository.
