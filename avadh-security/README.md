# Avadh Security — Website

Static site. No build step — just upload the contents of this folder to any static host
(Netlify, Vercel, GitHub Pages, Cloudflare Pages, S3 + CloudFront, nginx/Apache).

## Structure
```
avadh-security/
├── index.html                 # Homepage
├── pentest/
│   └── web/
│       └── index.html         # Web Application Pentesting page  (URL: /pentest/web)
└── assets/
    ├── img/                   # Hero avatars + illustration images
    │   ├── avatar-1.jpg
    │   ├── avatar-2.jpg
    │   ├── developer.png
    │   └── pentester.png
    └── logos/                 # Trusted-by marquee logos  (PLACEHOLDERS — replace)
        ├── compass.svg
        ├── epic-games.svg
        ├── nba.svg
        ├── roblox.svg
        └── visa.svg
```

## Hosting notes
- Deploy so that `/pentest/web/` serves `pentest/web/index.html` (default on every static host).
- Homepage references assets with relative paths (`assets/...`) and links pages with absolute
  paths (`/pentest/web`, `/contact`, etc.), so the homepage must sit at the site root.

## Before going live
1. **Replace the logo placeholders** in `assets/logos/` with the real brand SVGs
   (the files are text-only stand-ins right now).
2. **Other nav links are not built yet** — `/pentest/network`, `/pentest/mobile`,
   `/pentest/cloud`, `/pentest/ai`, `/engagement-models`, `/resources`, `/pricing`,
   `/contact`, `/privacy`, `/terms`. Add those pages (or point the links elsewhere).
3. Fonts (Google Fonts) and Bootstrap load from CDN — no action needed, but you may
   self-host them for offline/air-gapped deployments.

Built pages: Homepage + Web Application Pentesting.
