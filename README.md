# Athlete Connection

**Marketing website for a basketball sports group — bridging high school, college, and professional players with representation, career development, and global opportunities.**

Built with **Astro 5** and **Tailwind CSS 3**. Static-generated, deploys anywhere.

---

## What this project is

Athlete Connection is a boutique sports agency focused on basketball. This repo is their public-facing marketing site — the front door for athletes, agents, and teams looking to engage the group's services.

The site covers five service lines:

- **Athlete Management**
- **Consulting Services**
- **Brand & Marketing Development**
- **Team & Agent Partnerships**
- **Events & Exposure**

Pages: `index` (hero + services marquee), `services` (detailed service cards), `contact` (inquiry form), `thank-you` (post-submission).

---

## Tech stack

| Layer | Choice | Why |
|-------|--------|-----|
| Framework | **Astro 5** | Zero-JS by default, ideal for a content-driven marketing site with fast Core Web Vitals |
| Styling | **Tailwind CSS 3** | Utility-first, no CSS files to maintain, easy to keep the design system consistent |
| Language | **TypeScript** (tsconfig) | Type safety in component props and layout imports |
| Build | Astro's built-in Vite pipeline | Single-command production build to `./dist/` |

The site ships as fully static HTML/CSS with a marquee animation in CSS — no runtime JavaScript unless a page needs it.

---

## Project structure

```
athlete_connection/
├── src/
│   ├── layouts/
│   │   └── BaseLayout.astro        — shared page shell (head, fonts, global CSS)
│   ├── components/
│   │   ├── CardNav.astro           — top-of-card navigation
│   │   ├── FloatingCard.astro      — main content card wrapper
│   │   └── ServiceCard.astro       — reusable service tile
│   ├── pages/
│   │   ├── index.astro             — home / hero
│   │   ├── services.astro          — service line detail
│   │   ├── contact.astro           — inquiry form
│   │   └── thank-you.astro         — post-submit confirmation
│   └── styles/                     — Tailwind entry + custom CSS
├── public/                         — static assets (favicon, images)
├── astro.config.mjs                — Astro + Tailwind integration
├── tailwind.config.js              — design tokens
└── tsconfig.json
```

---

## Running locally

Prereq: **Node.js 20+**.

```bash
npm install
npm run dev        # http://localhost:4321
```

Other commands:

| Command | Action |
|---------|--------|
| `npm run build` | Production build → `./dist/` |
| `npm run preview` | Preview the production build locally |
| `npm run astro -- --help` | Astro CLI reference |

---

## Deployment

The build output in `./dist/` is a fully static site, so any static host works:

- **Netlify** — connect the GitHub repo, auto-detects Astro, redeploys on push (recommended)
- **Vercel** — same idea, also auto-detects
- **GitHub Pages** — needs a small Actions workflow to run `npm run build` and publish `./dist/`
- Any static CDN or S3 bucket

---

## License

All rights reserved. This repository is public for portfolio purposes; the content, brand, and design belong to Athlete Connection.

## Contact

Developer: Chasity Matthias — [cmat165@wgu.edu](mailto:cmat165@wgu.edu)
