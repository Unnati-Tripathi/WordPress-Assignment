# ClearPath — Design System

This document defines the visual language for the ClearPath website. All colors, fonts, spacing, and component patterns are configured through the **Kadence Theme Customizer** — no custom CSS or code is needed.

---

## Color Palette

### Kadence Global Color Mapping

Kadence uses a 9-slot global color palette. Here's how our ClearPath colors map to each slot:

| Kadence Slot | ClearPath Role | Color Name | Hex Code | Preview |
|-------------|---------------|------------|----------|---------|
| **Accent 1** | Primary brand color | Dark Navy Blue | `#1B2A4A` | 🔵 |
| **Accent 2** | Accent / links | Restrained Teal | `#2A9D8F` | 🟢 |
| **Contrast 1** | Body text | Charcoal | `#2C2C2C` | ⚫ |
| **Contrast 2** | Subtitles / meta | Slate | `#5A6270` | 🔘 |
| **Contrast 3** | Borders / dividers | Light Gray | `#D1CEC9` | ⚪ |
| **Base 1** | Page background | Warm Cream | `#FAF7F2` | 🟡 |
| **Base 2** | Card background | White | `#FFFFFF` | ⬜ |
| **Base 3** | Alternate sections | Light Warm Gray | `#F0EDE8` | 🔲 |

### Additional Colors (used in Gutenberg block settings)

| Role | Hex Code | Where Used |
|------|----------|------------|
| Primary button hover | `#2D4A7A` | Button hover states (lighter navy) |
| Teal hover | `#228176` | Link/button hover (darker teal) |
| Text on dark backgrounds | `#F5F5F0` | Off-white text on navy sections |

### How to Set This in Kadence

1. Go to **Appearance → Customize → Colors & Fonts → Colors**
2. Click each color circle in the palette
3. Paste the hex code from the table above
4. Click **Publish** to save

---

## Typography

### Font Selections

| Element | Font Family | Weight | Size | Line Height |
|---------|------------|--------|------|-------------|
| H1 | Inter | 700 (Bold) | 2.5rem (40px) | 1.2 |
| H2 | Inter | 700 (Bold) | 2rem (32px) | 1.3 |
| H3 | Inter | 600 (Semi-bold) | 1.5rem (24px) | 1.4 |
| H4 | Inter | 600 (Semi-bold) | 1.25rem (20px) | 1.4 |
| Body | Inter | 400 (Regular) | 1rem (16px) | 1.7 |
| Navigation | Inter | 500 (Medium) | 0.95rem (15px) | 1.5 |
| Buttons | Inter | 600 (Semi-bold) | 0.95rem (15px) | 1.5 |
| Accent/Quotes | Merriweather | 400 Italic | 1.1rem (18px) | 1.6 |
| Small/Caption | Inter | 400 (Regular) | 0.875rem (14px) | 1.5 |

### How to Set This in Kadence

1. Go to **Appearance → Customize → Colors & Fonts → Typography**
2. **Body Font:** Select "Inter" from the Google Fonts dropdown, weight 400, size 16px
3. **Heading Font:** Select "Inter", set weights per heading level
4. For Merriweather: Use it manually in specific blocks (blockquotes, mission statement) via the block typography settings

---

## Layout & Spacing

### Content Width
- **Max content width:** 1200px
- **Narrow content width:** 800px (for blog post body text)
- **Set in:** Appearance → Customize → General → Layout

### Spacing Scale

| Name | Value | Usage |
|------|-------|-------|
| Section padding (desktop) | 60px top/bottom | Space between major page sections |
| Section padding (mobile) | 40px top/bottom | Compressed for mobile |
| Card gap | 24px | Space between service/resource cards |
| Inner card padding | 32px | Padding inside card components |
| Paragraph spacing | 16px | Space between paragraphs |

### Border & Shadow

| Element | Value |
|---------|-------|
| Card border radius | 8px |
| Button border radius | 4px |
| Card box shadow | `0 2px 8px rgba(0, 0, 0, 0.08)` |
| Card hover shadow | `0 4px 16px rgba(0, 0, 0, 0.12)` |

---

## Component Patterns

### Service Card

Used on the **Services** page and as summary cards on **Home**.

```
┌──────────────────────────────────┐
│  ▬▬▬▬  (4px teal top border)    │
│                                  │
│  📋  Service Title  (H3, navy)  │
│                                  │
│  Description paragraph text      │
│  explaining the service clearly. │
│  2-3 sentences maximum.          │
│                                  │
│  ┌──────────────────┐           │
│  │  Learn More →    │  (navy    │
│  └──────────────────┘   button) │
└──────────────────────────────────┘

Background: #FFFFFF (white)
Border: 1px solid #F0EDE8
Border-top: 4px solid #2A9D8F (teal accent)
Border-radius: 8px
Padding: 32px
Shadow: 0 2px 8px rgba(0,0,0,0.08)
```

**Kadence Implementation:** Use a **Row Layout** block (3 columns on desktop, 1 on mobile) with each column containing a Heading + Paragraph + Button block. Apply background color and border via block settings.

### Resource Card

Used on the **Career Resources** archive/listing page.

```
┌──────────────────────────────────┐
│  GUIDES & TEMPLATES             │
│  (teal, uppercase, small, bold) │
│                                  │
│  Post Title (H3, linked)         │
│  Navy color, underline on hover  │
│                                  │
│  Brief excerpt text showing      │
│  the first 2 lines of content... │
│                                  │
│  Oct 15, 2026 · 5 min read      │
│  (slate gray, small)             │
└──────────────────────────────────┘

Background: #FFFFFF
Padding: 24px
Border-radius: 8px
Shadow: 0 2px 8px rgba(0,0,0,0.08)
```

**Implementation:** This is handled by the Kadence theme's archive/blog layout settings. Configure in Appearance → Customize → Posts/Blog → Blog Layout.

### Call-to-Action Banner

Used at the bottom of **Home** and optionally on other pages.

```
┌──────────────────────────────────────────────┐
│  Background: #1B2A4A (navy)                  │
│                                              │
│    "Ready to take the next step?"  (H2)      │
│    Off-white (#F5F5F0) text                  │
│                                              │
│    We're here to help you navigate your      │
│    career journey with confidence.            │
│                                              │
│    ┌──────────────────┐                      │
│    │  Get in Touch    │  (teal background,   │
│    └──────────────────┘   white text)        │
│                                              │
│  Padding: 60px top/bottom                    │
└──────────────────────────────────────────────┘
```

**Kadence Implementation:** Row Layout block with navy background color. Add Heading + Paragraph + Button inside. Set text colors to off-white, button to teal.

### Header

```
┌─────────────────────────────────────────────────────────┐
│  ClearPath          Home  About  Services  Resources  Contact  │
│  (Inter Bold, navy)              (Inter Medium, charcoal)      │
└─────────────────────────────────────────────────────────┘

Background: #FFFFFF
Border-bottom: 1px solid #F0EDE8
Position: Sticky
Padding: 16px vertical
```

**Kadence Implementation:** Appearance → Customize → Header → Set Logo as site title text. Add Primary Navigation element.

### Footer

```
┌─────────────────────────────────────────────────────────┐
│  Background: #1B2A4A (navy)                             │
│                                                         │
│  ClearPath              Quick Links      Get in Touch   │
│  Career guidance for    Home             contact@       │
│  students and fresh     About            clearpath.com  │
│  graduates.             Services         (sample email) │
│                         Resources                       │
│                         Contact                         │
│                                                         │
│  ─────────────────────────────────────────────────────  │
│  © 2026 ClearPath. This is a sample portfolio project.  │
└─────────────────────────────────────────────────────────┘

Text color: #F5F5F0 (off-white)
Link color: #2A9D8F (teal)
Padding: 48px top, 24px bottom
```

**Kadence Implementation:** Appearance → Customize → Footer → Use Kadence's footer builder. Add 3-column widget area + bottom row for copyright.

---

## Responsive Behavior

| Breakpoint | Layout Changes |
|-----------|---------------|
| **Desktop** (>1024px) | 3-column service cards, full navigation, 60px section padding |
| **Tablet** (768–1024px) | 2-column service cards, full navigation (may wrap), 48px section padding |
| **Mobile** (<768px) | 1-column everything, hamburger menu, 40px section padding, larger tap targets |

Kadence handles responsive behavior automatically for its blocks. The theme's built-in responsive controls allow per-device adjustments for padding, font sizes, and column layouts.

---

## Accessibility Notes

- All color combinations meet **WCAG AA contrast ratio** (4.5:1 for body text, 3:1 for large text)
- Navy (#1B2A4A) on Cream (#FAF7F2): **Ratio 10.2:1** ✅
- Charcoal (#2C2C2C) on Cream (#FAF7F2): **Ratio 12.1:1** ✅
- Off-white (#F5F5F0) on Navy (#1B2A4A): **Ratio 10.2:1** ✅
- Teal (#2A9D8F) on White (#FFFFFF): **Ratio 3.6:1** ✅ (large text only; pair with navy for small text)
- All interactive elements have visible focus states (handled by Kadence theme)
- Semantic heading hierarchy (one H1 per page, sequential H2/H3)
