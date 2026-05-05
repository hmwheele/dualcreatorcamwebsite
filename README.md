# Dual Creator Cam — Marketing Site

Single-page landing site with embedded privacy policy and support sections. Pure HTML + CSS, no build step, no dependencies.

## Files

- `index.html` — the entire site in one file.

## URLs (after deployment)

| Purpose | URL |
|---|---|
| Marketing URL (App Store Connect) | `https://YOUR-DOMAIN/` |
| Privacy Policy URL (App Store Connect) | `https://YOUR-DOMAIN/#privacy` |
| Support URL (App Store Connect) | `https://YOUR-DOMAIN/#support` |

App Store Connect accepts anchor URLs like `/#privacy` for the Privacy Policy and Support fields. If App Review rejects the anchor (rare), copy `index.html` into a `/privacy/` and `/support/` folder and use those paths instead.

## Deploy to GitHub Pages (fastest free option)

1. Create a new public GitHub repository (e.g. `dualcreatorcam-site`).
2. Copy `index.html` to the root of that repo and push.
3. In the repo: **Settings → Pages → Source → Deploy from a branch → main / (root)**.
4. Wait ~1 minute. Your site will be live at `https://YOUR-USERNAME.github.io/dualcreatorcam-site/`.
5. Optional: connect a custom domain (e.g. `dualcreatorcam.app`) via **Settings → Pages → Custom domain**.

## Deploy to a custom domain

If you own `dualcreatorcam.app`:

1. In your DNS provider, add four `A` records pointing to GitHub's Pages IPs:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
2. Add a `CNAME` record for `www` → `YOUR-USERNAME.github.io`.
3. In the repo, create a `CNAME` file at the root containing just: `dualcreatorcam.app`
4. Wait for DNS to propagate (5–30 min).
5. In GitHub Settings → Pages, enforce HTTPS once the cert provisions.

## Customize before launch

Search the file for these placeholders and replace:

- `idYOUR_APP_ID` in the App Store badge link → your actual App Store ID after the app is approved (you can leave a placeholder for launch and edit later).
- `hello@dualcreatorcam.app` → your real support email if different.
- `2026 Harrison Wheeler` in the footer.
- The `<meta name="description">` and Open Graph tags if you want different copy in search/social previews.

## What App Review will check

App Review will hit your Privacy Policy URL and confirm it loads. Make sure:

- The page actually resolves (no 404, no auth wall).
- The page is publicly accessible (not gated behind a login).
- The privacy content is present and readable on the page that loads.

That's it.
