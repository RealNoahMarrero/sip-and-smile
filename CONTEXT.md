# Sip & Smile — Project Context

Reference document for anyone (or any AI agent) working on this site. Keep this updated when business details or site behavior change.

## Business overview

| Field | Detail |
|-------|--------|
| **Public brand** | Sip & Smile |
| **Legal / DBA** | Sip & Smile Bar (DBA of MARRERO LLC) |
| **Owner / operator** | Lisa Alicea |
| **Entity** | MARRERO LLC |
| **Service type** | Event bartending — **Dry Hire** only |
| **Location** | Based in **Dayton, OH** |
| **Travel** | Will travel for the right event / price |
| **Experience** | Less than one year bartending; strong personality and professionalism |
| **License** | Ohio Bartender License |
| **Pricing** | Inquiry-only (no public rates) |
| **Contact** | Form-only for now (no public email, phone, or social links) |

## Dry hire model

Clients purchase **100% of the alcohol**. Lisa supplies:

- Custom mixers  
- Fresh garnishes  
- Ice  
- Bar tools  

This must remain clearly stated on the site.

## Event focus

- **Primary highlight:** Weddings  
- **Also serves:** Birthdays, showers, corporate events, private parties, and similar celebrations  
- **No minimum guest count** to advertise  

### Private home policy

Residential events are **case-by-case**. Lisa will serve at **larger homes** that can comfortably fit the guest count and provide a safe, suitable bartending setup. Standard/smaller residential settings may not be a fit. Wording should stay diplomatic — see FAQ on the live site.

## About Lisa (voice & personality)

- Warm, friendly, personable — even within the upscale visual design  
- Loves frogs (not currently on the site; can add subtle touches if desired)  
- First-person copy from Lisa’s perspective in the About section  

## Legal footer (required)

> Sip & Smile Bar is a DBA of MARRERO LLC. Services provided under MARRERO LLC. All clients are subject to standard event-liability waivers.

## Site structure

Single-page HTML site (`index.html`) with these sections:

1. **Hero** — Brand, tagline, CTA → `#contact`  
2. **About** — Lisa intro, photo, license badge  
3. **Services** — Dry Hire Standard  
4. **How It Works** — 3-step booking process + event type badges  
5. **FAQ** — Service area, event types, home events, pricing, dry hire  
6. **Contact** — Inquiry form (Name, Email, Venue Location, Event Date, Guest Count, Message)  
7. **Footer** — Copyright + legal notice  

## Design (final — luxury theme)

Lisa chose the **luxury** look. Single theme only — no toggle.

| | Detail |
|---|--------|
| **Feel** | Dark charcoal, gold accents, upscale |
| **Fonts** | Cormorant Garamond (headings) + Inter (body) |
| **Hero** | “Premium Event Bartending”, gold divider line |
| **Icons** | SVG icons in services section |

## Tech stack

- Plain **HTML** (no build step)  
- **Tailwind CSS** via CDN  
- **Google Fonts** — Cormorant Garamond + Inter  
- Vanilla JS for mobile nav only  
- Assets: `lisa.jpg` (About + link previews), `hero.jpg` (blurred hero background), `logo.png` (official logo, on file), `favicon.svg` (browser tab, transparent)  
- **Production URL:** https://sipandsmileevents.netlify.app/ (update canonical/OG tags if custom domain changes)  

## Mobile requirements

- Responsive layout (mobile-first)  
- Hamburger menu below `md` breakpoint  
- Touch targets ≥ ~48px  
- Hero uses `100dvh`  
- Form and FAQ usable on small screens  

## Repository

- **GitHub:** https://github.com/RealNoahMarrero/sip-and-smile  
- **Branch:** `master`  
- **Files:** `index.html`, `lisa.jpg`, `CONTEXT.md`  

### Local preview

```bash
# Open directly
start index.html

# Or local server (optional)
npx --yes serve .
```

### GitHub Pages (optional hosting)

Repo → Settings → Pages → Deploy from branch `master`, root `/`.

## Not yet implemented

- [x] Form backend — **Netlify Forms** (`name="contact"`, honeypot enabled). Configure email notifications in Netlify → Site → Forms → Form notifications  
- [ ] Custom domain (update `canonical`, `og:url`, and `og:image` to absolute custom-domain URLs)  
- [x] Final theme chosen — **luxury** (toggle removed)  
- [x] Favicon (`favicon.svg`)  
- [x] Open Graph / Twitter link preview meta tags  
- [x] JSON-LD structured data (ProfessionalService)  
- [x] How It Works section  
- [ ] Image compression (`hero.jpg` / `lisa.jpg` are ~1MB each — compress before launch)  
- [ ] Social links (explicitly deferred)  
- [ ] Public email / phone (explicitly deferred)  

## Naming notes

- Use **“Sip & Smile”** in customer-facing branding (avoid “Bar” — sounds like a brick-and-mortar).  
- Use **“Sip & Smile Bar”** only in legal/DBA footer text.  
- Do **not** describe the business as a physical bar or venue.

## Stakeholders

- **Lisa Alicea** — business owner, final approver on tone and design  
- **Noah Marrero** — building / maintaining the site; MARRERO LLC
