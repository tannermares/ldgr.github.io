# ldgrapp.com

Marketing site for **Ldgr** — a private, manual budgeting app for iPhone. Static HTML/CSS, no build step, served from GitHub Pages at [ldgrapp.com](https://ldgrapp.com).

## Pages

| File | URL | Purpose |
|------|-----|---------|
| `index.html` | `/` | Landing page — philosophy, how it works, founder note |
| `privacy.html` | `/privacy.html` | Privacy Policy (App Store required) |
| `terms.html` | `/terms.html` | Terms of Use |
| `support.html` | `/support.html` | Support + FAQ (App Store required) |
| `styles.css` | — | Shared design system (tokens, components) |

App Store URLs: **Support** → `https://ldgrapp.com/support.html`, **Privacy Policy** → `https://ldgrapp.com/privacy.html`.

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

Preview at the domain root (`/`), not a subpath — the pages use root-relative links.

## Design

Mirrors the iOS app's visual language: fern green `#4F7942`, rounded type (`ui-rounded` → real SF Rounded on Apple devices), and a live replica of the app's "left to spend" budget card as the hero. All tokens live as CSS custom properties at the top of `styles.css`; light and dark modes both defined there.

## Deployment

Pushing to `main` triggers GitHub Pages (branch deploy, root, `.nojekyll` to serve files as-is). Custom domain is set via the `CNAME` file. DNS: four `185.199.108–111.153` A records on the apex, plus a `www` CNAME to `tannermares.github.io`.

## Notes

- The legal pages are plain-language drafts, not attorney-reviewed.
- `support@ldgrapp.com` / `privacy@ldgrapp.com` need mailbox/forwarding set up on the domain.
- The App Store badge is "coming soon" — swap in the real store link once the app is live.

© 2026 Tanner Mares
