# Saga Projects — Site Reference

## Overview

**Local:** `/Users/mk/Documents/saga-site/`
**Live:** https://saga-projects.com (Vercel, deploys from `main` via GitHub push to `pooopalooop/saga-projects`)
**Deploy command:** `git push origin main`

## Tech stack

- Plain HTML/CSS/JS — no framework, no build step
- Google Fonts: Inter (400, 500, 600, 700, 800) — only typeface used
- Formspree for contact form
- `menu.js` for mobile nav toggle

## Design tokens

| Token | Value |
|---|---|
| `--bg` | `#0a0a0a` |
| `--surface` | `#161616` |
| `--accent` | `#c8a2ff` (soft purple) |
| `--text` | `#f0f0f0` |
| `--text-muted` | `#a0a0a0` |
| `--border` | `rgba(255,255,255,0.08)` |
| `--radius` | `10px` |
| `--max-w` | `1100px` |

## Logo mark

Two concentric stroked circles (SVG inline):
```html
<svg class="logo__mark" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" aria-hidden="true">
  <circle cx="10" cy="10" r="9" fill="none" stroke="currentColor" stroke-width="1.2"/>
  <circle cx="10" cy="10" r="5.5" fill="none" stroke="currentColor" stroke-width="1.2"/>
</svg>
```
Card bullet icon: `&#9678;` (◎)

## Pages

- `index.html` — homepage
- `about.html`
- `products.html` — Solutions
- `industries.html`
- `contact.html`
- `styles.css`, `menu.js`
- `favicon.svg` — dark bg, purple concentric rings

## Homepage section order

1. **Hero** — "Your partner for / engineered sealing solutions"
2. **Why Work With Us** — headline: "Sealing is our Specialty"; subtitle: "Application expertise, certified manufacturing, and one point of contact from design review to production."
3. **Solutions** (Gallery Teaser) — "Seals for every application"
4. **Who We Represent** — headline: "Performance Sealing, Inc (PSI)" (styled as `section__title` h2)
5. **Industries** — headline: "Where we specialize"
6. **Contact** — "Have a sealing challenge?"

## OG image

`images/og-image.png` — 1200×630 PNG, Saga Projects branding. Referenced in `index.html` as absolute URL `https://saga-projects.com/images/og-image.png`.

## Brand kit

Visual brand reference: https://claude.ai/code/artifact/1fd8619c-0430-4bc2-b684-b1f502ef278f
Also saved as `brand-kit.html` in the repo root.

## Internal tools hub

`tools.html` — password-protected, not linked in public nav. Lives at saga-projects.com/tools.html.
- Auth: SHA-256 hash + localStorage (stays logged in per device)
- To add a tool: add an `<a class="tool-card">` block in `tools.html`
- Tools linked:
  1. NADS Builder — https://nads-builder.vercel.app/
  2. Cold Outreach — https://nads-builder.vercel.app/outreach.html
  3. Send — https://nads-builder.vercel.app/send.html
  4. SEMICON West Field Guide — https://claude.ai/artifact/XpzbqeQ1i79q8W8nd2MsRn

## Key rules

- No decorative hero ring — `.hero::before` was removed
- Section alternating backgrounds: `.section--alt` = `--surface`, plain `.section` = `--bg`
- No em-dashes in copy
- Buttons: `.btn--primary` (accent fill), `.btn--outline` (accent border)
- Email addresses reversed in HTML for spam protection, corrected by CSS `direction: rtl`

## Who we represent

**PSI (Performance Sealing, Inc)** — AS9100D-certified, spring-energized polymer seals, PTFE rotary lip seals, proprietary Duron® materials, precision CNC machining. Saga Projects LLC is their manufacturer's rep.
