# Edelleye Digital

**Precision engineering and algorithmic growth strategies for high-velocity brands.**

We've spent 30 years opening doors that don't open from the inside.

## About Edelleye Digital

Edelleye Digital is a strategic growth partner for leading companies seeking transformation and accelerated revenue. We're not another agency—we're an execution engine.

We don't just build websites; we build a marketing cadence, and help you get your products and services to market in a way that scales with your ambitions. Through design, strategy, systems, and execution, we amplify teams through **strategic partnerships that build execution capacity, compress timelines, and move revenue at scale**. We don't add overhead—we amplify your team's impact.

Edelleye is the instrument for brand transformation and revenue growth. The best option for leading companies who want to get to the next level.

### Our Track Record

- **12+ SaaS products** built from vision to market
- **50+ client partnerships** across technology, commerce, and growth-stage companies
- **$2.5M+ ARR** generated through algorithmic growth strategies and platform acceleration

### Our Approach

We believe that pattern recognition and systems thinking are the foundations of sustainable growth. We make complexity legible, turning business challenges into executable roadmaps. Our methodology emphasizes precision engineering, data-driven decision making, and iterative velocity.

## Services

Edelleye Digital operates across five core service areas:

- **Marketing** — Platform strategy, demand generation, algorithmic positioning, and revenue acceleration
- **Design** — User experience, brand strategy, interface systems, and visual identity
- **Systems** — SaaS infrastructure, technical architecture, platform engineering, and scalability
- **Operations** — Go-to-market execution, process optimization, operational efficiency, and team enablement
- **Growth Strategy** — Product-market fit analysis, positioning, revenue modeling, and scale planning

We engage through **strategic partnerships** combining our expertise with your team's vision—compressing timelines, reducing risk, and moving revenue at scale.

## Portfolio & Case Studies

Our portfolio spans platform strategy, SaaS transformation, product development, and revenue growth across diverse industries:

- **Nokia, Palm/Be, ET Water** — Foundational mobile and IoT product work
- **Nomadz** — Community platform scaling and engagement
- **Green Life** — Sustainable commerce and marketplace transformation
- **And more** — Digital transformation engagements across tech, finance, and consumer sectors

See the full portfolio at the **[Live site](https://leemwilliams-eng.github.io/Edelleye/)**.

## Technical Stack

Edelleye's website is built with modern, performant tools optimized for production:

- **HTML5** — Semantic, accessible markup
- **Tailwind CSS** (compiled) — Utility-first styling via `edelleye.css` (~41KB, 95% smaller than CDN)
- **Google Fonts** — Plus Jakarta Sans (headlines, bold/extrabold), Inter (body copy)
- **Material Symbols Outlined** — Icon library
- **Calendly** — Booking widget for consultation scheduling

### Pages

- **Home** (`index.html`) — Hero, brand philosophy, capabilities overview, and methodology
- **Offering** (`offering.html`) — Service categories with capability panels and detailed bento grid
- **Portfolio** (`portfolio.html`) — Case studies, methodology modal, and approach documentation
- **Pricing** (`pricing.html`) — Service tiers (Growth, Scale, Bespoke), cadence levels, and engagement philosophy

## Design System

| Token | Value | Usage |
|-------|-------|-------|
| Primary | `#75d1ff` (turquoise) | Accents, buttons, highlights |
| Secondary | `#C8811A` (orange) | Emphasis, icons, secondary CTAs |
| Background | `#000000` | Canvas |
| Surface Container Low | `#1b1b1b` | Card backgrounds, panels |

**Typography:**
- Headlines: Plus Jakarta Sans, bold/extrabold, tight tracking (`letter-spacing: -0.02em`)
- Body: Inter, regular weight, 1.6 line height

## Local Development

### Setup
```bash
npm install
```

### Build CSS
After adding new Tailwind classes to any HTML file:
```bash
npm run build:css
```

This scans all `*.html` files and regenerates `edelleye.css`. **Always commit both the HTML and CSS together.**

### CSS Architecture

Edelleye migrated from Tailwind CDN (~3MB runtime JS) to compiled CSS (~41KB) on 2026-04-07, improving First Contentful Paint by 95%.

- `tailwind.config.js` — Shared config across all pages
- `input.css` — Three `@tailwind` directives
- `edelleye.css` — Generated output, loaded before page `<style>` blocks

**Important specificity note:** Inline `style=` attributes override both Tailwind utilities and page-level CSS. Use inline styles for unique utilities or design tokens not present in scanned HTML.

### Responsive Breakpoints

| Tier | Range | Tailwind Prefix |
|------|-------|-----------------|
| Phone | 0–639px | default |
| Large phone | 640–767px | `sm:` |
| Tablet | 768–1023px | `md:` |
| Desktop | 1024px+ | `lg:` |

All pages are fully responsive across these tiers. Hamburger navigation activates at the `md:` breakpoint.

## Image Assets

All images must follow strict conventions for Linux/case-sensitive GitHub Pages:

- **Lowercase with hyphens** — e.g., `robot-face-hero.png`, not `RobotFaceHero.png`
- **Local to repo** — no Google Drive links, external hosting, or CDN URLs
- **Case-matched in git** — Verify with `git ls-files *.png`

Mismatch = 404 in production. Always cross-reference `git ls-files` output with HTML `src=` attributes before committing.

### Key Assets

- `robot-face-hero.png` — Home page hero background
- `edelleye-header-brand-03.png` — Navigation logo (all pages)
- `edelleye-social-media-cubes.png` — Philosophy panel
- `edelleye-cloud.png`, `edelleye-eye-hero.png`, `edelleye-racks.png` — Service panels
- Portfolio images: `nomadz-*`, `datascension-*`, `real-estate-*`, `tulsawcr-*`, `digital-trend-*`, `gardner-*`

## Key Features

- **Bento Grid Layout** — Flexible multi-column panels with responsive stacking
- **Case Studies Modal** — Embedded case study cards accessible from the portfolio (click "View Case Study")
- **Methodology Modal** — Interactive methodology overview with Agile principles, sprint cadence, and measurable outcomes
- **Mobile Navigation** — Hamburger menu for screens under 768px, full navigation on desktop
- **Calendly Integration** — In-page booking widget for consultation scheduling
- **Responsive Design** — All pages adapt across phone, tablet, and desktop viewports

## Contributing

1. Clone the repo
2. Make changes to HTML or add new Tailwind classes
3. Run `npm run build:css` if you modified utilities
4. Test responsive behavior across all breakpoints
5. Verify image filenames match `git ls-files *.png` output
6. Commit both HTML and `edelleye.css` together

## License

This project operates under the **Creative Commons Attribution License** standard.

**You are free to:**
- Share, adapt, and build upon this work
- Use commercially or non-commercially
- Create derivative works

**Under the condition that you:**
- **Attribute** the original work to Edelleye Digital
- **License** any derivative works under the same Creative Commons Attribution terms
- **Provide attribution** in any published version or fork (credit Edelleye Digital as the source)

For full license details, see [Creative Commons](https://creativecommons.org/).

## Questions?

- **GitHub Issues:** [Edelleye Issues](https://github.com/leemwilliams-eng/Edelleye/issues)
- **Website:** [leemwilliams-eng.github.io/Edelleye/](https://leemwilliams-eng.github.io/Edelleye/)
