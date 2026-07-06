# Directorium — Website & Admin

> The flagship website and admin for the Directorium platform — *Introíbo ad altáre Dei.*

**Site** is directorium.app: the public reader (calendar + day pages, Sources & licenses, SEO,
cookieless analytics) and the authenticated **admin SPA** for the platform — API-key issue/revoke/
rotate per tenant, per-key quotas and rate limits, usage stats, data-version status, "rebuild &
purge," and health/status. It is a client of the Directorium API.

The admin SPA and public site ship as **static assets** (Cloudflare-cached) on authenticated PHP
endpoints; auth is PHP sessions + hashed passwords (optional 2FA). Privacy-first throughout:
cookieless analytics, minimal/no PII, no third-party trackers.

## Status

Pre-release — **v0.1.0 in progress**. See the [roadmap](ROADMAP.md).

## Stack

PHP + MySQL on DreamHost, Cloudflare in front. Node is build-time only (static asset build); no
Python.

## Development

Work branches off `develop`, lands via squash PRs with Conventional-Commit titles, and releases are
cut automatically by release-please.

## Licence

© 2026 Directorium. Licensed under **AGPL-3.0-or-later** (see [LICENSE](LICENSE)). The compiled
calendar dataset is released under **CC0**.
