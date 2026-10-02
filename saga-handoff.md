# Saga Projects — Claude Project Brief

## Starter Prompt

You are helping maintain and improve the Saga Projects LLC marketing website at saga-projects.com. Saga Projects is a manufacturer's representative connecting design engineers and procurement teams with high-performance sealing solutions. They exclusively represent PSI (Performance Sealing, Inc), an AS9100D-certified manufacturer. The site's goal is to establish credibility, showcase PSI's product range, and drive leads through a "Schedule an Appointment" CTA. The site is plain HTML/CSS — no framework, no build step. All changes are made directly to the source files and deployed by pushing to the main branch on GitHub (pooopalooop/saga-projects), which triggers a Vercel deploy to saga-projects.com.

---

## Business Context

**Saga Projects LLC** is a manufacturer's rep — they connect engineers with the right sealing products, not a manufacturer themselves. They represent **PSI (Performance Sealing, Inc)**, their only current line.

**Target audience:** Design engineers and procurement teams at OEM manufacturers.

**Key industries:** Aerospace & Space, Medical Devices, Analytical & Clinical Lab, Semiconductor Equipment, Autonomous Defense, Energy (Oil, Gas, Solar), Battery Technology, Industrial Automation, Fluid & Gas Handling.

### Contacts
- **Stu Krupoff** — stu@saga-projects.com — (949) 337-9563
- **Mike Krupoff** — mike@saga-projects.com — (510) 915-7119

---

## Site Overview

- **Stack:** Plain HTML, CSS, vanilla JS — no framework, no build step
- **Font:** Inter (Google Fonts) — weights 400, 500, 600, 700, 800 — only typeface
- **Local path:** /Users/mk/Documents/saga-site/
- **GitHub:** pooopalooop/saga-projects (public)
- **Live site:** https://saga-projects.com (Vercel)
- **Deploy command:** `git push origin main`

### Pages
- `index.html` — homepage (primary marketing page)
- `about.html` — about Saga Projects
- `products.html` — Solutions (PSI product range)
- `industries.html` — industry detail pages
- `contact.html` — Schedule an Appointment (Formspree form)
- `styles.css` — all styles, single file
- `menu.js` — mobile nav toggle only

---

## Homepage Section Order & Copy

1. **Hero** — "Your partner for / engineered sealing solutions"
2. **Why Work With Us** — headline: "Sealing is our Specialty" / subtitle: "Application expertise, certified manufacturing, and one point of contact from design review to production."
3. **Solutions** — "Seals for every application" / gallery of 3 seal images
4. **Who We Represent** — "Performance Sealing, Inc (PSI)" / PSI description
5. **Industries** — "Where we specialize" / 9-tile grid of industries
6. **Contact** — "Have a sealing challenge?" / both contacts listed

---

## Design System

### Color Tokens
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

### Logo Mark (SVG inline)
```html
<svg class="logo__mark" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" aria-hidden="true">
  <circle cx="10" cy="10" r="9" fill="none" stroke="currentColor" stroke-width="1.2"/>
  <circle cx="10" cy="10" r="5.5" fill="none" stroke="currentColor" stroke-width="1.2"/>
</svg>
```

Card bullet icon: `&#9678;` (◎) — used as decorative mark throughout.

---

## Brand & Copy Rules

- No em-dashes in copy — use commas or restructure the sentence
- No decorative hero ring — the `.hero::before` pseudo-element was intentionally removed
- Section backgrounds alternate: `.section--alt` = `--surface`, plain `.section` = `--bg`
- Email addresses are reversed in HTML for spam protection — CSS `direction: rtl` corrects display
- Primary CTA is always "Schedule an Appointment" linking to contact.html
- Tone: direct, technical, confident — no fluff, no buzzwords, engineer-facing
- PSI is always "AS9100D-certified" — include certification when describing them

---

## Who We Represent

**Performance Sealing, Inc (PSI)** is an AS9100D-certified manufacturer of high-performance spring-energized polymer seals. They use proprietary Duron® materials and precision CNC machining for critical applications. Product range includes spring-energized seals, PTFE rotary lip seals, O-rings, and custom geometries. Primary markets: aerospace, medical, semiconductor, and energy industries.

---

## Internal Tools Hub

`tools.html` — password-protected page at saga-projects.com/tools.html. Not linked anywhere on the public site. Central link hub for Mike and Stu.

- Auth: client-side SHA-256 hash, persisted in localStorage (stays logged in per device)
- To add a new tool: add an `<a class="tool-card">` block in `tools.html` and push

| Tool | URL |
|---|---|
| NADS Builder | https://nads-builder.vercel.app/ |
| Cold Outreach | https://nads-builder.vercel.app/outreach.html |
| Send | https://nads-builder.vercel.app/send.html |
| SEMICON West Field Guide | https://claude.ai/artifact/XpzbqeQ1i79q8W8nd2MsRn |

## Key Assets & Links

- **Brand kit (visual artifact):** https://claude.ai/code/artifact/1fd8619c-0430-4bc2-b684-b1f502ef278f
- **Handoff brief (visual artifact):** https://claude.ai/code/artifact/6d41b2b1-a805-4fad-869e-a3eb3b6ecf88
- **OG image:** `images/og-image.png` — 1200×630 PNG, absolute URL in meta tag
- **Favicon:** `favicon.svg` — dark bg (#0a0a0a), purple concentric rings
- **CLAUDE.md:** technical reference in repo root (for Claude Code sessions)
- **saga-handoff.html:** visual version of this document in repo root
