# Security Policy

## Scope

This repository hosts **Embodied Frontier Robot Community** — a static, serverless website served entirely via GitHub Pages.

Because the site is static (no backend, no database, no user accounts, no server-side code), the traditional web attack surface (SQL injection, server-side code execution, credential theft, brute-force login) **does not apply** to the served content.

Security protections in place:

- **Transport**: All traffic is served over HTTPS only (GitHub Pages).
- **Platform protection**: DDoS mitigation and CDN caching are handled by the GitHub Pages / Fastly infrastructure.
- **Hardening headers**: GitHub Pages injects `X-Content-Type-Options: nosniff`, `X-Frame-Options` and `Referrer-Policy` on responses.
- **Page-level policy** (`index.html` / `404.html`): a Content-Security-Policy restricts resource origins (scripts, styles, fonts, images), `frame-ancestors 'none'` blocks clickjacking, and a Permissions-Policy disables camera / microphone / geolocation / payment and other browser APIs. See the `<meta>` block in each page's `<head>`.
- **No third-party JavaScript** is loaded; the only external resources are the font stylesheet (miaoda.feishu.cn) and AI-generated illustration images (aka.doubaocdn.com).
- **Crawler control**: `robots.txt` blocks known aggressive scrapers.
- **Link hygiene**: all external links open with `rel="noopener"`.

## Reporting a vulnerability

This site contains no executable server logic, so most reports will relate to **content, links, or dependencies** rather than exploitable code. Still, please report anything you believe is a genuine security issue:

- **Preferred**: open a private discussion via the repository Issues, or email the maintainers (see repository profile).
- Include: a description of the issue, the affected URL, the expected vs. actual behavior, and (if applicable) a minimal reproduction.

We aim to acknowledge reports within 5 business days and respond with a fix or mitigation plan.

## Responsible disclosure

Please do not use automated scanners or attempt to disrupt the service while investigating. Give the maintainers reasonable time to respond before any public disclosure.

© 2026 Embodied Frontier Robot Community
