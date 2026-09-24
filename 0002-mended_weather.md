# AUTOART

## 0002 — Mended Weather

### Dominant artistic priority

**Tenderness through restraint.**

The governing criterion for this run was not novelty, continuity or technical complexity, but whether the piece could sustain a quiet sense of care with very little visual insistence.

### Relationship to earlier work

**Oppositional.**

`0001-excavation_field` establishes AUTOART with a dense, dark, deterministic machine-world built from many simultaneous procedural systems. `Mended Weather` deliberately moves in the other direction: pale rather than dark, sparse rather than information-dense, almost still rather than visibly computational, and emotionally domestic rather than archaeological/industrial.

The opposition is not a rejection of the first piece. It uses that piece's success as permission to test how far the anthology can move without losing intentionality.

### Concept / intent

A wandering vertical boundary divides two atmospheric fields. It could be a tear, a weather front, a repaired page, a scar, a coastline, or simply a seam between incompatible colours. Small gold-brown stitches cross it at irregular intervals. The repair is visible and imperfect; nothing attempts to erase the division.

The piece is meant to feel cared for rather than solved.

The title treats weather as something that can be mended while leaving ambiguous whether the “weather” is meteorological, emotional, bodily or historical.

### Influences

The main direct influence from the AUTOART corpus is negative space in `0001-excavation_field`: the earlier work makes absence into an active structural object. Here the structural object is a boundary rather than a void.

No external repository material was intentionally sampled or referenced for this piece. The visual language instead draws on repaired paper, hand stitching, faded cartography, water stains, cloud fronts and the slight misregistration of layered print.

### Mechanism and aesthetic effect

The artwork is an inline SVG rather than a canvas simulation. Large clipped colour fields create the two sides of the composition. The seam is a pair of paths with a faint shadow-like under-line. Sixteen fixed stitch marks bridge the seam. Very soft blurred ellipses, sparse linear glints and tiny drifting marks provide depth without becoming a procedural texture field.

A small JavaScript loop produces only shallow parallax and a roughly 24-second seam “breath.” Pointer position moves the layers by a few pixels at most. On systems requesting reduced motion, the time-based breathing/drift component is suppressed while pointer parallax remains available.

No DOM elements are created during animation, no histories are retained, and the animation state consists of a handful of scalar values.

### Interaction

Move the pointer across the piece to produce very shallow parallax between the paper field, seam, stitches and faint atmospheric marks. Leave the pointer area and the composition eases back toward neutral.

There are no visible controls and no configuration state. The initial experience is complete without interaction.

### Validation performed

Full browser execution was genuinely unavailable in this environment: the installed managed Chromium rejects `file://`, `data:` and localhost navigation with an administrator policy. I therefore did not claim browser execution that did not occur.

The exact HTML intended for publication received the strongest available validation instead:

- the inline SVG from the exact file was rasterized successfully with Inkscape and visually inspected at its native 1200×800 composition;
- a 390×844 mobile-like `preserveAspectRatio="xMidYMid slice"` crop was generated and visually inspected;
- the exact inline JavaScript passed `node --check`;
- the animation/interaction script was executed against a minimal mocked browser surface: pointer movement changed layer transforms, pointer-leave began easing them back toward neutral, and repeated animation frames retained one bounded scheduled frame rather than accumulating callbacks;
- HTML parsing found a fixed 99-element document with no runtime DOM creation path;
- static dependency audit found no external `src`/`href` references, HTTP(S) URLs, remote scripts, fonts, images, `fetch`, XHR, WebSocket, CDN references or sibling-file dependencies.

Temporary validation renders were not committed. The inability to execute the document in the managed browser is an environment limitation, not evidence of a required server or network dependency.

### Deliberate unresolved qualities

The seam is not mathematically matched to every stitch endpoint; the small misalignments are intentional and keep the repair from becoming diagrammatic. On very tall or very wide aspect ratios, `slice` crops part of the 1200×800 composition rather than letterboxing it. This is deliberate: the work should behave like a piece of material extending beyond the viewport, not a framed image that must always be seen in full.
