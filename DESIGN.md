# Design System Specification: Cinematic Tool-Obsessed High-Contrast

## 1. Overview & Creative North Star
**The Creative North Star: "The Obsidian Instrument"**

This design system moves away from the generic SaaS "whiteboard" look and towards the precision of a high-end cinematic tool. It is designed to feel like a premium optics lens or a professional grading suite—authoritative, dark, and hyper-focused.

The visual identity is defined by a **Pure Black (#000000)** foundation, creating an infinite canvas where elements don't just sit; they emerge. We break the "template" aesthetic by utilizing intentional asymmetry, where technical data overlaps high-end editorial typography. The system prioritizes "Tonal Depth" over structural rigidity, ensuring the UI feels like a seamless, breathing environment rather than a collection of boxes.

---

## 2. Colors & Surface Philosophy

### Palette Implementation
- **Primary (Turquoise/Blue - #75D1FF):** Reserved for the "Action Path." Used for primary interactive elements, active states, and glowing ring shadows that signify focus.
- **Secondary (Orange - #C8811A):** Used as a surgical highlighter. This is for status badges, high-priority callouts, and specific "tool-tip" indicators that require immediate ocular attention. Matches the Edelleye wordmark amber.
- **Background (#000000):** The absolute base. No exceptions.

### The "No-Line" Rule
Traditional 1px solid borders are strictly prohibited for sectioning. They create visual clutter and feel "cheap." Instead:
- **Tonal Shifts:** Define sections by moving from `surface` (#131313) to `surface-container-low` (#1B1B1B).
- **Implicit Boundaries:** Use white space from our spacing scale (e.g., `spacing-16` or `spacing-20`) to let the eye define the grouping.

### Glass & Texture
- **Glassmorphism:** Floating panels (Modals, Popovers) must use semi-transparent surface colors with a `backdrop-blur` (20px-40px). This allows the pure black background to "bleed" through, creating an integrated, high-end feel.
- **Signature Gradients:** For primary CTAs, use a subtle radial gradient transitioning from `primary` (#75D1FF) to `primary-container` (#3AB0E2). This adds "soul" and prevents the flatness common in budget frameworks.

---

## 3. Typography: The Editorial Edge

The tension between the headlines and the body text is what creates the "Cinematic" feel.

- **Headlines (Plus Jakarta Sans / GT Walsheim substitute):** Must use **negative letter-spacing** (-0.02em to -0.05em). This creates a "tight," authoritative block of text that feels custom-fitted.
- **Body & Labels (Inter):** Utilize extensive **OpenType features** (tnum, ss01, case). Use `body-md` for standard reading and `label-sm` for technical metadata. Inter’s neutrality provides the "functional" contrast to the expressive headline face.

### Heading Hierarchy

No H1 tags are used on any page. H2 is the top-level display heading. All hero/display headings use `text-4xl md:text-5xl` (36px / 48px) for legibility and controlled visual impact.

| Level | HTML | Font Family | Size (Tailwind) | Character Spacing |
| :--- | :--- | :--- | :--- | :--- |
| **Display** | H2 | Plus Jakarta Sans | `text-4xl md:text-5xl` | -0.02em |
| **Section** | H2 | Plus Jakarta Sans | `text-3xl` | -0.02em |
| **Sub-section** | H3 | Plus Jakarta Sans | `text-xl` | 0 |
| **Body-MD** | p | Inter | `text-base` (0.875rem) | 0.01em |
| **Label-SM** | span | Inter | `text-[10px]–text-[12px]` | 0.05em (Uppercase) |

---

## 4. Elevation & Depth: Tonal Layering

We do not use drop shadows to indicate "height"; we use **Light and Layering**.

- **The Layering Principle:** Stack surfaces logically. Place a `surface-container-highest` card on top of a `surface-container-low` section. The delta in grey values creates a natural "lift."
- **Ambient Glows:** When an element must "float" (like a primary action button), use a `primary` tinted shadow with a massive blur (30px+) and ultra-low opacity (6%). It should look like an ambient light source is sitting behind the element.
- **The Ghost Border:** If a divider is mandatory for accessibility, use `outline-variant` (#3E484F) at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Buttons (The Pill Style)
- **Primary:** Pill-shaped (`rounded-full`). Background: `primary` gradient. Text: `on-primary` (Bold).
- **Secondary:** Pill-shaped. Background: Transparent. Border: `Ghost Border` (15% opacity). Text: `primary`.
- **States:** On hover, the primary button should emit a 12px `primary` glow.

### Cards & Containers
- **Zero Borders:** Separate cards using background color shifts.
- **Nesting:** An inner card should always be one tier higher in the `surface-container` scale than its parent container.

### Interactive Elements
- **Chips:** Small, pill-shaped. Use `secondary` (#C8811A) for selection highlights to provide a "tool-obsessed" contrast against the blue primary path.
- **Inputs:** Darker than the surface. `surface-container-lowest` for the field background. On focus, the field receives a 1px `primary` glow ring (not a solid border).
- **Tooltips:** Use `surface-bright` with `on-surface` text. They should appear with a slight "zoom-in" motion to reinforce the cinematic feel.

---

## 6. Do’s and Don’ts

### Do:
- **Use Intentional Asymmetry:** Align technical data to the right while headlines sit on the left, creating a "dashboard" look.
- **Embrace Pure Black:** Let the `#000000` background act as negative space; it is the most expensive-looking color we have.
- **Layer with Logic:** Ensure the `surface-container` values always get lighter as they "stack" closer to the user.

### Don’t:
- **Don't use 100% Opaque Borders:** This immediately breaks the "high-end" illusion and reverts to a generic UI look.
- **Don't use standard Grey shadows:** Always tint your shadows with the Primary or Secondary brand colors to maintain tonal depth.
- **Don't use standard Letter-spacing for Headlines:** If GT Walsheim isn't tight, it isn't "Edelleye."