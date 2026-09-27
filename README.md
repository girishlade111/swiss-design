# Swiss Design

A Swiss-style portfolio landing page built with Next.js — big Helvetica-esque typography, a strict 12-column grid, red/black/white accents, and buttery hover transitions. It is a demo of the International Typographic Style (Swiss Design) applied to a modern personal portfolio.

## What it does

A single-page portfolio site with anchor navigation (Work, About, Contact sections), a bold hero ("SWISS DESIGN"), a project grid with hover states, an about block explaining Swiss design principles, and a contact footer. Fully responsive — the grid collapses cleanly on mobile.

## Features

- One-page portfolio layout: nav → hero → work → about → contact
- Strict 12-column Swiss grid with large display typography
- Red/black/white palette with red hover accents on project cards
- Responsive (mobile-first breakpoints)
- Dark "WORK" section contrast block
- Dark-mode theme provider included (next-themes)
- shadcn/ui components + Tailwind CSS utility styling
- Static export friendly — no backend, no API routes, no server actions

## Tech stack

- Next.js 15.2.8 (App Router, static export)
- React 19, TypeScript
- Tailwind CSS + tailwindcss-animate
- shadcn/ui (Radix UI primitives) + Lucide icons
- next-themes for dark/light theming
- pnpm

## Quick start

```bash
pnpm install
pnpm dev        # http://localhost:3000
```

Build a static export:

```bash
pnpm build      # emits ./out
```

## Project structure

```
app/
  page.tsx        # all sections of the landing page
  layout.tsx      # root layout, theme provider, fonts
  globals.css     # Tailwind + global styles
components/
  theme-provider.tsx
lib/
  utils.ts        # cn() helper
public/           # static assets
styles/           # extra styles
```

## Environment variables

None.

## Deployment

Static export (`output: 'export'`). Any static host works:

- GitHub Pages: build, then push `out/` to the `gh-pages` branch → `https://girishlade111.github.io/swiss-design/`
- Vercel / Cloudflare Pages: connect the repo and deploy (no adapter needed)

Note: `next.config.mjs` sets `basePath: '/swiss-design'` so assets resolve under the GitHub Pages subpath. Remove `basePath` when deploying to a root domain or Vercel.

## License

MIT — free to use and adapt.

---

Built by Girish Lade · [ladestack.in](https://ladestack.in)
