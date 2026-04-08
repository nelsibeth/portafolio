# Agent Instructions: The Luminescent Archivist Portfolio

You are an AI developer assisting in the expansion of this Astro-based portfolio. This project follows a specific 2026 tech aesthetic defined as **"The Luminescent Archivist"**.

## Core Creative North Star
- **Aesthetic:** Tonal Depth and Asymmetric Sophistication.
- **Colors:** Deep layered sapphire-black abyss (`#00101d`) with Electric Cyan (`#3bbffa`) as a bioluminescent light source.
- **Vibe:** Editorial-grade digital artifact. High-end, premium, and narrative-driven.
- **Language:** The primary language for all user-facing content is **Spanish**.

## Style Guidelines for Future Development
When adding new components or pages, strictly adhere to these rules from `DESIGN.md`:

### 0. Fixes and Robustness
- **Icons:** ALWAYS add `translate="no"` to any `material-symbols-outlined` span to prevent browser auto-translation from breaking the icon ligature.

### 1. The "No-Line" Rule
- **CRITICAL:** Do NOT use 1px solid borders for sectioning. 
- Use **Tonal Shifts** (`surface-container-low` atop `surface`) or **Negative Space** (64px/96px vertical gaps) to separate sections.
- For mandatory accessibility separators, use `outline-variant` (#264b67) at **15% opacity**.

### 2. Glassmorphism & Gradients
- Use **Glassmorphism** for floating UI (navigation, modals): `bg-surface-variant/60` with `backdrop-blur-xl`.
- Use the **"Sleek Flow" Gradient** for Hero headers and Primary CTAs: `linear-gradient(135deg, #3bbffa 0%, #22b1ec 100%)`.
- **Note:** In CSS, use `background-image` for these gradients to avoid overriding Tailwind's `bg-clip` utilities.

### 3. Typography
- **Display/Headlines:** `Space Grotesk` (Bold/Tracking-tighter).
- **Body/Titles:** `Manrope`.
- **Metadata/Utility:** `Inter`.

### 4. Component Patterns
- **Buttons:** Rounded-xl (`0.5rem`). Primary buttons use the gradient.
- **Cards:** Use `surface-container-low`. No dividers. 16px vertical gap between title and description.
- **Shadows:** Use Ambient Shadows (40px-60px blur, 6-10% opacity) using `on-surface` tint to create a "glow" effect rather than a dark stain.

## Project Structure
- `src/layouts/Layout.astro`: Base layout with font imports.
- `src/styles/global.css`: Contains custom design system tokens and utility classes.
- `src/components/`: Reusable fragments (TopAppBar, SideNavBar, etc.).
- `tailwind.config.mjs`: Centralized color and theme tokens mapping to the design strategy.

## Reference
Always refer back to [DESIGN.md](file:///home/nelsibeth/source/portafolio/DESIGN.md) for the full creative strategy before proposing visual changes.
