# Design System Strategy: Structural Precision & The Human Hand

## 1. Overview & Creative North Star: "The Technical Atelier"
This design system is built to bridge the gap between the rigid, uncompromising world of steel engineering and the tactile, bespoke nature of architectural craft. We are moving away from the "industrial warehouse" aesthetic and toward a "high-end studio" feel. 

**The Creative North Star: The Technical Atelier.**
The UI should feel like a blueprint laid out on a clean oak desk. It is precise, technical, and grounded, yet remains airy and inviting. We achieve this by breaking the traditional rigid grid through **intentional asymmetry**—letting elements breathe with varied margins—and using **overlapping layers** that mimic architectural drawings stacked on top of one another. We avoid the "template" look by treating the screen as a canvas where negative space is as structural as the content itself.

---

## 2. Colors: Tonal Integrity
The palette centers on the tension between the cold strength of steel (`primary: #192830`) and the warmth of a craftsman’s workshop (`secondary: #94492d`).

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to define sections. Traditional dividers are forbidden. Boundaries must be established through background shifts. For example, a project description in `surface` should transition into a technical specification area using `surface-container-low` (#f4f4f2). This creates a sophisticated, "blocked" editorial feel rather than a fragmented, "webby" one.

### Surface Hierarchy & Nesting
Treat the interface as a physical stack of materials.
*   **Base Layer:** `surface` (#f9f9f7) – The expansive "drawing board."
*   **Sub-Sections:** `surface-container-low` (#f4f4f2) – Used for grouping related technical data.
*   **Interactive Cards:** `surface-container-lowest` (#ffffff) – Use this to make cards feel like they are floating slightly above the page.

### The "Glass & Gradient" Rule
To add soul to the technicality, use **Glassmorphism** for navigation bars or floating action menus. Apply `surface` at 80% opacity with a `20px` backdrop-blur. For primary CTAs, use a subtle linear gradient from `primary` (#192830) to `primary-container` (#2f3e46) at a 135-degree angle to give the "steel" a metallic, three-dimensional depth.

---

## 3. Typography: The Editorial Blueprint
We use a dual-font system to balance technical precision with modern accessibility.

*   **Display & Headlines (Manrope):** Chosen for its geometric yet modern construction. Use `display-lg` and `headline-lg` in **Bold (700)** or **ExtraBold (800)** weights. These should be treated as architectural anchors on the page—don't be afraid of extreme scale.
*   **Body & Labels (Inter):** The workhorse. Inter provides maximum legibility for technical specifications and long-form project narratives.
*   **Hierarchy as Identity:** Use `label-md` in `secondary` (#94492d) all-caps for categories (e.g., "RESIDENTIAL," "INDUSTRIAL") to act as "stamps" on the design, mimicking architectural plan notations.

---

## 4. Elevation & Depth: Tonal Layering
In this system, depth is a function of light and material, not artificial shadows.

*   **The Layering Principle:** Avoid elevation shadows where possible. Instead, place a `surface-container-highest` element against a `surface` background to create a "recessed" or "pressed" look.
*   **Ambient Shadows:** For floating elements (like a "Contact Studio" button), use a diffused shadow: `0px 24px 48px rgba(25, 40, 48, 0.06)`. Notice the shadow is tinted with our `primary` charcoal, not pure black.
*   **The "Ghost Border" Fallback:** If a boundary is required for accessibility, use the `outline-variant` (#c3c7ca) at **15% opacity**. It should be felt, not seen.
*   **Glassmorphism:** Use for overlays. A `surface-container-low` fill at 70% opacity with a heavy backdrop blur creates a "frosted vellum" effect, allowing the structural elements beneath to peek through.

---

## 5. Components: Precision Elements

### Buttons
*   **Primary:** `primary` background with `on-primary` text. `0.25rem` (sm) corner radius for a sharp, architectural edge.
*   **Secondary:** `surface` background with a `ghost border` (outline-variant @ 20%).
*   **Tertiary:** `tertiary` (#34230b) text with no background, using a `secondary` (#94492d) 2px underline that expands on hover.

### Cards & Project Previews
*   **Rule:** No dividers. Use `spacing-8` (2.75rem) to separate content.
*   **Style:** Use `surface-container-lowest` (#ffffff) with a `surface-variant` (#e2e3e1) 1px "Ghost Border." Image headers should have a slight `0.25rem` radius to match the structural theme.

### Technical Input Fields
*   **Style:** Flat backgrounds using `surface-container-high`. Labels should use `label-sm` in `primary` for a "blueprint annotation" look. Focus states should transition the background to `surface-container-lowest` with a `secondary` (terracotta) bottom-border only.

### Structural Chips
*   Used for material types (e.g., "Grade A36 Steel"). Use `secondary-fixed` (#ffdbcf) background with `on-secondary-fixed-variant` (#763318) text. This provides the "human touch" warmth against the charcoal UI.

---

## 6. Do's and Don'ts

### Do:
*   **Do use asymmetrical white space.** Allow images to bleed off the grid or sit offset from the text to create an editorial, high-end feel.
*   **Do use "Primary Fixed Dim" (#b9c9d3)** for background icons or watermarks. It evokes the look of faded blueprints.
*   **Do prioritize "Manrope Bold"** for numbers. In a structural portfolio, the data (sq ft, tonnage, dates) is as beautiful as the photos.

### Don't:
*   **Don't use 100% black.** It is too harsh. Always use `primary` (#192830) for text to maintain the "charcoal" sophistication.
*   **Don't use large corner radiuses.** Avoid `xl` or `full` roundedness. Stick to `sm` (0.25rem) or `none` (0px) to reinforce the "steel" brand.
*   **Don't use standard dividers.** If you feel the need to separate sections, use a background color shift from `surface` to `surface-container-low`.