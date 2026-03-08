# locallistassist.app

Static website for:

- the paid standalone Android app
- the free Home Assistant integration
- the public privacy policy

## Pages

- `/` landing page
- `/products/android/` Android product page
- `/products/home-assistant/` Home Assistant product page
- `/privacy/` privacy policy
- `/404.html` fallback page

## Support contact

- `support@locallistassist.app`

## Recommended hosting

Recommended: Cloudflare Pages with Cloudflare DNS.

Why:

- simplest static deployment flow
- automatic HTTPS on the custom domain
- easy redirects and headers support
- better DNS and edge security controls than GitHub Pages alone
- easy long-term maintenance for a small static marketing site

Other static hosts will work, but Cloudflare Pages is the best balance for this domain.

## Required public URLs

- `https://locallistassist.app/`
- `https://locallistassist.app/privacy/`
- `https://locallistassist.app/products/android/`
- `https://locallistassist.app/products/home-assistant/`

## Security notes

- `_headers` sets strict security headers for a static site
- `_redirects` handles only path redirects that Cloudflare accepts during static deploys
- `www` to apex redirect should be configured in Cloudflare domain settings
- the site uses no third-party JavaScript
- fonts are local/system fonts to avoid unnecessary external requests

## Suggested next step

Deploy this directory to Cloudflare Pages and point `locallistassist.app` at that project.
