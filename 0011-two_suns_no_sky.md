# AUTOART

## 0011 — Two Suns, No Sky

### Dominant artistic priority

**Tactility.**

The governing question is whether a browser artwork can feel materially layered before it feels computational. The mechanism is intended to disappear behind the familiar physical language of coloured material, light and shadow.

### Relationship to earlier work

**Independent.**

`Almost Says` exposes a symbolic grammar of segmented marks, recognition targets and deliberate omissions. `Two Suns, No Sky` leaves that territory rather than extending it.

The only retained lineage is the requirement that pointer response belong to the artwork rather than appear as interface chrome. Here the pointer behaves as an unseen light source.

### Concept / intent

Ten coloured, cut-paper-like forms lie on a warm field. Their shapes never move.

At rest they share one coherent soft shadow direction, allowing the composition to read as a simple physical collage under one lamp. Moving the pointer changes that direction: every primary shadow pivots together while the coloured forms remain fixed.

Clicking or tapping introduces one temporary second “sun.” For about 4.8 seconds a cooler, softer shadow appears from another direction. The two shadow systems disagree about where light should originate, making the unchanged forms feel alternately lifted, thickened, doubled or spatially impossible. A later click relocates the temporary second sun rather than accumulating additional lights.

There is no drawn lamp, cursor marker, control panel or explanatory label inside the artwork.

### Influences

The immediate motivation comes from reviewing `Almost Says`: after several works where the digital rule is visibly expressed as geometry, notation or field behaviour, tactile illusion felt more urgent than another legibility problem.

Loose associations include cut paper, classroom collage, desk lamps, coloured card and shadow theatre. No external artwork, font, asset or repository material is quoted.

### Mechanism and aesthetic effect

The piece uses one inline SVG. Ten fixed path definitions are reused as the coloured forms, the primary shadow layer and the temporary secondary shadow layer.

Pointer position changes only the primary shadow group's translation. The forms themselves remain pixel-stable.

A click records one temporary secondary-light position. Its duplicate shadow layer receives a larger, cool-tinted offset and then fades completely over 4.8 seconds. A subsequent click replaces that one temporary state, so state cannot accumulate.

The animation loop is event-driven: it runs while the primary shadow is easing to a new position or while the secondary shadow is fading, then stops.

### Interaction

- Move the pointer: change the direction of the primary shadow field.
- Click or tap: create one temporary contradictory second shadow.
- Click again while it is active: relocate that second shadow rather than add another.
- Leave the viewport: the primary shadow eases back to its authored resting direction.

The initial composition is complete without interaction.

### Implementation / format

- One self-contained HTML file with inline CSS, SVG and JavaScript.
- No external assets, fonts, packages, stylesheets, server, account, telemetry or network access.
- Ten fixed SVG path definitions and a fixed DOM.
- One primary shadow state and at most one temporary secondary shadow state.
- Secondary-shadow lifetime is approximately 4.8 seconds.
- One event-driven `requestAnimationFrame` chain that becomes idle after easing/fade completes.
- `prefers-reduced-motion` increases easing speed rather than removing interaction.
- A fixed SVG `viewBox` with `xMidYMid slice`; narrow screens intentionally crop the outer collage while preserving the apparent material scale.

### Validation performed

The exact HTML intended for publication was validated as follows:

- parsed successfully as HTML;
- exact inline JavaScript extracted from it passed `node --check`;
- static scanning found no external `src`, no remote `href`, no `http://` or `https://`, and no fetch/XHR/WebSocket/EventSource/Worker/dynamic-import path;
- exact inline SVG rasterised successfully with Inkscape at 1200×800 and was visually inspected;
- the same SVG was rendered and inspected in a 390×844 portrait viewport using the authored `xMidYMid slice` behaviour;
- a minimal mocked DOM/RAF runtime executed the exact script through startup, pointer movement, click, a second click, pointer leave, secondary-shadow expiry and resize without exceptions;
- the mock confirmed that pointer motion changes the primary shadow transform, a click makes the secondary shadow visible, a later click relocates instead of accumulating it, the secondary shadow returns to zero opacity after expiry, and the RAF queue returns to idle;
- transforms produced by that exact script were applied to the exact SVG and rasterised for visual inspection of pointer and two-shadow states;
- direct Chromium `file://` rendering was attempted, but the installed browser currently stalls during graphics/compositor initialisation and produced no page image within the timeout. No live-browser or console result is claimed.

### Known limitations / deliberate unresolved qualities

The broad soft shadows can make the forms read as pebbles, tablets or ceramic pieces rather than literal paper. That is acceptable because the priority is tactile depth, not strict material imitation.

On tall portrait screens, `slice` crops outermost forms. This is intentional; preserving apparent scale and shadow softness was preferred to shrinking the entire collage into a small central strip.

The second shadow is a global lighting contradiction rather than a local one. Once the rule is understood, further clicks change direction rather than reveal a new class of behaviour.
