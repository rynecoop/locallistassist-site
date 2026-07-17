# Working in this repo

This is the **marketing site** for Local List Assist, served at
https://locallistassist.app and deployed via **Cloudflare Pages** (a push to
`main` publishes; PRs get a branch preview URL from the Cloudflare bot).

It documents **two apps**, and each maps to specific pages here:

- **Home Assistant integration** (`rynecoop/ha-grocery-learning`)
  → `/products/home-assistant/index.html` + the Home Assistant card on `/index.html`
- **Android app** (`rynecoop/local-list-assist-android`)
  → `/products/android/index.html` + the Android card on `/index.html`

## Keep pages in sync with the apps (standing rule)

When either app changes a **user-facing feature**, the matching page(s) above
should be updated to match — ideally in the same unit of work as the app change.
Keep copy honest about what actually works: on Android, **saved meals and the
meal planner are local-only** (they do not sync across devices) — don't imply
they sync.

## Conventions

- Static HTML/CSS; shared styles in `assets/site.css`. Reuse existing classes
  (`grid-3`, `section-card`, `feature-list`, `policy-card`, `pill`, etc.).
- Keep the page responsive and free of horizontal overflow; verify a render
  before shipping.
