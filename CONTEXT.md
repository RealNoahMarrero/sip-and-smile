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

- Warm, friendly, personable  
- Loves frogs (subtle nods OK in friendly theme; hidden in luxury theme)  
- Site tone should feel **approachable**, not overly luxurious — though a luxury theme variant exists for comparison  
- First-person copy from Lisa’s perspective in the About section  

## Legal footer (required)

> Sip & Smile Bar is a DBA of MARRERO LLC. Services provided under MARRERO LLC. All clients are subject to standard event-liability waivers.

## Site structure

Single-page HTML site (`index.html`) with these sections:

1. **Hero** — Brand, tagline, CTA → `#contact`  
2. **About** — Lisa intro, photo, license badge  
3. **Services** — Dry Hire Standard  
4. **FAQ** — Service area, event types, home events, pricing, dry hire  
5. **Contact** — Inquiry form (Name, Email, Event Date, Guest Count, Message)  
6. **Footer** — Copyright + legal notice  

## Theme system

Two switchable themes for Lisa to compare preferences:

| | **Friendly** (default) | **Luxury** |
|---|------------------------|------------|
| **Feel** | Warm, casual, approachable | Dark, gold, upscale |
| **Fonts** | Fraunces + Nunito Sans | Cormorant Garamond + Inter |
| **Colors** | Cream, sage green, coral | Charcoal, gold |
| **Hero** | Casual copy, frog accents | “Premium Event Bartending”, gold line |
| **Icons** | Emojis in services | SVG icons |

- Toggle lives in the **header** (☀️ Friendly / ✨ Luxury on mobile).  
- Preference stored in `localStorage` under key `sip-smile-theme`.  
- When Lisa picks a final theme, remove the toggle and lock one theme for production.

## Tech stack

- Plain **HTML** (no build step)  
- **Tailwind CSS** via CDN  
- **Google Fonts** (both theme font sets loaded)  
- Vanilla JS for theme toggle + mobile nav  
- Assets: `lisa.jpg` (About section headshot)  

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

- [ ] Form backend (Formspree, Netlify Forms, custom API, etc.) — form currently `action="#"`  
- [ ] Custom domain  
- [ ] Final theme chosen (toggle still present)  
- [ ] Social links (explicitly deferred)  
- [ ] Public email / phone (explicitly deferred)  

## Naming notes

- Use **“Sip & Smile”** in customer-facing branding (avoid “Bar” — sounds like a brick-and-mortar).  
- Use **“Sip & Smile Bar”** only in legal/DBA footer text.  
- Do **not** describe the business as a physical bar or venue.

## Stakeholders

- **Lisa Alicea** — business owner, final approver on tone and design  
- **Noah Marrero** — building / maintaining the site; MARRERO LLC
