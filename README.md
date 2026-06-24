# idr.to marketing site

Static site for [idr.to](https://idr.to), built with [Astro](https://astro.build) and deployed to GitHub Pages.

## Development

```bash
npm install
npm run dev
```

## Build

```bash
npm run build
npm run preview
```

## Deploy

Pushes to `main` trigger `.github/workflows/deploy.yml` (GitHub Pages).

Custom domain: `CNAME` → `idr.to`

## Site map

| Path | Content |
|------|---------|
| `/` | Product overview, on-prem workloads, addressing snapshot |
| `/addressing` | v1 URI grammar, DEF, mirror HTTPS, `*.idr` |
| `/architecture` | P2P vs signaling vs relay, data billing |
| `/pricing` | Personal / Enterprise / data bundles |
| `/case-study/ollama` | M4 Mac Mini + Ollama walkthrough |
| `/isv` | Browser SDK & Dart SDK |
| `/faq` | FAQ by persona |
| `/evaluate` | 30-day signaling trial signup |
| `/checkout` | Mock Stripe purchase flow |

Previous single-file HTML marketing content (pre-v1 URI examples) is **deprecated** and removed.
