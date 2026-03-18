# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Official website for **Broker-Brain**, an AI platform for credit brokerage (mediazione creditizia) in Italy. The site is written in Italian and targets both consumers (B2C) and business partners (B2B).

## Architecture

This is a **single-file static website** — all HTML, CSS, and JavaScript live in `index.html`. There are no build tools, no dependencies to install, and no frameworks.

- `index.html` — the entire site: structure, styles (inline `<style>`), and scripts (inline `<script>`)
- `img/` — static image assets referenced by `index.html`
- `BB_logo.svg` — brand logo (SVG)

## Development

Open `index.html` directly in a browser — no server required. For live-reload during editing:

```bash
npx serve .
# or
python3 -m http.server 8080
```

## Deployment

The site deploys automatically via Vercel or Netlify when changes are pushed to `main`. It can also be served via GitHub Pages from the repo root.

## Site Sections

- **Hero / B2C** — consumer financing (dental, auto, optical, vet, health, home)
- **B2B / Partner** — dashboard and integration for business partners
- **Team** — team profiles
- **Contatti** — contact form with profile selector (cliente / azienda / rivenditore / dentista)

## Design Tokens (CSS variables in `:root`)

| Variable | Value | Use |
|---|---|---|
| `--teal` | `#06AED5` | Primary brand color (blue) |
| `--teal-dark` | `#086788` | Hover states, text, dark sections |
| `--teal-light` | `#39C4E5` | Accents, em highlights |
| `--orange` | `#F0C808` | Action CTA buttons (btn-primary) — golden yellow |
| `--red` | `#DD1C1A` | Hover/danger states (btn-primary hover, orange-dark) |
| `--navy` | `#086788` | Deep blue — text, dark sections |
| `--bg-light` | `#FFF1D0` | Section backgrounds (warm cream) |
| Font | Montserrat 400/600/800 (Google Fonts) | All text |

## Brand Rules (from `guidelines.md`)

- **Font:** Montserrat — weights 400 (body), 600 (subheadings), 800 (H1/display)
- **Tone:** Clear, direct, reassuring — professional but never stiff
- **Slogan:** "Il prestito intelligente, alla velocità del pensiero."
- **Logo icon:** Combines "B" with a 45°-rotated checkmark — symbolises fast approval
- **Hero gradient:** `linear-gradient(45deg, var(--teal), var(--navy))` — always blue→dark-blue at 45°
- **Border radius:** 12px for cards and buttons
- **CTA buttons (golden yellow):** uppercase, font-weight 700, use `btn-primary` class
- **Brand blue buttons:** use `btn-teal` class
- **Icons:** thin line icons matching Montserrat stroke weight
