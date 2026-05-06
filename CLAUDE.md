# CLAUDE.md — Sunshine Road Motors Website

## Project Overview
Static single-page website for **Sunshine Road Motors**, an auto mechanic & car repair service in Tottenham, VIC, Australia. Design style is inspired by [Blok Watches](https://blokwatches.com/?ref=godly) — dark, bold, premium modern aesthetic.

## Business Details
- **Name:** Sunshine Road Motors
- **Type:** Auto mechanic service / car repair
- **Address:** 1/243 Sunshine Road, Tottenham, VIC, Australia
- **Phone:** 0412 751 394
- **Logo:** `Logo.png` (gold/gear mechanic logo on transparent background)

## Design System

### Color Palette
| Role | Hex | Usage |
|------|-----|-------|
| Background | `#0a0a0a` | Page background |
| Surface | `#141414` | Card/section backgrounds |
| Surface raised | `#1e1e1e` | Hover states, elevated cards |
| Accent gold | `#d4a017` | Primary accent, CTAs |
| Accent gold light | `#f0c040` | Hover gold, highlights |
| Border | `#2a2a2a` | Dividers, card borders |
| Text primary | `#ffffff` | Headings |
| Text secondary | `#a0a0a0` | Body text, captions |
| Text muted | `#606060` | Placeholder, footnotes |

### Typography
- **Headings font:** `'Barlow Condensed', sans-serif` (Google Fonts) — bold, condensed, impactful
- **Body font:** `'Inter', sans-serif` (Google Fonts) — clean, readable
- **Display size:** `clamp(3rem, 8vw, 7rem)` for hero headlines
- **Section titles:** `clamp(2rem, 5vw, 3.5rem)`, uppercase, letter-spacing: 2px
- **Body:** `1rem / 1.6rem`
- **Small caps / labels:** uppercase, 0.75rem, letter-spacing: 3px

### Layout
- **Max content width:** 1280px, centered with `margin: auto`
- **Grid:** CSS Grid + Flexbox, 12-column conceptual grid
- **Section padding:** `clamp(4rem, 8vw, 8rem) 0`
- **Container padding:** `0 clamp(1.5rem, 5vw, 4rem)`

### Spacing Scale
`4px | 8px | 16px | 24px | 32px | 48px | 64px | 96px | 128px`

## Required Features

### Navigation
- Fixed top nav, dark background `rgba(10,10,10,0.95)` with backdrop blur
- Logo left-aligned, nav links right-aligned
- Mobile: hamburger menu (CSS-only or minimal JS toggle)
- Active section highlighting via scroll spy
- Smooth scroll to sections

### Hero Section
- Full-viewport height (`100vh`)
- Background: dark car workshop image with dark overlay (`rgba(0,0,0,0.65)`)
- Large display headline + sub-headline
- Two CTAs: primary (gold filled) + secondary (outlined)
- Animated text reveal on load (fade-in + translateY)

### Animations & Interactions
- **Scroll-triggered reveal:** elements fade-in + slide-up as they enter viewport (IntersectionObserver)
- **Hover on cards:** scale(1.03) + box-shadow glow in gold
- **Hover on buttons:** color shift, slight scale, transition 0.3s ease
- **Nav hover:** gold underline sweep animation
- **Counter animation:** numbers count up when stats section enters viewport
- **Image hover:** subtle zoom (scale 1.05) with overflow hidden on container

### Back to Top Button
- Fixed bottom-right, circular gold button
- Hidden when near top, visible on scroll (> 300px)
- Smooth scroll to top on click
- Hover: brighter gold + scale

### Cards / Service Items
- Dark background `#141414`, border `1px solid #2a2a2a`
- Icon + title + description layout
- On hover: border color → gold, slight lift with box-shadow

### Sections Required
1. **Navigation** — logo + links + mobile menu
2. **Hero** — full-screen with tagline and CTA
3. **Services** — grid of service cards (6 services)
4. **Stats** — animated counters (years experience, cars serviced, etc.)
5. **Why Choose Us** — feature highlights
6. **Gallery** — photo grid (workshop/cars)
7. **About** — team/story section
8. **Testimonials** — customer reviews
9. **Contact** — address, phone, map embed, hours
10. **Footer** — links, social, copyright

## Images
- **Logo:** `Logo.png` (use at ~180px wide in nav, ~240px in footer)
- **External images:** Use Unsplash direct URLs for automotive/mechanic content
  - Hero bg: `https://images.unsplash.com/photo-1486262715619-67b85e0b08d3?auto=format&fit=crop&w=1920&q=80`
  - Engine: `https://images.unsplash.com/photo-1580274455191-1c62238fa333?auto=format&fit=crop&w=800&q=80`
  - Workshop: `https://images.unsplash.com/photo-1625047509168-a7026f36de04?auto=format&fit=crop&w=800&q=80`
  - Mechanic team: `https://images.unsplash.com/photo-1549317661-cf369843c6c0?auto=format&fit=crop&w=800&q=80`
  - Tire/wheel: `https://images.unsplash.com/photo-1555215695-3d1506e56e2e?auto=format&fit=crop&w=800&q=80`

## Code Standards
- **Single file:** All HTML + CSS + JS in `index.html` (no build tools needed)
- **No frameworks:** Pure HTML5, CSS3, vanilla JavaScript
- **CSS Variables:** All design tokens defined in `:root {}`
- **Mobile first:** Base styles for mobile, `@media (min-width: 768px)` for tablet, `@media (min-width: 1024px)` for desktop
- **Semantic HTML:** Use `<header>`, `<nav>`, `<main>`, `<section>`, `<footer>`, `<article>`
- **Accessibility:** `alt` text on images, `aria-label` on icon buttons, focus styles visible
- **Performance:** Lazy-load images (`loading="lazy"`), minimal JS, CSS animations prefer `transform` and `opacity`

## Screenshot & Review Process
When making design changes:
1. Take a screenshot of the current state
2. Compare side-by-side with reference: https://blokwatches.com/?ref=godly
3. Identify differences in: spacing, typography weight, color contrast, animation feel
4. Apply adjustments to match the premium, dark, bold aesthetic
5. Delete screenshots once satisfied with the comparison

## Reference Design Key Traits (from Blok Watches)
- **Bold, oversized typography** that dominates sections
- **Dark backgrounds** with high-contrast white/gold text
- **Minimal decoration** — let content breathe with generous whitespace
- **Sharp card edges** (low border-radius, max 4-8px)
- **Premium feel** through restraint: not many colors, not many fonts
- **Full-width section breaks** with slightly different background shades
- **Subtle grid lines** or borders to separate content areas
- **CTAs are prominent** — gold/accent color, never blending into background
