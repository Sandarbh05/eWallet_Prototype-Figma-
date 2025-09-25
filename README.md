# FlowIN — E‑Wallet Application (Figma) — Full README

> This document collects every page, style, component, and design decision you provided for the FlowIN e‑wallet Figma project.
---

## Table of Contents

1. Project summary
2. Goals & target users
3. File & page structure (what's in the Figma file)
4. Global design principles
5. Breakpoints & responsive rules
6. Page-by-page detailed documentation
   - 6.1 Thumbnail / Cover
   - 6.2 Mobile — Lo‑Fi (wireframes)
   - 6.3 Desktop — Lo‑Fi (wireframes)
   - 6.4 Mobile — Hi‑Fi
   - 6.5 Desktop — Hi‑Fi
   - 6.6 Style Guide (visual tokens)
   - 6.7 Customized Styles
   - 6.8 Used Components
7. Component inventory (detailed)
8. Tokens, naming conventions & structure for handoff
9. Accessibility & interaction notes
10. Exporting assets & developer handoff checklist
11. Suggested next steps, testing & versioning
12. Appendix: useful snippets and examples

---

## 1) Project summary

**FlowIN** is a Figma UI/UX design project for an e‑wallet application. The deliverables captured inside the Figma file include:

- Project cover / thumbnail
- Low‑fidelity wireframes (mobile and desktop)
- High‑fidelity polished screens (mobile and desktop)
- A style guide and customized Figma text/color styles
- A components page with all reusable elements (buttons, inputs, icons, rating, etc.)

The goal of this README is to be a single-source documentation that describes the visual system, interactions, accessibility considerations, and practical handoff artifacts required for development.

---

## 2) Goals & target users

**Primary goals**
- Communicate the product value clearly and quickly via the marketing/home screens.
- Provide a clean path to purchase (product browsing → detail → checkout → success).
- Build trust through consistent visual language (typography, spacing, colors).
- Produce an organized design system to speed up developer handoff.

**Target users (summary)**
- Busy people who want a fast and secure way to pay and manage small purchases.
- Users who prefer mobile-first flows but also use desktop for longer sessions.
- People who value clarity, recallable actions (clear CTAs) and social sharing of purchases.

---

## 3) File & page structure (what's in the Figma file)

```
FlowIN Figma Project
├── 01_Thumbnail_Cover
├── 02_Mobile_LoFi
├── 03_Desktop_LoFi
├── 04_Mobile_HiFi
├── 05_Desktop_HiFi
├── 06_Style_Guide
├── 07_Customized_Styles
└── 08_Used_Components
```

Each page contains multiple frames/flows. Frames are named to match the flow (e.g., `Home`, `Product-Details`, `Checkout`, `Order-Success`). Keep this naming pattern — it helps when exporting or giving devs prototype links.

---

## 4) Global design principles

- **Clarity first**: use whitespace and clear hierarchy so that price and primary CTAs are visually dominant.
- **Progressive disclosure**: show high‑level information up front, allow users to reveal details (e.g., product features) when needed.
- **Consistency**: reuse styles and components everywhere (same button sizes, same spacing rules, same radii).
- **Affordance**: visual cues for interactable elements (raised/filled buttons, outlined buttons for secondary actions).
- **Trust & security**: clear copy and secure UI patterns on payment screens (padlock icon, masked card numbers, subtle microcopy).

---

## 5) Breakpoints & responsive rules

**Recommended base breakpoints** (adjust as needed depending on final front-end framework):

- Mobile (small): 360 × 812 (iPhone SE min); design at 375 × 812 typical mobile viewport
- Mobile (large / phablet): 412 × 915
- Tablet: 768 × 1024
- Desktop: 1280 × 768 (base)
- Wide desktop: 1440+ (responsive expansion)

**Grid**
- Baseline grid: 8px system (4px optional for fine tuning)
- Desktop — 12 column grid; gutter 24px; content max width 1200–1280px
- Mobile — single column flow, edge spacing 16px

Spacing scale: 4, 8, 12, 16, 20, 24, 32, 40, 48, 64 (use these tokens for margins/padding)

---

## 6) Page‑by‑page detailed documentation

Below each page we list: purpose, frames, interaction notes, copy suggestions, accessibility hints and handoff tips.

### 6.1 Thumbnail / Cover (Project cover)

**Purpose**
- Visual anchor for the project. Used as the Figma thumbnail and as the cover image when sharing on GitHub/Behance/Dribbble or when exporting the project preview.

**Composition**
- Central wallet illustration overlaying a phone mockup.
- Surrounding iconography (shopping cart, globe, mail) to indicate app domain.
- Soft gradients and subtle textures to convey modern finance-tech.

**Design & export notes**
- Export at multiple sizes (400x300, 1200x800) for thumbnails and social previews.
- Provide a square 1:1 and a 16:9 variant for different platforms.

**Copy suggestion**
- Project tagline (subtitle): "A simple, secure mobile-first e‑wallet experience"

---

### 6.2 Mobile — Lo‑Fi (wireframes)

**Frames included**
- `Home / Marketing` — hero image mock, marketing headline, primary CTA (Buy Now), secondary CTA (Learn More)
- `Product-List` (if present) — product cards
- `Product-Details` — product image, price, description, features list, add to cart CTA
- `Checkout` — input fields for email and card details, quantity, shipping cost, order total, purchase CTA
- `Order-Success` — success messaging, social share CTAs

**Wireframe annotations**
- CTA placement: primary CTAs in the hero and product detail should appear above the fold.
- Product image: full width at top of product detail; include a small floating CTA (add to cart) for quick actions.
- Feature tiles: three features in a single row (or stacked on small screens) to communicate benefits quickly.

**Interaction & validation**
- Form validation: inline errors beneath inputs (red text + icon)
- Keyboard type: numeric keyboard for card/CVC, date picker for MM/YY
- Disabled state: Purchase CTA disabled until required fields are filled

**Accessibility**
- Use minimum 44px touch targets for CTAs and controls
- Provide clear alt text for product images in prototype annotations

**Handoff**
- Annotate required microcopy and success/error states in Figma comments so dev knows expected messages.

---

### 6.3 Desktop — Lo‑Fi (wireframes)

**Frames included**
- `Landing / Marketing` — wide hero with left/right split: marketing message + product tiles
- `Product-Details` — large product preview + description column
- `Checkout` — order summary on the right, form on the left
- `Order-Success` — celebratory image with tracking CTA and social buttons

**Layout notes**
- Use extra horizontal space to show additional product context (reviews, related items, functionality cards).
- Checkout layout: show product summary + price breakdown on the same screen as the payment form to reduce cognitive load.

**Interaction notes**
- Hover states for product cards (elevate and show quick-add button)
- Persistent topnav with icons (profile, share, more)

**Handoff**
- Provide desktop spacing tokens and alt image sizes for product preview (e.g., 800px wide hero image)

---

### 6.4 Mobile — Hi‑Fi

**What’s included**
- Final visual treatments: real imagery and sample devices, gradients, brand colors, and typography implemented
- Onboarding / splash frames, fully styled hero, product pages, checkout forms, and success states

**Key design decisions**
- Visual hierarchy: large H1 hero, supportive H2/H3 for sections; CTA uses gradient primary button for emphasis
- Imagery: sample images used for hero and product previews; image crops chosen to communicate trust/security

**Microcopy / CTA examples**
- Button labels: `Buy Now`, `Add to Cart`, `Purchase`, `Track My Order`
- Payment field CTAs: `Enter card details`, `Apply coupon` (if applicable)

**Motion / prototyping**
- Use Figma prototype transitions for: add-to-cart animation, checkout progression, and order success celebration.
- Recommended transitions: `Smart Animate` for card flip / add‑to‑cart micro interactions; `Dissolve` for simple screen changes.

**Handoff**
- Include a prototyping flow with clickable hotspots and an ordered flow from `Home` → `Product` → `Checkout` → `Success`.

---

### 6.5 Desktop — Hi‑Fi

**What’s included**
- Fully styled desktop screens mirroring mobile hi‑fi but utilizing wider layout and additional content areas (newsletter panel, bigger hero, testimonials or tips)

**Key design decisions**
- Large hero image with overlaid CTA and a product carousel below
- Checkout: visually separated blocks for `Order Summary` and `Card Input` with clear totals and shipping breakdown
- Order-success: social sharing box (icons for Instagram, LinkedIn, X/Twitter) highlighted

**Accessibility & performance**
- Avoid heavy hero images without optimized versions — provide multiple image sizes for responsive loading.

---

### 6.6 Style Guide (visual tokens)

This page contains the visual tokens and sample imagery used as references.

**Typography**
- H1 — 72px (hero/main headings)  
- H2 — 48px (section headings)  
- H3 — 24px (subheadings)  
- H4 — 18px (small headings / labels)  
- Body (Paragraph) — 16px (default)  

> In Figma these styles were created as `Text styles`: `H1, Alt H1, H2, Alt H2, H3, Alt H3, H4, Alt H4, Para, Alt Para`.

**Color palette (tokens)**

You provided named color styles in Figma: `Primary-1` `Primary-2` `Primary-3`, `Info-1`–`Info-3`, `Success-1`–`Success-3`, `Border-1`–`Border-3`, and `Background-1`.

- Use `Primary` tokens for main CTAs and prominent UI accents.
- Use `Info` palette for informational UI elements or subtle highlights.
- Use `Success` palette for success states and confirmations.
- Use `Border` tokens for outlines and separators.
- Use `Background-1` as the default page background or surface tone.

**Imagery**
- `Samples` (finance & app UI images) and `Themes` (landscape-based mood imagery) were included to help pick a final mood (vibrant / natural / gradient).

**Spacing & radii**
- Spacing scale (8px system): `4, 8, 12, 16, 24, 32, 40, 48, 64`.
- Radii: `r-sm: 6px`, `r-md: 12px`, `r-pill: 9999px` (used for pill-shaped CTA buttons in hi-fi)

---

### 6.7 Customized Styles

This page is the actual Figma `Styles` panel snapshot exported in your assets. It contains the project’s canonical text and color styles. Use these to maintain consistency between screens and to implement tokens in CSS variables or theme files.

**What to include in the Figma style page**
- Exact text style names: `H1`, `Alt H1`, `H2`, `Alt H2`, `H3`, `Alt H3`, `H4`, `Alt H4`, `Para`, `Alt Para`.
- Color tokens with clear semantic names (don’t use raw hex names in code; use semantic tokens):
  - `--color-primary-1`, `--color-primary-2`, `--color-primary-3`
  - `--color-info-1`, etc.
  - `--color-success-1`, etc.
  - `--color-border-1`, etc.
  - `--color-bg-1`

**Designer notes**
- Keep `Alt` text styles for tight spaces or alternative typography needs.
- Keep `Alt` color variations for hover/focus/pressed states.

---

### 6.8 Used Components

A sacrament page that visually demonstrates component states and available variants. The frames you provided show a set of buttons (solid and gradient), checkboxes, star ratings, and input field styles.

**General guidance**
- Organize components into named groups: `Buttons/Primary`, `Buttons/Secondary`, `Forms/Input`, `Forms/Checkbox`, `Feedback/Rating`, `Cards/Product`, `Navbar/Topbar`, `Icons`.
- Use `Variants` in Figma where applicable (e.g., Button variant with properties `size: sm|md|lg`, `state: default|hover|active|disabled`, `variant: filled|outline|ghost|gradient`).

---

## 7) Component inventory (detailed)

Below are details for each major component, recommended props/variants, and usage guidance for developers.

### Buttons
Variants and guidance:
- `Button.Primary.Filled` — large, pill style for primary CTAs (e.g., `Buy Now`, `Purchase`).
  - Sizes: `sm` (32px height), `md` (44px), `lg` (56px) — use md as default on mobile and md/lg on desktop for hero.
  - States: `default`, `hover` (slight lift or stronger shadow), `active` (pressed), `disabled` (reduced opacity + no pointer)
  - Use `Primary-1` or gradient as background.

- `Button.Secondary.Outline` — outlined with 1px border, no fill (for `Learn More` or auxiliary CTAs)
- `Button.Fullwidth` — full width bars used for checkout CTAs (e.g., `Purchase`) with comfortable padding
- `Button.Success` — green filled style for positive actions (use `Success` tokens)

Accessibility: Ensure color contrast on text is AA/AAA compliant. Disabled buttons should also have the appropriate `aria-disabled` attribute.

### Inputs
- `Input.Text` with label (top) and helper text (optional). States: `default`, `focus`, `error`.
- `Input.CreditCard` — format mask for card number, show card logo, masked characters for security.
- `Input.Date` — `MM/YY` with validation and `aria-describedby` for errors.

Error state pattern: border turns `--color-border-error` (use semantic token), show inline message under the input.

### Checkbox / Toggle
- `Checkbox` — square box with check state. Include keyboard navigation and `aria-checked`.
- `Toggle` — pill shaped for on/off features (saves as boolean in code)

### Rating / Stars
- `Rating` — up to 5 stars; display both interactive (for review input) and static (read-only) states.
- Provide `aria-label` describing the rating (e.g., "4 out of 5 stars").

### Cards
- `Card.Product` — product image, title, short desc, price and CTA (Add to cart)
- `Card.Info` — small information card with icon and short copy

### Top Navigation / Header
- Left: logo
- Center/right: nav icons (home, profile, share, menu) — ensure touch targets are 44px

---

## 8) Tokens, naming conventions & structure for handoff

**Figma naming conventions**
- Pages: `01_Thumbnail`, `02_Mobile_LoFi`, etc.
- Frames: `Home`, `Product-Details`, `Checkout`, `Order-Success`
- Components: `Button/Primary/Filled`, `Input/Text`, `Card/Product`
- Variants: use `property:value` style for variant properties in Figma (example: `size:md | variant:filled | state:default`).

**CSS token examples** (for developer handoff)

```css
:root {
  --color-primary-1: /* copy hex from Figma */;
  --color-primary-2: /* copy hex */;
  --color-success-1: /* copy hex */;

  --font-base: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial;
  --font-size-h1: 72px;
  --font-size-h2: 48px;
  --font-size-h3: 24px;
  --font-size-h4: 18px;

  --space-1: 4px;
  --space-2: 8px;
  --space-3: 16px;
  --radius-pill: 9999px;
}
```

**Export asset naming**
- `product-hero@1x.jpg`, `product-hero@2x.jpg` (for high DPI)
- `icon-add-to-cart.svg` (vector icons are preferred)

---

## 9) Accessibility & interaction notes

- **Contrast**: Ensure text on primary buttons has a contrast ratio of at least 4.5:1 (AAA for large text is 3:1).
- **Touch targets**: 44px × 44px minimum for mobile.
- **Keyboard navigation**: All interactive elements must be reachable with keyboard `Tab` and have visible focus states.
- **ARIA**: Use `aria-label`, `aria-pressed`, `aria-disabled`, `aria-invalid` where appropriate.
- **Form validation**: Provide inline error messages with clear instructions on how to fix the issue.

---

## 10) Exporting assets & developer handoff checklist

**From Figma**
- Export icons as SVG (named consistently)
- Export raster images in `webp`/`jpg` @1x and @2x for mobile and desktop
- Provide a prototype link with the starting frame and ordered user flow
- Provide an `assets` folder zipped with exported images and icons

**Handoff checklist (for each screen)**
- [ ] All layers properly named
- [ ] Text styles and color styles applied
- [ ] Components set as Figma components and grouped in Variant sets
- [ ] Prototype hotspots and flow order set
- [ ] Exportable assets marked and exported
- [ ] Developer notes or comments added for edge cases and microcopy

---

## 11) Suggested next steps, testing & versioning

**Quick wins**
- Run a 5-user unmoderated usability test for the checkout flow. Focus on the payment form (time to enter card details, error recoverability).
- Annotate copy variations in Figma to test which CTA wording converts best (e.g., `Buy Now` vs. `Complete Purchase`).

**Versioning**
- Tag major milestones in the file name: `v1.0-basic-flow`, `v1.1-styles-updated`, etc.
- Keep a short changelog page in the Figma file describing what changed per version.

---

## 12) Appendix: useful snippets and examples

**Example of a Button variant table**
```
Button/Primary/Filled
- props: size=md, state=default
- css: padding 12px 24px, border-radius: var(--radius-pill), background: var(--color-primary-1)

Button/Secondary/Outline
- props: size=md, state=default
- css: border: 1px solid var(--color-border-1), background: transparent
```

**Example microcopy for checkout**
- `Card Information` label → helper: `We do not store your full card number.`
- `Purchase` confirmation → `Your order is on the way. Check email for tracking info.`

---
