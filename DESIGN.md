# Design System: Editorial Minimalism for the Modern Engineer

## 1. Overview & Creative North Star: "The Digital Architect"
This design system moves beyond the "standard developer portfolio" by embracing an editorial, high-end aesthetic. The Creative North Star is **The Digital Architect**: a philosophy where code is treated as craft, and the UI serves as a gallery. 

We reject the rigid, "boxed-in" layout of traditional templates. Instead, we utilize **intentional asymmetry**, **tonal layering**, and **expansive whitespace** to create a sense of effortless sophistication. The goal is to present technical expertise through a lens of premium, minimalist design—where what is left out is just as important as what is included.

---

## 2. Colors: Tonal Depth & The "No-Line" Rule
The palette is built on a foundation of "Midnight Slate" (`#0b1326`) and "Electric Emerald" (`#4edea3`). We do not use color merely for decoration; we use it to define space and focus.

### The "No-Line" Rule
**Explicit Instruction:** Prohibit the use of 1px solid borders for sectioning or containment. Boundaries must be defined through:
1.  **Background Color Shifts:** Placing a `surface-container-low` (`#131b2e`) section against the primary `surface` (`#0b1326`).
2.  **Tonal Transitions:** Using the `surface-container` tiers to create natural breaks in content flow.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. Hierarchy is achieved by "stacking" tones:
*   **Base Layer:** `surface` (#0b1326) – The canvas.
*   **Subtle Recess:** `surface-container-lowest` (#060e20) – Use for inactive background areas or footer foundations.
*   **Primary Content Area:** `surface-container` (#171f33) – The main body of project descriptions or code blocks.
*   **Elevated Components:** `surface-container-highest` (#2d3449) – Reserved for active states or floating navigation.

### The "Glass & Gradient" Rule
To add "soul" to the minimalist aesthetic:
*   **Glassmorphism:** For top navigation bars and floating action menus, use `surface-variant` (`#2d3449`) at 60% opacity with a `24px` backdrop-blur. 
*   **Signature Textures:** Use a subtle linear gradient from `tertiary` (`#4edea3`) to `on-tertiary-container` (`#009365`) for primary CTAs or high-impact data visualizations.

---

## 3. Typography: Editorial Authority
We pair the geometric precision of **Manrope** for displays with the hyper-readability of **Inter** for functional text.

*   **Display & Headline (Manrope):** Large, bold, and authoritative. `display-lg` (3.5rem) should be used for hero statements with tight letter-spacing (-0.02em) to create a "block" of text that feels like a graphic element.
*   **Title & Body (Inter):** Clean and functional. Use `body-lg` (1rem) with an increased line-height (1.6) for project narratives to ensure long-form readability.
*   **Labels (Inter):** Use `label-md` (0.75rem) in uppercase with generous letter-spacing (0.1em) for category tags or "Technical Specs" headers. This conveys a "blueprint" aesthetic.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are forbidden unless specified. Depth is a product of light and material simulation.

*   **The Layering Principle:** Instead of a shadow, place a `surface-container-low` card on a `surface` background. The slight shift in hex value creates a "soft lift" that feels integrated into the architecture.
*   **Ambient Shadows:** For floating elements (like a "Back to Top" button), use a diffuse shadow: `offset: 0 12px, blur: 40px, color: rgba(6, 14, 32, 0.4)`. The shadow must feel like an ambient occlusion, not a dark smudge.
*   **The "Ghost Border" Fallback:** If accessibility requires a container definition (e.g., input fields), use `outline-variant` (`#45464d`) at **15% opacity**. It should be felt, not seen.

---

## 5. Components: The Minimalist Toolkit

### Buttons
*   **Primary:** Fill: `tertiary` (`#4edea3`); Text: `on-tertiary` (`#003824`). Roundedness: `md` (`0.375rem`). No border.
*   **Secondary:** Fill: `transparent`; Text: `primary` (`#bec6e0`); Border: `Ghost Border` (15% opacity `outline-variant`).
*   **Interaction:** On hover, primary buttons should scale 2% (`scale-102`) rather than just changing color.

### Cards & Projects
*   **Constraint:** Never use divider lines.
*   **Layout:** Use `surface-container` (`#171f33`) as the card base. Separate the image from the text using a `1.5rem` (xl) internal gutter. Use `roundedness-lg` (`0.5rem`) for project thumbnails.

### Input Fields
*   **Visual Style:** Only a bottom border (1px) using `outline-variant` at 30% opacity. Upon focus, the border transitions to `tertiary` (`#4edea3`) and the background shifts to `surface-container-high`.

### Code Blocks
*   **Style:** Use `surface-container-lowest` (`#060e20`) for the background. This "sinks" the code into the page, signaling it as a different functional layer. Use `tertiary` for syntax highlighting of key variables.

---

## 6. Do's and Don'ts

### Do:
*   **Embrace Asymmetry:** Align text to the left but allow images to bleed off-center to create visual interest.
*   **Use Generous Whitespace:** If you think there is enough margin, double it. Content needs room to breathe to feel premium.
*   **Focus on Micro-Interactions:** Use subtle spring physics for hover states to make the "Minimalist" environment feel alive.

### Don't:
*   **Don't use 100% Black:** Always use `surface` (`#0b1326`) for the darkest areas to maintain tonal depth.
*   **Don't use Decorative Outlines:** Never use the "text-outline" or "stroke" effect on typography; it breaks the clean editorial feel.
*   **Don't use Grid Borders:** Avoid "table-like" layouts with visible lines. Use spacing (`gap-8` or `gap-12`) to define columns.
*   **Don't Over-Saturate:** Keep the `tertiary` accent (`#4edea3`) to less than 10% of the total screen real estate. It is a scalpel, not a sledgehammer.