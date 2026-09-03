# Embodied Frontier · Robot Community

**Embodied Frontier Robot Community** — an open exploration and sharing site for embodied intelligence and robotics.

> Where embodied intelligence meets the frontier.

Serving a **global (English-first)** audience at https://jeuigi78638.github.io/embodied-frontier/

## Sections

- **Industry Pulse** (SYS.01): key 2026 embodied-AI milestones by month + representative players
- **Frontier Lab** (SYS.02): plain-language explainers — VLA, world models, tactile sensing, edge inference, dexterous manipulation, embodied navigation
- **Robot Archive & Exchange** (SYS.03): form-factor ecosystem map + community creative submissions
- **Field Notes** (SYS.04): lab-notebook style hands-on explorations

## Tech notes

- Pure static single-page site (native HTML/CSS/JS, no build dependencies, no third-party JS)
- Illustrations are AI-generated and do not represent any specific product
- Content is compiled from public reporting for reference and learning; always defer to official vendor announcements

## Security hardening

See [SECURITY.md](SECURITY.md) for the full policy. Highlights:

- **HTTPS + DDoS protection** provided by GitHub Pages / Fastly at the platform layer
- **Content-Security-Policy** meta on every page restricts script / style / font / image origins; `frame-ancestors 'none'` prevents clickjacking
- **Permissions-Policy** disables camera, microphone, geolocation, payment and other browser APIs
- **robots.txt** blocks known aggressive scrapers
- **Custom 404 page** (`404.html`) with mirrored security policy
- All external links use `rel="noopener"`

## Deploy

Site is deployed to GitHub Pages from the `main` branch (see `.github/workflows/pages.yml`).

## Contributing

Welcome to [Issues](https://github.com/jeuigi78638/embodied-frontier/issues) for submissions, discussion and co-building.

© 2026 Embodied Frontier Robot Community
