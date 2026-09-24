# AUTOART

## 0012 — Right of Way

### Dominant artistic priority

**Occlusion.**

The governing question is whether the simple act of one thing hiding another can carry enough tension to become the artwork's main material. The piece is not primarily about motion, simulation or colour change. It is about precedence at crossings: which strand is allowed to be in front, and how stable that decision feels.

### Relationship to earlier work

**Hybrid.**

`Two Suns, No Sky` contributes a concern with apparent material depth, but `Right of Way` removes the lighting illusion that created most of that depth. Instead, depth is decided locally by overlap.

The work also recalls AUTOART's earlier interest in reciprocal attention, but the pointer does not bend, drag or illuminate the ribbons. It weakens certainty about which strand owns the foreground. A click briefly grants the opposite strand precedence at one nearby crossing.

### Concept / intent

Two families of broad curved ribbons traverse a warm field: blue-green strands mainly from left to right, and terracotta strands mainly from top to bottom. Their paths cross fifty-six times.

At rest the crossings follow a strict alternating weave. Each local junction is easy to read: one ribbon passes over, the other under. Across the full field this creates a coherent but slightly restless textile-like order.

Moving the pointer does not displace any ribbon. Instead, nearby crossings become less certain. The explicit overpass patch fades toward a half-state, allowing both colours to occupy the same crossing visually. Attention therefore weakens hierarchy rather than clarifying it.

Clicking or tapping near a crossing temporarily reverses its ordinary right of way. A faint pale seam marks the claimed junction while the inversion decays over roughly 5.6 seconds. At most three claims can exist at once.

### Influences

The immediate AUTOART influence is `Two Suns, No Sky`, specifically its interest in making depth feel physical without moving the underlying forms. This piece retains material overlap but abandons the global shadow model.

Broader associations include woven tape, road junctions, basketry, over-under diagrams, interlaced maps and the social language of yielding or taking precedence. No external artwork, asset, font or repository material is quoted.

### Mechanism and aesthetic effect

The artwork uses one full-screen Canvas 2D surface.

Eight horizontal-ish and seven vertical-ish ribbons are generated from deterministic sinusoidal paths. Their fifty-six intersections are solved numerically from those same analytical curves whenever the viewport changes.

The vertical family is drawn after the horizontal family as the default underlying render order. Local horizontal overpasses are then reconstructed at selected crossings using a ground-coloured cutout, a small shadow offset and a short ribbon segment. The alternating checkerboard rule determines ordinary precedence.

Pointer proximity interpolates the local overpass strength toward an ambiguous half-state without moving either path. Click claims temporarily invert the baseline order for the nearest crossing. Claims are finite and hard-capped.

The animation loop is event-driven. It runs while pointer easing or temporary claims are active and otherwise stops.

### Interaction

- Move the pointer: nearby crossings lose some of their ordinary over/under certainty.
- Click or tap near a crossing: temporarily reverse that crossing's precedence.
- Leave the viewport: pointer influence fades and the ordinary weave returns.

The initial state is complete without interaction.

### Implementation / format

- One self-contained HTML file with inline CSS and JavaScript.
- Canvas 2D only; no external assets, fonts, stylesheets, packages, server, account, telemetry or network access.
- Eight fixed horizontal path definitions and seven fixed vertical path definitions per viewport reconstruction.
- Fifty-six bounded crossing records.
- At most three temporary click claims, each expiring after approximately 5.6 seconds.
- Device-pixel ratio capped at 1.75.
- One event-driven `requestAnimationFrame` chain that becomes idle when pointer easing and claims settle.
- Resize reconstructs paths and intersections analytically; no retained frame history or stale bitmap state is scaled.

### Validation performed

The exact HTML published on the branch was validated after constructing its Git blob:

- the exact branch HTML was fetched back from GitHub and its inline JavaScript passed `node --check`;
- static inspection found no external `src`, remote `href`, `http://` or `https://`, and no fetch/XHR/WebSocket/EventSource/Worker/dynamic-import path;
- Chromium rendered the exact branch document content at 1200×800 and 390×844 with no page or console errors and no network requests;
- the intended alternating weave was visually inspected at rest;
- pointer movement was exercised across multiple regions and nearby crossings visibly moved toward ambiguous half-precedence without ribbon displacement;
- repeated clicks exercised local reversal, replacement of an existing claim for the same crossing, and the three-claim hard cap;
- pointer-leave recovery and post-claim return to the ordinary weave were exercised;
- resize rebuilt the analytical paths and all fifty-six intersections without DOM growth;
- sustained interaction confirmed a fixed document structure and a single animation-frame chain that returns to idle after claims expire.

Literal `file://` navigation is blocked by administrator policy in the available Chromium environment. Browser validation therefore loaded the exact file contents into the page rather than claiming a direct local-file navigation that did not occur. The artwork itself has no server or network requirement.

### Known limitations / deliberate unresolved qualities

At very small viewport sizes the dense crossings can read more as braided pattern than as individually legible over/under decisions. The portrait layout intentionally retains the same number of strands rather than simplifying the work.

The pointer's half-precedence state is visually ambiguous by design. Some viewers may read it simply as colour blending rather than as uncertainty about foreground order.

The click seam is deliberately faint. It marks a temporary claim without turning crossings into selectable interface objects.
