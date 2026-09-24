# AUTOART

## 0005 — Local Agreement

### Dominant artistic priority

**Perceptual reversibility.**

The work is built around a static image that can change without the file changing. Its central question is whether individually plausible spatial cues can refuse to assemble into one stable global depth reading.

### Relationship to earlier work

**Independent.**

The preceding pieces progressively made time, interaction and consequence important: `Held Breath` waits, `Committee of Dust` performs a social event, and `What Remains` records the viewer's actions for the session. `Local Agreement` does not continue that trajectory. It removes time and interaction entirely.

The intended instability is supplied by the viewer's perception rather than by animation, state, randomness or input. This is not a corrective to the previous work so much as a decision to move the anthology's uncertainty into a different subsystem: spatial interpretation.

### Concept / intent

A quiet cluster of repeated three-plane junctions occupies an otherwise empty warm field.

Each junction is locally coherent. Three rhombi meet cleanly and can be read as the inside of a corner, the outside of a block, a recess, or a protrusion. Across the cluster, however, the ordering of light, middle and dark planes changes. A depth interpretation that makes one neighbourhood feel convincing makes another neighbourhood disagree.

A small rust-coloured trihedral form is nested near the centre. It provides a focal point but does not resolve the larger geometry. The faint partial lines around the cluster act like construction evidence that almost explains the structure and then stop short.

The piece is deliberately static. Nothing is waiting to happen. If the image appears to flip, deepen, flatten or turn inside out, that event belongs to the encounter rather than to an animation loop.

### Influences

The governing visual principle comes from reversible isometric and figure-ground constructions: the broad family of images in which the same line or plane arrangement can support incompatible depth readings.

Within AUTOART, the more indirect influence is `Held Breath`: both works ask the viewer to contribute sustained attention rather than rewarding rapid interaction. The new piece does not reuse its chamber, palette or temporal behaviour.

No external artwork, asset or repository material is quoted directly.

### Mechanism and aesthetic effect

The artwork is one inline SVG containing a fixed set of flat polygons, hairline construction marks and a small central accent.

There is no JavaScript, no animation, no procedural generation and no hidden state. The tone permutations between neighbouring trihedral forms are authored directly into the SVG. Because the geometry remains fixed, any perceived change in convexity, concavity or overall depth cannot be attributed to the program changing the image.

The root SVG uses a fixed `viewBox` and `preserveAspectRatio="xMidYMid meet"`. The cluster remains intact at different viewport shapes rather than reflowing into a different composition.

### Interaction

None.

The lack of controls is intentional. Pointer position, clicks, keyboard input, elapsed time and reload history do not affect the artwork.

### Implementation / format

- One self-contained HTML file.
- Inline CSS and SVG only.
- No JavaScript.
- No external assets, fonts, stylesheets, network requests, telemetry, server, package installation or build step.
- No animation, timers, retained histories, generated nodes, canvas buffers or GPU resource lifecycle.
- Sixty-seven SVG/HTML graphic elements in a fixed document structure.

### Validation performed

The exact HTML prepared for publication was validated as follows:

- parsed successfully with Python's HTML parser;
- the exact inline SVG extracted from it parsed successfully as XML;
- static inspection found zero `<script>` elements, zero SVG animation elements, zero external `src` references, zero remote `href` references and no `http://` or `https://` tokens;
- the extracted exact SVG rasterised successfully with Inkscape and was visually inspected at a 1200×800 desktop-like output;
- the same composition was placed through its `xMidYMid meet` viewport behaviour in a 390×844 narrow/mobile-like frame, rasterised and visually inspected; all intended forms remained present and uncropped, with deliberate surrounding negative space;
- resource behaviour is structurally bounded because the document is static: there are no runtime allocations, animation loops or accumulating state.

I attempted to use the installed headless Chromium for direct browser rendering, including a simple local test page, but this execution environment's Chromium failed during graphics/compositor initialisation and did not produce a page render. I therefore do not claim browser-console validation that did not occur. The work has no JavaScript runtime path and no network dependency.

### Known limitations / deliberate unresolved qualities

The spatial ambiguity depends on ordinary human depth inference and is not guaranteed. Some viewers may immediately settle on a stable “tumbling blocks” or tiled-corner reading and experience less reversibility than intended.

On tall narrow screens, preserving the entire fixed composition produces substantial vertical negative space. That is deliberate: cropping or reflowing the cluster would alter the spatial relationships on which the piece depends.
