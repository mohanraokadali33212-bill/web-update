# Design System Strategy: The Elevated Heritage

## 1. Overview & Creative North Star
**Creative North Star: "The Modern Heirloom"**

This design system rejects the "fast-casual" aesthetic in favor of a digital experience that feels as curated as a Michelin-starred meal. We are blending the raw, earth-bound soul of South India—the warmth of terracotta, the tactile grit of charcoal, and the glow of brass—with the clinical precision of Swiss modernism. 

To break the "template" look, we move away from rigid, centered grids. Instead, we use **Intentional Asymmetry**. Large serif display type should feel "editorial," often overlapping onto image containers or floating within expansive whitespace. The Telugu script accent ('తృప్తిగా') acts not as a label, but as a high-fashion watermark—rotated 90 degrees or set at 5% opacity—creating a layered, atmospheric depth that suggests history without cluttering the interface.

---

## 2. Colors: Tonal Earth & Metallic Light
We don't use color to decorate; we use it to evoke temperature and taste.

*   **Primary (#7c5800 / #ffb800):** This is our "Liquid Brass." Use it sparingly for high-intent actions.
*   **The Neutrals:** Our `surface` (#fcf9f3) is a crisp off-white that prevents the "blue-light" eye strain of pure white, feeling more like handmade paper.
*   **Tertiary (#944925):** The "Burnt Sienna" role. Use this for moments of warmth, like active states in navigation or price points.

**The "No-Line" Rule:** 
Standard 1px borders are strictly prohibited for sectioning. Boundaries must be defined solely through background color shifts. A `surface-container-low` section sitting on a `surface` background provides enough contrast to signal a transition without the "boxed-in" feel of a generic template.

**Surface Hierarchy & Nesting:** 
Treat the UI as physical layers. An "Order" card should not have a border; it should be a `surface-container-lowest` (#ffffff) card sitting on a `surface-container` (#f0eee8) background. This "paper-on-stone" stacking creates sophisticated depth.

**The "Glass & Gradient" Rule:** 
For floating elements like Navigation Bars or Mobile Menus, use Glassmorphism. Apply `surface-bright` at 80% opacity with a `20px` backdrop-blur. For CTAs, use a subtle radial gradient from `primary` (#7c5800) to `primary_container` (#ffb800) to mimic the way light hits polished brass.

---

## 3. Typography: The Swiss-Serif Dialogue
Our typography is a conversation between the old world (Serif) and the new (Sans).

*   **Display & Headline (Noto Serif):** These are our "hero" voices. Use `display-lg` (3.5rem) for menu categories and brand statements. The high contrast of Noto Serif reflects the premium nature of the brand.
*   **Title & Body (Inter):** High-end Swiss typography. Inter provides the functional clarity required for ingredient lists and pricing. 
*   **Telugu Watermarks:** Use the Telugu script ('తృప్తిగా') as a decorative element in `display-sm` sizing, set to `outline-variant` with 10% opacity, placed behind primary text to add a sense of place.

---

## 4. Elevation & Depth
We eschew traditional drop shadows for **Tonal Layering**.

*   **The Layering Principle:** Depth is achieved by stacking. Place a `surface-container-lowest` element on top of a `surface-container-high` section. This creates a soft, natural "lift" that feels architectural.
*   **Ambient Shadows:** If an element must float (e.g., a "Book Table" FAB), use an extra-diffused shadow: `box-shadow: 0 20px 40px rgba(49, 49, 45, 0.06)`. The shadow is tinted with the `on-surface` color, never pure black, to mimic natural ambient light.
*   **The "Ghost Border" Fallback:** If a divider is required for accessibility in complex forms, use the `outline-variant` token at **15% opacity**. Never use 100% opaque lines.

---

## 5. Components

### Buttons
*   **Primary:** High-gloss brass finish. Use `primary` background with `on_primary` text. Shape: `md` (0.375rem) for a subtle "bespoke" feel—not too round, not too sharp.
*   **Secondary:** Glassmorphic. `surface_variant` at 40% opacity with a blur. 
*   **Tertiary:** Text-only in `tertiary` (#944925), using 1.5pt letter spacing for an editorial look.

### Cards & Menu Items
*   **The Rule:** No dividers between menu items. 
*   **Style:** Use `spacing-6` (2rem) of vertical whitespace to separate items. For featured dishes, use a `surface-container-low` background with an asymmetrical image crop (e.g., top-left corner radius at `xl`, others at `none`).

### Input Fields
*   **Minimalist Slate:** No containers. Use a bottom-only "Ghost Border" (15% opacity `outline`). Labels should be `label-md` in `secondary` color, floating 8px above the input.

### Signature Component: "The Texture Overlay"
For Hero sections, overlay a subtle "Woven Palm" texture (SVG pattern) at 3% opacity over the `surface` color to provide a tactile, rustic feel that breaks the digital flatness.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use asymmetrical margins. If the left margin is `16` (5.5rem), the right can be `8` (2.75rem) to create a dynamic, editorial flow.
*   **Do** allow the Telugu script to be cut off by the edge of the screen—it’s a texture, not a headline.
*   **Do** use `surface-container-highest` for "Active" states in navigation.

### Don't:
*   **Don't** use standard "Shadow-2dp" styles. They look cheap. Use tonal shifts or ambient 4% opacity blurs.
*   **Don't** use pure black (#000). Use `Charcoal Slate` (#2D2D2D) for all "dark" needs to maintain the rustic warmth.
*   **Don't** use generic South Indian iconography (like coconut trees). Lean into textures—terracotta, brass, and weave patterns—to signal "Premium."