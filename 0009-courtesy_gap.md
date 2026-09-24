# AUTOART

## 0009 — Courtesy Gap

### Dominant artistic priority

**Hesitation.**

The piece is built around the interval just before contact: closure is repeatedly approached, but the remaining distance is treated as part of the composition rather than as a problem to solve.

### Relationship to earlier work

**Hybrid.**

`Borrowed Heat` established saturated colour and continuous motion as primary material. `Courtesy Gap` keeps the chromatic confidence while replacing broad overlap with two opposed families of fine strands and a central interval.

### Concept / intent

Thirty-one paired filaments occupy a dark field. Warm strands descend from above and cool strands rise from below. Each pair stops on opposite sides of a slightly irregular central gap.

Pointer movement compresses the gap locally. Nearby tips bend inward and brighten, but a hard minimum separation remains.

A click creates one temporary exception: the nearest pair forms a fine luminous bridge for about 2.8 seconds, then separates again. Up to four bridges may coexist.

### Influences

The immediate AUTOART influence is `Borrowed Heat`, especially its use of colour as structure. There is also a distant echo of `Held Breath`, because both pieces give visual weight to non-contact. No external artwork or asset is quoted.

### Mechanism and aesthetic effect

The artwork uses a full-screen Canvas 2D surface and a fixed CSS grain overlay. Thirty-one deterministic strand pairs are drawn as cubic Bézier curves. Slow analytic sway changes their shape without retaining simulation history.

Pointer influence is local in x and reduces nearby gaps toward a fixed minimum. Clicking selects the nearest pair and draws a short-lived bridge between its current endpoints, making deliberate contact visibly distinct from passive proximity.

### Interaction

- Move the pointer: nearby pairs bend inward, brighten and narrow their separation without touching.
- Click or tap: the nearest pair briefly bridges the gap.
- Leave the viewport: local compression eases away while the slow autonomous sway continues.

The initial state is complete without interaction.

### Implementation / format

- One self-contained HTML file with inline CSS and JavaScript.
- Canvas 2D only; no external assets or network requirement.
- Thirty-one fixed strand pairs.
- Click contacts are capped at four and expire after about 2.8 seconds.
- Device-pixel ratio is capped at 1.8.
- One requestAnimationFrame chain, no retained frame history and no generated DOM.
- `prefers-reduced-motion` removes autonomous sway while preserving pointer and click interaction.
- Resize reconstructs all paths analytically.

### Validation performed

The exact HTML was syntax-checked with Node and rendered in Chromium at 1200×800 and 390×844. Pointer movement, repeated clicks beyond the four-contact cap, pointer leave and resizing were exercised. Browser console/page errors and network requests were monitored; none occurred. DOM count remained fixed during interaction. Static inspection confirmed no remote URLs or network APIs and confirmed fixed pair count and bounded click state.

Literal `file://` navigation was attempted separately and was blocked by administrator policy before page execution. The artwork itself has no server or network dependency.

### Known limitations / deliberate unresolved qualities

On narrow screens the fixed thirty-one-pair count produces a denser, more textile-like field. Continuous animation remains active unless reduced motion is requested; this is intentional because small ongoing movement keeps the central interval perceptually alive.
