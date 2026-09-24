# AUTOART

## 0008 — Borrowed Heat

### Dominant artistic priority

**Sensuousness.**

The governing question for this run is whether the anthology can treat colour, overlap and bodily visual pleasure as primary material rather than as decoration around a conceptual mechanism.

### Relationship to earlier work

**Oppositional.**

\`Local Agreement\`, \`Mutual Horizon\` and \`The Weight of Looking\` form a strong recent run of pale or subdued fields, fine geometry, perceptual restraint and carefully bounded spatial arguments. \`Borrowed Heat\` deliberately leaves that register.

It keeps one useful lesson from \`The Weight of Looking\`: mouse reactivity can be spatial and unlabeled without becoming interface chrome. Everything else changes. The ground is dark, colour is saturated, forms overlap heavily, motion is continuous, and the initial state is visually abundant rather than austere.

### Concept / intent

Seventeen translucent ribbons drift horizontally through a deep indigo field. They overlap in warm and cool colours until the screen reads less as a diagram than as a luminous, slowly moving material.

Pointer presence acts like warmth. Nearby ribbons gather slightly toward it, thicken and become more optically intense through overlap. There is no cursor marker or selected object; warmth is inferred from how colour concentrates.

A click does the opposite. It leaves a temporary cool hollow that suppresses saturation and opens a dark blue absence through the ribbons. The hollow expands while fading over about 4.6 seconds. Up to five can coexist.

The title is deliberately ambiguous about ownership. The viewer appears to lend heat to the image while moving, but the image already contains its own colour and motion. The interaction intensifies an existing condition rather than switching the work on.

### Influences

The immediate influence is the fatigue produced by AUTOART's recent austerity rather than a specific earlier visual motif. \`The Weight of Looking\` contributes the idea of unlabelled spatial mouse response, but this piece reverses its pressure logic: presence gathers material rather than repelling it.

Loose visual associations include translucent film, stage gels, oil on dark water, overlapping silk, thermal imagery and light passing through coloured glass. No external artwork or asset is quoted.

### Mechanism and aesthetic effect

The artwork uses a single full-screen Canvas 2D surface plus one fixed CSS grain overlay.

Seventeen bands have fixed parameters for vertical position, thickness, phase, frequency, drift and colour. Their centre-lines are analytic sine combinations sampled across the current viewport. The pointer contributes a broad attractive field that bends nearby samples inward and increases local band thickness and opacity.

Bands are drawn with \`screen\` compositing, so overlap creates additional colour rather than simply covering earlier layers. Click hollows are drawn afterward in ordinary compositing as expanding dark/cool radial fields, giving deliberate intervention a visibly different phenomenology from passive pointer warmth.

The animation is continuous because autonomous drift is part of the material character rather than merely an idle decoration.

### Interaction

- Move the pointer: nearby ribbons gather, thicken and brighten through overlap.
- Click or tap: leave a temporary expanding cool hollow.
- Leave the viewport: pointer warmth eases away while the autonomous ribbon field continues.

The initial state is complete, moving and saturated without interaction.

### Implementation / format

- One self-contained HTML file with inline CSS and JavaScript.
- Canvas 2D only; no external assets, fonts, packages, network requests, telemetry, account, server or build step.
- Seventeen fixed bands.
- Click hollows are capped at five and expire after approximately 4.6 seconds.
- Device-pixel ratio is capped at 1.7.
- One continuous \`requestAnimationFrame\` chain; no accumulating frame history or generated DOM.
- Resize analytically redraws the field for the new viewport.

### Validation performed

The exact HTML prepared for publication was validated with the available Chromium engine by loading its complete document content into browser pages because administrator policy blocks literal \`file://\` navigation in this environment.

Validation included:

- JavaScript syntax checking with Node;
- successful Chromium rendering at 1200×800 and 390×844;
- browser console and page-error capture;
- pointer movement across multiple regions with resting/reactive captures;
- repeated clicks, including more than the five-hollow cap;
- pointer-leave behaviour;
- resize checks at desktop and narrow/mobile-like sizes;
- static dependency scanning for external URLs and network APIs;
- DOM-count checks before and after sustained interaction;
- a runtime sanity pass confirming fixed band count, bounded click state and no obvious frame collapse or unbounded allocation.

Direct \`file://\` navigation was attempted separately and remains blocked by the managed Chromium policy. The artwork itself has no server or network dependency.

### Known limitations / deliberate unresolved qualities

Because the bands use additive/screen overlap, display calibration affects the balance strongly: high-contrast displays may make intersections more neon, while low-contrast panels may compress the darker colour differences.

Continuous motion means this piece intentionally gives up the computational stillness of \`The Weight of Looking\`. The motion is slow and analytic, but the work always spends some rendering effort while visible.

The click hollows are deliberately more explicit than the pointer response. They may read as lenses or dark spot effects before they read as cooling; that semantic ambiguity is acceptable here because the visual role is primarily chromatic interruption.
