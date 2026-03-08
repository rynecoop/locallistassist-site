# Deploying locallistassist.app

Recommended platform: Cloudflare Pages with Cloudflare DNS.

## Why this setup

- simple static deployment
- automatic HTTPS
- easy custom domain support
- easy security headers and redirects
- strong DNS and edge controls

## Repo structure

This directory is ready to deploy as a static site:

- `index.html`
- `privacy/index.html`
- `products/android/index.html`
- `products/home-assistant/index.html`
- `404.html`
- `_headers`
- `_redirects`
- `CNAME`

## Recommended repository setup

Do not deploy this out of the parent `.codex` repository.

Create a dedicated GitHub repository for this site, for example:

- `locallistassist-site`

Then copy the contents of this folder into that repository root.

## Cloudflare Pages setup

1. Push this site to its own GitHub repository.
2. In Cloudflare, create a new Pages project.
3. Connect the GitHub repository.
4. Framework preset: `None`
5. Build command: leave empty
6. Build output directory: `/`
7. Deploy

## Custom domain

After the first deploy:

1. Add `locallistassist.app` as a custom domain in Cloudflare Pages.
2. Add `www.locallistassist.app` if you want it redirected.
3. Keep the `_redirects` file so `www` redirects to the apex domain.

## Security checklist

1. Turn on HTTPS only.
2. Enable DNSSEC in Cloudflare DNS.
3. Keep the `_headers` file in place.
4. Do not add third-party JavaScript unless there is a clear need.
5. Keep support email links as `mailto:` unless a secure form is actually needed.

## Public URLs to verify after deploy

- `https://locallistassist.app/`
- `https://locallistassist.app/privacy/`
- `https://locallistassist.app/products/android/`
- `https://locallistassist.app/products/home-assistant/`
- `https://locallistassist.app/robots.txt`
- `https://locallistassist.app/sitemap.xml`

