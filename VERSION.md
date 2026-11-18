# MINDS4MOTION Website — v1.3.2

**Release:** 18 November 2026  
**Status:** motion/touch refinement — pending merge and GitHub Pages publish  
**Repository:** `rwmt95ny9r-gif/minds4motion-website`

## v1.3.2 — MOTION / STATE ambient interaction

Second interaction refinement based on direct iPhone testing.

### Changed

- Reduced autonomous particle movement to a near-static ambient drift.
- Lowered initial particle velocity dramatically.
- Added stronger damping and a much lower velocity cap.
- Increased touch influence so dragged movement shapes the field more clearly than autonomous motion.
- Increased the interaction radius around the finger.
- Moved touch handling to the complete MOTION / STATE shell.
- Added `touch-action: none` and `overscroll-behavior: contain` to prevent page scrolling while interacting inside the field.
- Added explicit non-passive `touchstart` / `touchmove` handlers with `preventDefault()` for iPhone Safari.
- Updated the hint to: **Drag to shape it · scroll outside**.

---

## v1.3.1 — MOTION / STATE interaction refinement

Refines the first MOTION / STATE release after iPhone screen-capture review.

### Changed

- Significantly reduced autonomous particle speed for a calmer visual field.
- Reduced particle count slightly to create more negative space.
- Strengthened pointer/touch attraction so movement is clearly influenced by the visitor.
- Added explicit touchstart/touchmove handling for iPhone interaction.
- Added a subtle red touch point, expanding ring and temporary connections to nearby particles.
- Added velocity clamping and stronger damping to prevent the field from becoming hectic.
- Kept THINK / FEEL / CREATE distinct, but all three now remain intentionally calm.

---

## v1.3.0 — MOTION / STATE

A new interactive creative layer turns the MINDS4MOTION idea into a small experience rather than another static content block.

### New

- Added **MOTION / STATE** between “Why it exists” and “Four worlds”.
- Added the prompt **“What moves you right now?”**
- Three selectable states: **THINK · FEEL · CREATE**.
- Each state has its own motion character:
  - THINK — structured, restrained, reflective.
  - FEEL — slower, softer, more organic.
  - CREATE — more energetic, connected and red.
- Mouse and touch position subtly influence the moving field.
- Multiple rotating thought fragments make repeat visits feel slightly different.
- Added the line **MINDS → MOTION** as the conceptual signature of the experience.
- Added a **Motion** anchor to the desktop navigation.

### Selected fragments

**THINK**
- Not every thought needs a conclusion.
- Questions can be places too.
- 1 + 1 ≥ 2.
- Stay curious long enough for the obvious to change.
- A thought can move before it becomes an answer.

**FEEL**
- Some things do not need to be understood. Only felt.
- Stay with it long enough to really notice it.
- Not everything needs an answer.
- Home is a feeling.
- Let the feeling exist before you name it.

**CREATE**
- Make the invisible visible.
- Create without needing to be an artist.
- #justcreative.
- Follow the line and see where it goes.
- Permission is sometimes the first creative act.

### Technical principles

- Vanilla HTML, CSS and JavaScript only.
- Canvas-based motion; no external animation library.
- Touch and pointer input supported.
- No tracking, cookies, backend or data transmission.
- Device pixel ratio capped for performance.
- Canvas rendering pauses when the experience is outside the viewport.
- `prefers-reduced-motion` is respected with a static fallback.
- Existing landing-page structure and MINDS4MOTION visual identity remain intact.

---

## Previous baseline

The public site continues to include:

- Responsive English-language landing page.
- MINDS4MOTION wordmark with red `4`.
- **Think. Feel. Create.**
- **#justcreative**
- Manifesto around thinking, feeling and creating.
- Four worlds: Fight · Family · Love · Joy.
- Custom white/red/black icon system.
- Creative-language section for visual work, music, series and reduction.
- Personal “Behind MINDS4MOTION” section.
- Original MINDS4MOTION logo and supplied portrait collage.
- Floating back-to-top control, sticky navigation, scroll progress and subtle reveal transitions.
- Instagram and obfuscated contact link.
- No external libraries, tracking, cookies, forms or backend.

## Design rules

- Primary palette: black, white and MINDS4MOTION red.
- Reduced, clean and intentional.
- No decorative kitsch or artificial “AI beauty”.
- High-contrast typography and generous negative space.
- Interaction must support meaning rather than become decoration.

## Deployment

- GitHub Pages via `.github/workflows/pages.yml`.
- Publish workflow runs manually via `workflow_dispatch`.
- Merge the v1.3.0 pull request into `main`, then run **Publish MINDS4MOTION Website**.

## Boundaries

The public site expresses the MINDS4MOTION creative identity. It deliberately excludes private Project Michael / M60 information that is not part of the public brand narrative, including personal family, legal, financial, health or employer-internal material.
