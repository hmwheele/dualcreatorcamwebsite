# Dual Creator Cam — Marketing Site

Three-page marketing site styled from the Figma design (red hero, cream features, black close + footer). Pure HTML + CSS, mobile-friendly, no build step, no dependencies.

## Structure

```
site/
├── index.html              # Home (red hero + features + closer)
├── privacy/index.html      # Privacy Policy
├── support/index.html      # Support
├── assets/
│   ├── logo.jpg            # Brand mark (copied from project's appicon.jpg)
│   └── style.css           # Shared stylesheet
├── CNAME.example           # Rename to "CNAME" if using a custom domain
└── README.md
```

## URLs (after deployment)

| Purpose | URL |
|---|---|
| Marketing URL (App Store Connect) | `https://YOUR-DOMAIN/` |
| Privacy Policy URL (App Store Connect) | `https://YOUR-DOMAIN/privacy/` |
| Support URL (App Store Connect) | `https://YOUR-DOMAIN/support/` |

These are clean dedicated pages — App Review prefers these over anchor URLs.

## Deploy to GitHub Pages (fastest free option)

1. Create a new public GitHub repository (e.g. `dualcreatorcam-site`).
2. Push the contents of this `site/` folder to the repo root.
3. In the repo: **Settings → Pages → Source → Deploy from a branch → main / (root)**.
4. Wait ~1 minute. Your site will be live at `https://YOUR-USERNAME.github.io/dualcreatorcam-site/`.
5. Optional: connect a custom domain (e.g. `dualcreatorcam.com`) via **Settings → Pages → Custom domain**.

## Deploy to a custom domain

If you own `dualcreatorcam.com`:

1. In your DNS provider, add four `A` records pointing to GitHub's Pages IPs:
   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`
2. Add a `CNAME` record for `www` → `YOUR-USERNAME.github.io`.
3. Rename `CNAME.example` to `CNAME` (no extension) and put your domain on the only line:
   ```
   dualcreatorcam.com
   ```
4. Wait for DNS to propagate (5–30 min).
5. In GitHub Settings → Pages, enforce HTTPS once the cert provisions.

## Customize before launch

Search the project for these placeholders and replace:

- `idYOUR_APP_ID` in the App Store badge link → your actual App Store ID after the app is approved (you can leave a placeholder for launch and edit later).
- `hello@dualcreatorcam.com` → your real support email if different.
- `2026 Harrison Wheeler` in the footer if you want a different copyright line.

## Mobile

The site is responsive at three breakpoints:

- Default — desktop / tablet (1280px max width).
- `≤ 720px` — single-column features, condensed hero, vertical footer.
- `≤ 380px` — full-width CTA buttons, tighter padding.

Test by resizing the browser or using DevTools device emulation. The site has been built specifically for iOS Safari (the most likely traffic source from the App Store page).

## What App Review will check

App Review will hit your Privacy Policy URL and Support URL and confirm they load. Make sure:

- The pages actually resolve (no 404, no auth wall).
- The pages are publicly accessible (not gated behind a login).
- The privacy and support content is present and readable.

That's it.
