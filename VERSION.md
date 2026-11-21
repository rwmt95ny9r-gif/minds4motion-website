# MINDS4MOTION Website — v1.7.1

**Release:** 18 November 2026  
**Status:** Behind portrait palette alignment — ready for merge
**Repository:** `rwmt95ny9r-gif/minds4motion-website`

## v1.7.1 — Behind portrait palette alignment

Evidence-driven visual refinement based on the final live review.

- Replaced the previous warm-toned Behind portrait with the approved black / white / red treatment.
- Keeps Michael and the composition intact; the change is limited to visual tonality and brand integration.
- Added the portrait as a dedicated repository asset: `assets/michael-behind-minds4motion-bw-red.jpg`.
- Updated both EN and DE landing pages to use the same asset.
- No copy, navigation, interaction or Create Together logic changed.

This is a maintenance-level exception to the v1.7.0 feature cut, not a reopening of feature development.

---

## v1.7.0 — DE / EN language layer

Adds a complete German-language layer while keeping English as the default public version.

### Language model
- English remains the default at `/`.
- German lives under `/de/`.
- Minimal text-only switch: `EN / DE`.
- No flags.
- Brand language such as `MINDS4MOTION`, `#justcreative`, `Think. Feel. Create.` and `Create Together` is intentionally preserved where it functions as identity rather than prose.

### German pages
- `de/index.html`
- `de/create-together.html`
- `de/imprint.html`
- `de/privacy.html`

### English pages
- Added matching language switches to:
  - `index.html`
  - `create-together.html`
  - `imprint.html`
  - `privacy.html`

### Editorial approach
- German copy is adapted for tone and readability rather than translated mechanically word-for-word.
- Dynamic MOTION / STATE phrases are translated as well.
- Existing design, MOTION / STATE interaction, privacy model and Create Together demand-test logic remain unchanged.

### Cut line
v1.7.0 is intended as the final planned website feature release for now. Future changes should be maintenance, legal updates or evidence-driven changes based on real user response.

---

## v1.6.1 — Mobile Create Together entry

- Added a compact `Create Together ↗` link in the mobile header, positioned to the right of the MINDS4MOTION wordmark.
- Keeps the mini chapter navigation unchanged.
- Desktop navigation remains unchanged.

---

## v1.6.0 — Create Together

Adds a deliberately light commercial layer without turning MINDS4MOTION into a conventional service website.

### New

- Added `create-together.html` as a separate public page.
- Three offer directions:
  1. Creative Sparring
  2. Personal Story / Soundtrack
  3. Creative Concepting
- Each offer explains who it is for, how the work can unfold and a possible outcome.
- Added a low-friction email CTA: `Tell me what’s moving you`.
- Added deterministic mini chapter navigation for the new page.
- No public pricing, booking engine, analytics or third-party embeds.

### Main-site integration

- Added `Create Together ↗` to the desktop navigation.
- Added `Create Together` as the primary CTA in the closing section.
- Existing landing-page chapter navigation remains unchanged.

### Commercial reference

- Added `docs/create-together-commercial-model.md`.
- Contains positioning, detailed scope, pricing hypotheses, exclusions and a demand-test framework.
- The Pages workflow now excludes `docs/` from the deployed site artifact.
- Public site intentionally does not expose pricing.

---

## v1.5.0 — Personal soundtrack

Adds a dedicated music chapter that turns five personally meaningful tracks into a reduced emotional narrative.

### New

- Added a dedicated `Music` chapter between `Creative` and `Behind it`.
- Added `Music` to both the desktop navigation and the compact chapter navigation.
- Added five tracks with artist and emotional state:
  - Light Falls — EMBRZ
  - Wie Liebe geht — Lucien Voss
  - Disco Mare — Luca Vasta
  - Heartbeat — Hessian & Courtney Storm
  - Tranquil — Virtua & Akraa
- Light Falls receives a subtle personal annotation: `An anchor since 2023.`
- Added the closing line `My soundtrack. My way.`

### Changed

- Reworked the existing Music card inside `Creative language` into a teaser for the new chapter.
- Removed the previous artist-chip list to avoid duplication and generic playlist aesthetics.
- Kept the section deliberately typographic: no cover art, embeds, players or third-party tracking.

### Design intent

- Black / white / red only.
- Strong negative space.
- Five tracks presented as five emotional states rather than a playlist.
- Mobile layout collapses cleanly into an index / title / state rhythm.

---

## v1.4.7 — Imprint navigation active-state fix

Corrects the active chapter highlighting on the Imprint page.

### Changed

- Replaced the Imprint IntersectionObserver-based chapter detection with deterministic scroll-position tracking.
- The active navigation item now follows the section whose top has passed the fixed navigation stack.
- Clicking a chapter immediately activates the selected item.
- The final chapter is forced active at the bottom of the page.
- Main page and Privacy Policy navigation remain unchanged.

---

## v1.4.6 — GitHub Pages two-job deployment

Refactors the deployment workflow to follow GitHub's recommended Pages pattern.

### Changed

- Split the previous single deployment job into separate `build` and `deploy` jobs.
- The `build` job checks out the site, configures Pages and uploads the Pages artifact.
- The `deploy` job starts only after `build` completes successfully via `needs: build`.
- Restores the standard `github-pages` artifact name.
- Avoids the intermittent artifact-visibility race observed when upload and deploy run back-to-back in the same job.
- No website content or visual changes.

---

## v1.4.5 — Compact mobile header

Refines the mobile header proportions after the new chapter navigation was introduced.

### Changed

- Reduced the mobile MINDS4MOTION header height from `84px` to `58px`.
- Slightly reduced the small wordmark size on mobile.
- Reduced the mobile hero top padding from `57px` to `32px`.
- Moves `#JUSTCREATIVE` visibly upward while preserving its safe spacing below the sticky header.
- Chapter navigation and desktop layout remain unchanged.

---

## v1.4.4 — Mobile hero offset fix

Corrects the mobile hero position after the chapter-navigation layer was introduced.

### Changed

- Increased the mobile hero top padding from `22px` to `57px`.
- Compensates for the additional 35px fixed chapter-navigation layer.
- Restores the full visibility of `#JUSTCREATIVE` below the sticky header.
- No changes to hero typography, alignment, navigation behavior or desktop layout.

---

## v1.4.3 — GitHub Pages retry robustness

Makes GitHub Pages deployments resilient to re-running failed jobs.

### Changed

- Pages artifacts now use a unique name per workflow attempt: `github-pages-${{ github.run_attempt }}`.
- `deploy-pages` is explicitly pointed at the artifact for the current attempt.
- Prevents duplicate `github-pages` artifacts from causing deployment ambiguity during re-runs.
- No website content or visual changes.

---

## v1.4.2 — Chapter navigation + unified footer

Adds a compact sticky chapter navigation below the red scroll-progress bar and aligns footer presentation across all public pages.

### New

- Added a mini chapter navigation directly below the red progress bar on the landing page.
- Added matching chapter navigation to Imprint and Privacy Policy.
- The active chapter is highlighted while scrolling.
- On mobile, the chapter navigation remains horizontally scrollable and automatically keeps the active item in view.
- Added scroll-margin offsets so chapter links land cleanly below the fixed navigation layers.

### Changed

- Footer content is now identical on Landing, Imprint and Privacy.
- Footer typography, spacing, border treatment and mobile stacking are aligned across all three pages.
- Imprint and Privacy now also show the red scroll-progress bar.

---

## v1.4.1 — Privacy Policy + email obfuscation

Adds a dedicated privacy page and improves protection of the public contact email address.

### New

- Added `privacy.html` in the existing MINDS4MOTION visual language.
- Added a small **Privacy** link next to **Imprint** in the landing-page footer.
- Documented GitHub Pages hosting and security-related IP logging.
- Documented that MINDS4MOTION currently uses no own analytics, advertising tracking, profiling, marketing pixels or contact forms.
- Added information on email contact, external links, data-subject rights and the competent Bavarian supervisory authority.

### Changed

- Removed the clear-text email address and static `mailto:` value from `imprint.html`.
- The email address is now assembled client-side from separate JavaScript fragments and rendered as a clickable mail link in the browser.
- The same client-side rendering approach is used on the Privacy Policy page.

### Note

This reduces trivial source-code harvesting, but no publicly displayed email address can be made completely bot-proof.

---

## v1.4.0 — Imprint

Adds a dedicated legal-information page for the Germany-based MINDS4MOTION website.

### New

- Added a dedicated English-language **Imprint** page.
- Added a small, discreet **Imprint** link in the landing-page footer.
- Structured the page around current German provider-information requirements under **§ 5 DDG** and **§ 18 MStV**.
- Added contact information using the existing MINDS4MOTION email address.
- Added a consumer-dispute-resolution statement.
- Kept the visual treatment consistent with the existing black / white / red MINDS4MOTION identity.

### Publication status

- Complete serviceable postal address added.
- Imprint is ready to merge and publish.

---

## v1.3.6 — Hero alignment refinement II

Second optical adjustment of the red **4** in the large hero wordmark.

### Changed

- Shifted the red **4** further to the right.
- Target: visually align its right edge with the **N** in `MOTION` below.
- No other layout, interaction or content changes.

---

## v1.3.5 — Hero alignment refinement

Small visual polish based on mobile review.

### Changed

- Shifted the red **4** in the large hero wordmark slightly to the right.
- This visually aligns the **4** more cleanly with the **M** in the line below.
- No other layout, interaction or content changes.

---

## v1.3.4 — MOTION / STATE separated interaction layers

Replaces the previous global touch interception with a cleaner interaction architecture.

### Changed

- Removed touch/scroll locking from the full MOTION / STATE shell.
- The **canvas alone** now owns drag gestures and `touch-action: none`.
- THINK / FEEL / CREATE remain normal DOM buttons above the canvas and are no longer part of the drag-lock layer.
- The center text is pointer-transparent except for the state buttons, so the canvas remains draggable across almost the complete visual field.
- Added Pointer Events + `setPointerCapture()` on the canvas for stable iPhone dragging without page scroll.
- Added a pointer-up activation path for state buttons in addition to click as an iOS reliability fallback.
- Kept the v1.3.3 ambient drift and gravity behavior unchanged.

---

## v1.3.3 — MOTION / STATE ambient drift + tappable controls

Refines the balance between autonomous motion, touch interaction and control usability.

### Changed

- Added a persistent ultra-slow base drift so the field remains visibly alive even without touch.
- Kept the interaction velocity separate from ambient movement so touch still has clear visual weight.
- THINK / FEEL / CREATE now have slightly different ambient drift scales while staying calm.
- Excluded the state buttons from the global touch interception.
- Added `touch-action: manipulation` to the controls so buttons are tappable on iPhone.
- Gravity and drag interaction remain active everywhere else in the MOTION / STATE field.
- Page scrolling remains blocked while dragging in the interactive field, but controls are usable again.

---

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


---

## Project cut — website complete at v1.7.0

**Decision date:** 20 November 2026

The MINDS4MOTION website is considered feature-complete at **v1.7.0**.

This is an intentional cut, not a pause in unfinished work.

### What is complete

- Core MINDS4MOTION identity and narrative
- MOTION / STATE interaction
- Four Worlds
- Creative language and personal soundtrack
- Behind MINDS4MOTION
- Create Together as the light commercial edge
- DE / EN language layer
- Imprint and Privacy
- GitHub Pages deployment flow
- No tracking / no cookies approach

### What happens next

The website should now be allowed to exist and create resonance without further feature expansion.

Future changes should only be made for one of these reasons:

1. **Real user resonance** — inquiries, repeated feedback, misunderstandings or clear demand.
2. **Legal / privacy requirements** — changes that are necessary to remain compliant.
3. **Technical defects** — broken links, layout issues, deployment failures or accessibility problems.
4. **Evidence-driven improvement** — a change supported by actual usage or concrete feedback, not by the urge to keep polishing.

### Explicit non-goal

Do not continue adding features, sections, visual effects, sales mechanics, analytics or infrastructure simply because they are possible.

The next meaningful signal should come from the outside world.

**Current state:** publish, observe, learn.
