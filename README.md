# ldgrapp.com

The marketing site for Ldgr, a budgeting app for iPhone that you keep by hand. It's plain HTML and CSS with no build step, served from GitHub Pages at [ldgrapp.com](https://ldgrapp.com).

## Pages

| File | URL | Purpose |
|------|-----|---------|
| `index.html` | `/` | Landing page: the idea, how it works, and why I built it |
| `privacy.html` | `/privacy.html` | Privacy Policy (App Store required) |
| `terms.html` | `/terms.html` | Terms of Use |
| `support.html` | `/support.html` | Support and FAQ (App Store required) |
| `styles.css` | n/a | Shared design system (tokens, components) |

App Store listing: <https://apps.apple.com/app/id6476118269>. The Support URL in App Store Connect points to `https://ldgrapp.com/support.html` and the Privacy Policy URL to `https://ldgrapp.com/privacy.html`.

## Local preview

```sh
python3 -m http.server 8000
# open http://localhost:8000
```

Preview at the domain root (`/`), not a subpath. The pages use root-relative links.

## Design

The site borrows the app's look: fern green `#4F7942`, rounded type (`ui-rounded`, which is real SF Rounded on Apple devices), and a replica of the app's "left to spend" card in the hero. All the tokens are CSS custom properties at the top of `styles.css`, with light and dark modes both defined there.

## Deployment

Pushing to `main` deploys to GitHub Pages (branch deploy from the root, with `.nojekyll` so files are served as-is). The custom domain comes from the `CNAME` file. DNS is four `185.199.108–111.153` A records on the apex, plus a `www` CNAME to `tannermares.github.io`.

## Notes

- The legal pages are plain-language drafts. A lawyer hasn't reviewed them.
- `support@ldgrapp.com` and `privacy@ldgrapp.com` need mailboxes or forwarding set up on the domain.
- The App Store badge links to the live listing (`id6476118269`), and an `apple-itunes-app` meta tag shows the native smart banner in iOS Safari.

© 2026 Tanner Mares
