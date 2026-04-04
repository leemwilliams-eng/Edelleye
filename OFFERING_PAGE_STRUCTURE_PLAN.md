# OFFERING PAGE — REVISED STRUCTURE & IMPLEMENTATION PLAN

---

## COPY REVISIONS (APPROVED)

### HEADER STATEMENT (REVISED)
**Old:** "We don't solve the problem you think you have. We find the problem you can't see yet. Then we rebuild everything around that."

**New:** "We don't solve the problem you think you have. We find the problem you can't see yet. Then we methodically reveal the specific focus needed, and create execution targets."

### CLOSING STATEMENT (REVISED)
**Old:** "No smoke. No performance. Just the math. The tiers above reflect how we work: transparent about what you're paying for, honest about the scope, and direct about the outcome."

**New:** "No smoke. No mirrors. A measurable execution plan. The tiers above reflect how we work: transparent about what you're paying for, honest about the scope, and direct about the outcome. It will be obvious that we have been here before, learned from you, and are there to help you move the needle."

---

## PAGE STRUCTURE — 3 SECTIONS

### SECTION 1: TOP THIRD (No Changes)
- Existing header, nav, and hero are locked
- No layout changes
- Copy updates only where needed for consistency with new voice

### SECTION 2: MAIN BODY (New Service Line Card Layout)

#### 2A. KEY CONCEPT OPENER (New)
**Purpose:** Position a higher-level strategic concept that shows how multiple services work together.

**Concept: "Market Placement and Targeting"**
(Example positioning)

How we achieve this:
- Strategic positioning and messaging (Strategy & Acquisition)
- Visual identity and creative execution (Design Services)
- Technical platform and conversion optimization (Software Development)
- Audience targeting and campaign execution (Marketing & Advertising)
- Organizational alignment and execution (Business Operations & Leadership)

Copy approach: "To achieve market placement, we use design and creative, strategy and acquisition, software and technology, business operations, and advertising—working as one system, not separate services."

**Length:** 150-200 words. Sets up the 5 service lines as integrated rather than siloed.

---

#### 2B. FIVE SERVICE LINE CARDS (Alternating Layout)

**Layout Pattern:**
- Card 1: 2/3 left (service description + design element) + 1/3 right (key concept panel)
- Card 2: 1/3 left (key concept panel) + 2/3 right (service description + design element)
- Card 3: 2/3 left (service description + design element) + 1/3 right (key concept panel)
- Card 4: 1/3 left (key concept panel) + 2/3 right (service description + design element)
- Card 5: 2/3 left (service description + design element) + 1/3 right (key concept panel)

**Card Anatomy:**

Left Panel (2/3):
- Service line headline
- Description + proof points
- Real numbers
- Brand voice closing ("We don't just...")

Right Panel (1/3) or Left Panel (1/3):
- Key Concept box (design element, visual treatment)
- Core concept from the service (e.g., "Algorithmic Scaling" for card 2)
- Single-line descriptor
- Subtle visual graphic/icon

**Each Card Content:**

**Card 1: MARKETING & ADVERTISING (2/3 left + 1/3 right)**

Left: 
- "Strategic Campaigns That Move Revenue"
- Google/Amazon/Facebook/LinkedIn partner ratings (85/100, 95/100, 80/100, 90/100)
- Service description + real numbers (32% average revenue increase)
- "We don't just place ads. We build systems..."

Right:
- Key Concept: "Algorithmic Targeting"
- Design element/graphic
- Single-line: "Precision at scale"

---

**Card 2: SOFTWARE DEVELOPMENT (1/3 left + 2/3 right)**

Left:
- Key Concept: "Cloud-Native Architecture"
- Design element/graphic
- Single-line: "Systems that grow"

Right:
- "Build Systems That Scale"
- Services: Cloud (AWS/GCP), AI (Claude/ChatGPT/MCPs), DevOps, microservices
- Real numbers: 40% time-to-market reduction, 100M+ users at Nokia, $0→$8M ARR at ET Water
- "We don't just code. We build..."

---

**Card 3: STRATEGY & ACQUISITION (2/3 left + 1/3 right)**

Left:
- "Roadmaps, M&A, Revenue Growth"
- Services: Roadmaps, revenue growth, M&A, partnerships, ecosystem, affiliate programs
- Real numbers: $8M ARR, 40% global market share, $1.2B+ acquisitions
- "We don't consult. We advise..."

Right:
- Key Concept: "Strategic Positioning"
- Design element/graphic
- Single-line: "Decisions that move needles"

---

**Card 4: DESIGN SERVICES (1/3 left + 2/3 right)**

Left:
- Key Concept: "Visual Systems"
- Design element/graphic
- Single-line: "Strategy made visible"

Right:
- "Visual Identity & Creative Direction"
- Services: Branding, visual systems, content strategy, UX/UI, art direction
- Real numbers: 100M+ users, iconic smartphone design (Palm Treo)
- "Design isn't decoration. It's strategy."

---

**Card 5: BUSINESS OPERATIONS & LEADERSHIP (2/3 left + 1/3 right)**

Left:
- "Scale From Startup to Enterprise"
- Services: Organizational strategy, team building, operational efficiency, customer success, strategic planning
- Real numbers: Teams shipping to 100M+ users, 94% customer retention
- "We don't manage. We build..."

Right:
- Key Concept: "Execution Excellence"
- Design element/graphic
- Single-line: "Organizations that win"

---

### SECTION 3: CLOSING (Bottom Third)

#### 3A. PRICING SECTION (Existing structure, no layout change)
- GROWTH: $1,500
- SCALE: $5,000
- BESPOKE: Custom

#### 3B. CLOSING STATEMENT (Revised)
**"No smoke. No mirrors. A measurable execution plan."**

"The tiers above reflect how we work: transparent about what you're paying for, honest about the scope, and direct about the outcome. It will be obvious that we have been here before, learned from you, and are there to help you move the needle."

---

## DESIGN ELEMENTS (For HTML Implementation)

### Card Components:
- `.service-card` — Container for alternating layout
- `.service-card.left-2-3` — 2/3 left + 1/3 right
- `.service-card.left-1-3` — 1/3 left + 2/3 right
- `.service-panel` — Left/right panel wrapper
- `.service-description` — Left panel content
- `.key-concept` — Right/left concept box

### Key Concept Box:
- Border-left: 4px primary (#75D1FF or #3AB0E2)
- Background: surface-container-low (#1B1B1B)
- Padding: 24px
- Border-radius: 8px
- Font: Headline-MD (GT Walsheim with -0.04em letter-spacing)
- Icon/graphic: Simple, minimal (SVG or design element)

### Alternating Pattern CSS:
```css
.service-card:nth-child(odd) .service-description {
  grid-column: 1 / 3;
}
.service-card:nth-child(odd) .key-concept {
  grid-column: 3 / 4;
}
.service-card:nth-child(even) .key-concept {
  grid-column: 1 / 2;
}
.service-card:nth-child(even) .service-description {
  grid-column: 2 / 4;
}
```

---

## IMPLEMENTATION CHECKLIST

- [ ] Update header statement in HTML
- [ ] Add "Who We Serve" section (already in copy, needs HTML integration)
- [ ] Build Key Concept opener section
- [ ] Create 5 service line cards with alternating layout
- [ ] Add design elements/graphics to key concept boxes
- [ ] Update closing statement
- [ ] Test responsive behavior (cards stack on mobile)
- [ ] Verify tone consistency across all copy
- [ ] Test on live site (edelleye.net/offering)
- [ ] Screenshot for review before final push

---

## TOTAL PAGE WORD COUNT: ~850 words

---

## NOTES

**Tone Voice Calibration:**
- Prosecutorial openings maintained ("We don't just...", "We don't consult...", "We don't manage...")
- "Methodically reveal" and "execution targets" language matches your voice precision
- "No mirrors" addition strengthens the transparency commitment
- "It will be obvious that we have been here before" grounds the credibility claim in experience

**Design System Alignment:**
- All cards use existing Edelleye design system (black background, turquoise primary, glass effects)
- Letter-spacing maintained at -0.02em globally
- Logo and nav stay locked (existing top third)
- Key concept boxes follow bento grid aesthetic already on homepage

**Cloud & AI Integration:**
- Explicitly mentioned in Service Line 2 (Software Development)
- Mentioned in Key Concept opener ("intelligent systems")
- Integrated into real numbers examples (ET Water cloud platform, Claude/ChatGPT integration)

---

## READY FOR CLAUDE CODE?

**Recommendation: YES, use Claude Code.**

**Reasoning:**

1. **Complexity:** This page has 5+ interactive cards with CSS grid alternating layouts, multiple design elements, and precise responsive behavior. It's beyond simple copy-paste HTML.

2. **Precision:** The alternating 2/3-1/3 layout needs clean CSS that won't break on mobile. Claude Code can write the grid system, media queries, and test responsiveness in context.

3. **Design Elements:** Key Concept boxes need SVG icons or design elements. Claude Code can generate those inline or set up the structure for them.

4. **Testing:** Claude Code can build the page, then we can test it immediately in a browser tab, adjust, and iterate without pushing to production each time.

5. **Speed:** Building in Claude Code first, getting approval, then integrating to GitHub is faster than ping-ponging HTML edits in the chat.

6. **Safety:** We won't touch the live site until you've approved the design AND content.

**Claude Code Workflow:**
1. Create the full offering.html file in Claude Code
2. Build the layout with all 5 cards, alternating pattern, design elements
3. Style according to Edelleye design system
4. Test in a browser tab
5. You review and approve
6. Push to GitHub and live site

**Ready to proceed in Claude Code?**
