# Design System Strategy: The Digital Editorial CV

## 1. Overview & Creative North Star
**Creative North Star: "The Luminescent Archivist"**

This design system moves beyond the concept of a standard website to create a high-end, editorial-grade digital artifact. For a 2026 tech aesthetic, we are departing from the "flat grid" of the early 2020s in favor of **Tonal Depth and Asymmetric Sophistication**. 

The goal is to present career data not as a table, but as a narrative. We achieve this through a "vibrant-on-void" approach—using the signature Electric Cyan hair color from the reference image as a bioluminescent light source against a deep, layered sapphire-black abyss. The layout rejects standard templates, utilizing wide margins, overlapping typographic elements, and a "glass-sheet" hierarchy that suggests a physical presence in a digital space.

---

## 2. Colors & Surface Architecture

The palette is anchored by the vibrant `primary` (#3bbffa), a direct extraction of the character’s hair, designed to pop against the `background` (#00101d).

### The "No-Line" Rule
Designers are strictly prohibited from using 1px solid borders for sectioning or containment. Traditional lines create visual "noise" that cheapens the experience. Instead, boundaries must be defined through:
- **Tonal Shifts:** Placing a `surface-container-low` (#001524) module atop the base `surface` (#00101d).
- **Negative Space:** Using a strict 64px/96px vertical spacing scale to separate CV sections (Experience, Skills, Education).

### Surface Hierarchy & Nesting
Think of the UI as layers of fine, dark paper stacked in a void. 
- **Base Layer:** `surface` (#00101d).
- **Secondary Modules:** `surface-container` (#001b2e).
- **Interactive/Hover States:** `surface-container-high` (#002237).
Use these shifts to create "nested" importance. A portfolio project card should be one tier higher than the section it sits within.

### The Glass & Gradient Rule
To achieve the "2026 Tech" look, use **Glassmorphism** for floating UI (navigation bars, tooltips). 
- **Effect:** Apply `surface_variant` (#002840) at 60% opacity with a 24px Backdrop Blur.
- **Signature Gradients:** For Hero headers and Primary CTAs, use a "Sleek Flow" gradient: `linear-gradient(135deg, #3bbffa 0%, #22b1ec 100%)`. This mimics the natural highlight and shadow found in the reference image's hair.

---

## 3. Typography
The system utilizes a dual-font strategy to balance technological precision with editorial authority.

*   **Display & Headlines (Space Grotesk):** A tech-forward, high-character sans-serif. Use `display-lg` (3.5rem) for name/title to establish an immediate, bold identity. The wide apertures of Space Grotesk feel futuristic and intentional.
*   **Body & Titles (Manrope):** A highly legible, professional sans-serif. Manrope’s geometric balance ensures that dense CV information (job descriptions, bullet points) remains readable without losing the modern edge.
*   **Utility (Inter):** Used for `label-md` and `label-sm` (metadata, dates, tags). Inter’s neutrality ensures it doesn't compete with the primary narrative.

**Hierarchy Strategy:** Use `primary` (#3bbffa) for key keywords within body text to guide the recruiter's eye toward specific achievements or technologies.

---

## 4. Elevation & Depth

### The Layering Principle
Avoid the "Shadow Drop" of 2015. Instead, use **Tonal Layering**. If a card needs to feel prominent, do not add a shadow; shift its background from `surface-container` to `surface-bright` (#002f4a).

### Ambient Shadows
For floating elements (Modals, Hovered Cards):
- **Blur:** 40px - 60px.
- **Opacity:** 6% - 10%.
- **Color:** Use `on-surface` (#d1e8ff) as the shadow tint. This creates a "glow" rather than a "stain," simulating light bouncing off the dark surface.

### The "Ghost Border" Fallback
If a visual separator is mandatory for accessibility:
- Use `outline-variant` (#264b67) at **15% opacity**.
- It should be barely perceptible, serving as a subtle "catch-light" on the edge of a container.

---

## 5. Components

### Buttons
- **Primary:** Gradient fill (`primary` to `primary-container`), no border, `md` (0.375rem) roundedness. Text color: `on-primary` (#00374d).
- **Tertiary:** No fill. Text color `primary`. On hover, a subtle `surface-variant` background bleed.

### Portfolio Cards
- **Construction:** Use `surface-container-low`.
- **Constraint:** **No Dividers.** Separate the "Project Title" from "Description" using a 16px vertical gap.
- **Interactive State:** On hover, the card shifts to `surface-container-highest` and the `primary` light-glow (Ambient Shadow) intensifies.

### CV Timeline / Lists
- Instead of a vertical line for timelines, use a series of `primary` colored dots.
- Leading elements (Company Logos) should be housed in a `surface-variant` circle with 20% opacity to maintain the dark-mode aesthetic.

### Chips (Skills/Tags)
- Use `secondary-container` (#3c475a) with `on-secondary-container` (#c5d1e8) text.
- Shape: `full` (pill-shaped) to contrast against the structured, rectangular layout of the CV.

---

## 6. Do's and Don'ts

### Do
- **Do** embrace extreme white space. A CV is more impressive when it isn't "crowded."
- **Do** use `primary` sparingly. It is a laser, not a paint bucket. Use it for highlights, icons, and CTA states.
- **Do** use the `xl` (0.75rem) roundedness for large layout containers to soften the "tech" edge.

### Don't
- **Don't use 100% Black (#000000).** Our base is `surface` (#00101d). Pure black kills the depth and prevents the "Glass" effect from working.
- **Don't use Divider Lines.** If you feel you need a line, you actually need more padding.
- **Don't use standard "Blue."** Only use the specific Vibrant Blue (`primary`) and its derived tones. Any other blue will break the signature visual identity.