# JIGERZ Shopify Theme — Design Handoff

## Overview
This is a complete design reference package for the **JIGERZ** premium men's clothing ecommerce store. The designs cover 3 core pages of a Shopify storefront. Your job is to implement these designs in the Shopify theme (Liquid + CSS) connected to GitHub.

## About the Design Files
The HTML files in this bundle are **high-fidelity design references** — prototypes showing exact intended look, colors, typography, spacing, and interactions. They are NOT production code. Your task is to **recreate these designs in Shopify Liquid templates** using Shopify's theme architecture.

## Fidelity
**HIGH FIDELITY** — These are pixel-perfect mockups with:
- Final colors, typography, spacing, and interactions
- All copy, labels, and content finalized
- Hover states, mobile responsive behavior, and animations implemented

---

## Design Tokens

### Colors
```
--black:      #0a0a0a   /* Page background */
--off-white:  #f5f4f0   /* Primary text */
--gold:       #b8975a   /* Accent — CTAs, badges, highlights */
--card-bg:    #141414   /* Card/section backgrounds */
--border:     rgba(255,255,255,0.08)  /* Subtle borders */
--sale-red:   #e85d04   /* Stock urgency indicator */
--cod-green:  #4caf50   /* Cash on Delivery badge */
```

### Typography
```
Headings:  Cormorant Garamond (Google Font) — weights 300, 400, 600, 700
Body/UI:   Barlow (Google Font) — weights 300, 400, 500, 600

Load via:
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;0,700;1,300;1,400&family=Barlow:wght@300;400;500;600&display=swap" rel="stylesheet">
```

### Spacing
```
Page horizontal padding:  60px desktop / 20px mobile
Section vertical padding: 80–100px desktop / 48–60px mobile
Nav height:               72px desktop / 60px mobile
Card gap:                 24px desktop / 12px mobile
```

### Border Radius
```
None — all elements are sharp / square corners (luxury aesthetic)
```

---

## Pages & Screens

---

### 1. Homepage (`JIgerz Store.html`)
**Shopify template:** `templates/index.liquid`

#### Sections (top to bottom):

**A. Promo Bar**
- Gold background (#b8975a), black text
- Font: Barlow 11px, weight 600, letter-spacing 0.15em, uppercase
- Text: "FREE DELIVERY ON ORDERS OVER PKR 2,500 · LIMITED SUMMER SALE — USE CODE JIGERZ10"
- Shopify: Make text editable via section settings

**B. Navigation**
- Sticky, dark background rgba(10,10,10,0.97) with backdrop-filter blur(12px)
- 3-column grid: links left | logo center | actions right
- Logo: centered, height 40px, filter invert(1) (white on dark)
- Nav links: 11px Barlow, letter-spacing 0.15em, uppercase, opacity 0.7 → 1 on hover
- Links: New In · Shop All · T-Shirts · Winter Clearance (Winter Clearance in gold)
- Right side: Search · Account · Bag button (gold background)
- Mobile: hamburger (☰) replaces links, full-screen overlay menu

**C. Hero Section**
- Height: 92vh
- Dark gradient background with subtle gold grid overlay
- Left: editorial content (bottom-left aligned)
  - Eyebrow: "New Collection — Summer 2026" (10px, gold, uppercase)
  - H1: "Summer Essentials 2026" — Cormorant Garamond 84px weight 300
  - Tagline italic: "Not Just A Brand — It's A Bond." (gold, Cormorant 20px italic)
  - Subtext: 13px Barlow, opacity 0.5
  - CTA buttons: "Shop Now" (gold fill) + "Explore Collection" (ghost/outline)
- Right: product image placeholder (360×500px)
- "SS 2026 Collection" label top-left in gold

**D. Scrolling Marquee**
- Dark card-bg background, border top+bottom
- Auto-scrolling text: Premium Imported Fabric ✦ Summer 2026 ✦ Free Delivery 2500+ ✦ Cash On Delivery ✦ JIGERZ — Not Just A Brand
- Animation: 25s linear infinite loop

**E. Category Grid**
- 4 equal columns
- Each card: full-height image with gradient overlay at bottom
- Category names: Cormorant Garamond 24px weight 300
- Categories: T-Shirts (24 Styles) · Polo (10) · Oversized (14) · Accessories (8)
- Hover: image scales 1.04, arrow icon fades in top-right

**F. Trust Bar**
- 4 columns, card-bg background
- Items: Free Delivery · Cash on Delivery · 30-Day Returns · Genuine Quality
- Each: icon (22px) + title (11px bold uppercase) + description (11px, opacity 0.4)
- Dividers between columns

**G. New Arrivals Product Grid**
- 4-column grid, 24px gap
- Section label + title + "View All →" link (right-aligned)
- See Product Card spec below

**H. Brand Values (light section)**
- Background: #f5f4f0 (off-white), text: #0a0a0a
- 2-column: left = large heading, right = 3 numbered values
- Values: 01 Premium Fabric · 02 Modern Fit · 03 Everyday Comfort
- Gold numbered labels, thin top border separator

**I. Testimonials**
- Background: #0d0d0d
- 3-column grid, gold star ratings
- Italic Cormorant Garamond 18px quotes
- Author: 11px uppercase, opacity 0.4

**J. Newsletter**
- Centered, email input + subscribe button (gold)

**K. Footer**
- 4-column grid: Brand description | Shop | Help | Brand links
- Logo white, tagline text opacity 0.35
- Column titles: 10px gold uppercase
- Bottom bar: copyright left, social links right

---

### 2. Collection Page (`JIgerz Collection.html`)
**Shopify template:** `templates/collection.liquid`

#### Layout
- Sticky nav + filter tabs below header
- 2-column layout: 220px sidebar | flex products area

#### Filter Tab Bar
- Horizontal scrollable tabs: All · T-Shirts · Polo · Oversized · Accessories · Sale ✦
- Active tab: gold color, 2px gold bottom border
- Each tab: 11px Barlow, letter-spacing 0.15em, border-right separator

#### Sidebar Filters
- Sticky, 220px wide
- Sections: Category (checkboxes) · Size (pill buttons) · Color (circle swatches) · Price Range (slider) · Availability (checkboxes)
- Active states: gold accent color
- Filter section titles: 10px gold uppercase

#### Sort Row
- Left: "Showing X products"
- Right: sort dropdown + grid toggle (2/3/4 columns)

#### Product Card Spec
```
Container:    cursor pointer
Image:        aspect-ratio 3/4, background #141414, hatched texture overlay
Badges:       New (gold fill) | Sale (dark, border) | Best Seller (white fill)
              Position: top-left, 9px bold uppercase
Wishlist:     top-right, 30px square, fades in on hover
Quick Add:    slides up from bottom on hover, dark bg, uppercase 10px
Name:         13px Barlow weight 400
Price:        Gold Cormorant Garamond 19px weight 600
Compare:      Strikethrough, 12px opacity 0.35
Save badge:   "−18%" gold bg rgba(184,151,90,0.15), 9px
Color dots:   10px circles, bottom of card
Size chips:   9px, border, opacity 0.35
```

---

### 3. Product Detail Page (`JIgerz Product.html`)
**Shopify template:** `templates/product.liquid`

#### Layout
- 2-column grid: gallery left (50%) | product info right (50%)
- Gallery sticky on desktop

#### Image Gallery
- Left column: 76px thumbnail strip | main image
- Thumbnails: 4 images, active = gold border
- Main image: full height, zoom text bottom-right
- Navigation arrows: left/right

#### Product Info (RIGHT COLUMN — critical for conversion)

**Badges Row:**
- "New Arrival" (gold filled)
- "In Stock" (gold outline)
- "💵 Cash on Delivery" (green bg #1a3a1a, green text #4caf50)

**Title:** Cormorant Garamond 44px weight 300, line-height 1.05
**SKU:** 10px, opacity 0.3

**Rating Row:**
- Gold stars ★★★★★
- "4.9 / 5" rating count
- "48 Reviews" link in gold

**Compare-at-Price Box** ⭐ HIGH PRIORITY:
```
Background: rgba(184,151,90,0.08)
Border: 1px solid rgba(184,151,90,0.25)
Padding: 16px 20px
Layout: flex space-between
Left: label "COMPARE AT PRICE" (10px uppercase) + price row
  - Current price: Cormorant Garamond 32px gold
  - Was price: 16px strikethrough opacity 0.4
Right: "SAVE 18%" pill — gold background, black text, 10px bold
```

**Stock Indicator:**
```
Pulsing red dot (animation 1.5s)
Text: "Only 5 pieces left!" in #e85d04
Subtext: "— Order soon" opacity 0.45
```

**Product Bullets (above fold):**
```
✓ Premium Imported Fabric — 100% Ring-Spun Cotton  (gold checkmark)
✓ Stretchable & Breathable — Perfect for Summer
✓ Smart Fit Design — Modern Relaxed Silhouette
Font: 12px Barlow, opacity 0.75
```

**Color Picker:**
- Label: "Color" left + selected color name right (gold)
- Options: 30px circles, active = 2px gold border, hover = scale 1.1

**Size Picker:**
- Pills: min-width 50px, border var(--border), active = gold border + text
- Sold out: opacity 0.2, strikethrough, not clickable
- "Size Guide →" link in gold, right-aligned

**Delivery Line:**
- Dark bg box with truck icon
- "Order now & get delivery in 3–5 business days · Free on orders PKR 2,500+"

**Add to Cart Row:**
- 110px qty control (−/qty/+) | flex Add to Bag button
- Add to Bag: gold background, black text, 12px bold uppercase, 48px height
- On click: turns green "✓ Added!" for 2 seconds

**Buy Now button:**
- Full width, ghost/outline style

**Trust Badges (4 columns):**
- Free Shipping · Cash on Delivery · 30-Day Returns · Genuine Quality

**Accordion Sections:**
- Description · Fabric & Care · Shipping & Returns · Size & Fit
- Open/close with + icon rotating 45deg

**Sticky Mobile CTA (mobile only):**
```css
position: fixed; bottom: 0; left: 0; right: 0;
background: rgba(10,10,10,0.97);
border-top: 1px solid var(--border);
display: flex; align-items: center;
padding: 12px 20px;
```
- Left: product name + price
- Right: gold "Add to Bag" button

**Related Products:**
- 4-column grid
- Each: image + name + price (gold) + compare-at-price

---

## Interactions & Behavior

| Interaction | Behavior |
|---|---|
| Product card hover | Quick add slides up (transform translateY), wishlist fades in |
| Category card hover | Image scales 1.04, arrow appears |
| Nav scroll | Sticky with blur backdrop |
| Mobile nav | Hamburger opens full-screen overlay |
| Size selection | Gold border highlight |
| Color selection | Gold ring + color name updates |
| Add to Cart | Turns green "✓ Added!" for 2 seconds |
| Accordion | Rotates + icon, slides body open |
| Stock dot | Pulsing opacity animation |
| Marquee | Infinite scroll left, 25s duration |
| Gallery thumb | Click switches main image |

---

## Mobile Responsive Breakpoint: 768px

| Element | Mobile Behavior |
|---|---|
| Nav | Collapse to hamburger |
| Hero | Hide product placeholder, stack buttons |
| Categories | 2×2 grid |
| Product grid | 2 columns |
| Gallery | Horizontal thumb strip, 400px main |
| PDP layout | Single column (gallery top, info below) |
| Sidebar | Hidden (use filter tabs only) |
| Sticky CTA | Visible on product page |
| Footer | 2-column grid |

---

## Shopify Implementation Notes

### Section Files Needed:
```
sections/
  announcement-bar.liquid
  header.liquid
  hero-banner.liquid
  marquee-strip.liquid
  category-grid.liquid
  trust-bar.liquid
  product-grid.liquid
  brand-values.liquid
  testimonials.liquid
  newsletter.liquid
  footer.liquid
```

### Collection Template:
```
templates/collection.liquid
sections/collection-filter-sidebar.liquid
sections/collection-product-grid.liquid
```

### Product Template:
```
templates/product.liquid
sections/product-gallery.liquid
sections/product-info.liquid
sections/related-products.liquid
snippets/compare-at-price.liquid
snippets/size-picker.liquid
snippets/color-swatches.liquid
snippets/trust-badges.liquid
```

### Key Shopify Liquid Variables:
```liquid
{{ product.title }}
{{ product.price | money }}
{{ product.compare_at_price | money }}
{{ product.available }}
{{ variant.inventory_quantity }}
{{ product.images }}
{{ product.variants }}
{{ collection.products }}
```

### Compare-at-Price Logic:
```liquid
{% if product.compare_at_price > product.price %}
  {% assign savings = product.compare_at_price | minus: product.price %}
  {% assign savings_percent = savings | times: 100 | divided_by: product.compare_at_price %}
  <div class="compare-price-box">
    <span class="compare-now">{{ product.price | money }}</span>
    <span class="compare-was">{{ product.compare_at_price | money }}</span>
    <span class="save-pill">SAVE {{ savings_percent }}%</span>
  </div>
{% endif %}
```

---

## Assets

| Asset | Description | Location |
|---|---|---|
| Logo | JIGERZ brand logo (white/black) | `uploads/logo-1776684626245.png` |
| Product images | Placeholder — add real photos | Shopify admin > Files |
| Category images | Placeholder — add real photos | Shopify admin > Files |
| Hero image | Dark luxury model shot needed | Shopify admin > Files |

---

## Files in This Package

| File | Purpose |
|---|---|
| `JIgerz Store.html` | Homepage design reference |
| `JIgerz Collection.html` | Collection/Shop page reference |
| `JIgerz Product.html` | Product detail page reference |
| `logo.png` | Brand logo |
| `README.md` | This document |

---

## How to Give This to Claude Code

1. Download this ZIP file
2. Open your Shopify theme in VS Code / Claude Code
3. Drop this ZIP into your project folder
4. Tell Claude Code:

> "I have a design handoff package in the `jigerz_handoff` folder. Please read the README.md and implement the designs into my Shopify theme. The HTML files are design references — recreate them in Shopify Liquid templates with the design tokens and interactions described."

---

## Brand Summary
- **Brand:** JIGERZ
- **Tagline:** "Not Just A Brand — It's A Bond"
- **Market:** Pakistan (PKR pricing)
- **Products:** Men's T-Shirts, Polo, Oversized Tees, Accessories
- **Season:** Summer 2026
- **Aesthetic:** Dark luxury editorial (Fear of God / Represent inspired)
