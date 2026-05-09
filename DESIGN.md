# Design System Strategy: High-End Editorial

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Intelligent Observer."** 

Unlike standard SaaS platforms that feel mechanical and grid-locked, this system treats digital interfaces as high-end editorial publications. We prioritize whitespace as a functional element, not a void. By utilizing intentional asymmetry, sophisticated serif-to-sans-serif transitions, and tonal layering, we move away from "software" and toward "intelligence." The goal is to make every screen feel like a curated page from a prestige market report—authoritative, human-centric, and deeply credible.

## 2. Colors & Surface Philosophy
The palette is grounded in the warmth of Taupe and the brilliance of Gold, punctuated by an analytical Teal. We move beyond the flat web by treating color as a physical material.

### The "No-Line" Rule
To maintain a premium editorial feel, **designers are prohibited from using 1px solid borders for sectioning.** Structural boundaries must be defined solely through:
*   **Background Color Shifts:** Moving from `surface` to `surface-container-low`.
*   **Negative Space:** Using the spacing scale to create distinct visual groupings.
*   **Tonal Transitions:** Subtle shifts in hue to denote change in context.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers—like stacked sheets of fine, heavy-weight paper.
*   **Base:** `surface` (#fff8f4) is your canvas.
*   **Containers:** Use `surface-container` tiers (Lowest to Highest) to create "nested" depth. For example, a data visualization should sit on a `surface-container-high` card, which itself sits on a `surface-container-low` section. This creates a soft, natural lift without the "heaviness" of traditional shadows.

### The "Glass & Gradient" Rule
To avoid a "flat" or "stock" aesthetic:
*   **Glassmorphism:** For floating elements like navigation bars or hover-state popovers, use `surface` colors at 80% opacity with a `20px` backdrop-blur. This allows the sophisticated Taupe tones to bleed through, softening the interface.
*   **Signature Textures:** For primary CTAs or Hero sections, utilize a subtle linear gradient (from `primary` #00687a to `primary-container` #69cce5) at a 135-degree angle. This adds a "silk-screen" professional polish.

## 3. Typography
The typography is the voice of the brand: authoritative yet accessible.

*   **Display & Headlines (Noto Serif):** Used for the "Editorial Voice." Large scales (Display-LG) should be used with generous leading and occasional intentional asymmetry (e.g., left-aligned with a wide margin) to mimic prestige print layouts.
*   **Body & Titles (Manrope):** The "Analytical Voice." Manrope provides a clean, modern contrast to the serif headings. Title-LG should be used for data-heavy labels to maintain readability at a glance.
*   **Visual Hierarchy:** The massive scale jump between `display-lg` (3.5rem) and `body-lg` (1rem) is intentional. It forces a clear narrative path, guiding the user from high-level insight to granular detail.

## 4. Elevation & Depth
In this design system, depth is a result of **Tonal Layering** rather than structural lines.

### The Layering Principle
Depth is achieved by "stacking" the surface-container tiers. Place a `surface-container-lowest` card on a `surface-container-low` section to create a soft, natural lift.

### Ambient Shadows
When an element must float (e.g., a modal or a primary dropdown), use **Ambient Shadows**:
*   **Blur:** 30px–60px.
*   **Opacity:** 4%–8%.
*   **Color:** Use a tinted version of the `on-surface` color (#2a1701) rather than pure black. This mimics natural light passing through a high-end lens.

### The "Ghost Border" Fallback
If a border is absolutely necessary for accessibility (e.g., in high-density data tables), it must be a **Ghost Border**:
*   Use `outline-variant` (#d0c5b0) at **20% opacity**. 
*   **Never** use 100% opaque, high-contrast borders.

## 5. Components

### Buttons
*   **Primary (Action):** Filled with `primary` (#00687a), text in `on-primary`. Use the `md` (0.375rem) roundedness for a sophisticated, slightly sharp look.
*   **Secondary (Gold):** Use `secondary-container` (#fdd35d) with `on-secondary-container`. This is for high-priority highlights that aren't the main "Action."
*   **Tertiary:** Text-only using `primary` color, with a 2px underline appearing only on hover.

### Cards & Lists
*   **Rule:** Forbid the use of divider lines. 
*   **Execution:** Separate content using `8px` or `16px` of vertical white space or by alternating background colors between `surface-container-low` and `surface-container-lowest`.

### Input Fields
*   **Style:** Minimalist. No enclosing box. Use a `surface-variant` (#ffddb9) bottom-only border (2px).
*   **States:** On focus, the bottom border transitions to `primary` Teal. Helper text should always use `label-md` in `on-surface-variant`.

### Chips
*   **Style:** Use `surface-container-high` for the background with `0.25rem` (DEFAULT) roundedness. 
*   **Selection:** When selected, chips transition to `secondary-fixed` (Gold) to highlight the active filter without the "heavy" look of a button.

### Market Intelligence Components (Unique to Limina)
*   **Insight Callouts:** A `tertiary-container` (#dcb892) box with no border, using `Noto Serif` for the quote/insight.
*   **Data Highlights:** Large `display-sm` numbers in `primary` Teal, paired with `label-sm` descriptors in `on-surface-variant`.

## 6. Do's and Don'ts

### Do
*   **Do** use asymmetrical layouts. A column of text should often have a wider margin on one side than the other to feel "editorial."
*   **Do** use `notoSerif` for quotes or key market takeaways to inject humanity.
*   **Do** leverage `surface-bright` for areas meant to draw the eye without using high-saturation colors.

### Don't
*   **Don't** use 1px dividers or borders to separate sections.
*   **Don't** use "Drop Shadows" from a standard UI kit; only use the diffused Ambient Shadows described above.
*   **Don't** use bright, "startup-style" gradients. If a gradient is used, it must be subtle and tonal.
*   **Don't** crowd the interface. If a screen feels full, increase the spacing scale rather than shrinking the elements. This system requires "breathing room" to feel premium.
