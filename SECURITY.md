# Security Notes

This website is intentionally static.

That is the main security strategy:

- no backend runtime
- no database
- no login flow
- no client-side JavaScript
- no third-party tracking scripts

## Current protections

- strict security headers in `_headers`
- canonical redirect in `_redirects`
- no external font loading
- HTTPS expected at the hosting layer
- DNSSEC recommended at the DNS layer

## Operational guidance

1. Use Cloudflare Pages or another static host with automatic HTTPS.
2. Keep the domain on a provider that supports DNSSEC.
3. Avoid adding contact forms unless they are truly needed.
4. If a form is added later, treat it as a security-sensitive feature and review it separately.
5. Keep dependencies at zero unless there is a clear product reason to add them.

## Reporting

Security concerns can be reported to:

- `support@locallistassist.app`

