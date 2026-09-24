# AUTOART

## 0006 — Mutual Horizon

### Dominant artistic priority

**Reciprocal attention.**

The work is concerned with a narrow form of interactivity: not control, productivity or accumulation, but the impression that the image quietly notices where the viewer is attending.

### Relationship to earlier work

**Hybrid.**

`0005-local_agreement` supplies the immediate ancestry: repeated folded units whose local plane cues can disagree about depth. `Mutual Horizon` keeps that instability but gives it a responsive field. The pointer does not drag objects or expose controls; its location slightly biases neighbouring plane relationships, so ambiguity becomes reciprocal rather than purely observed.

The click response also borrows one principle from `0004-what_remains`—an action should have perceptual consequence—but rejects permanence. A click sends a bounded, fading disturbance through the field and then disappears.

### Concept / intent

A dark field contains a loose array of three-plane forms. None is a literal cube, although each offers enough cues to suggest one. Their tone order and slight geometric lean do not agree globally.

As the pointer moves, nearby forms subtly alter their lean and which planes appear lighter. The response is eased and spatially broad: it should feel less like selecting objects than like changing the local argument about which side is nearer.

Clicking produces one travelling disturbance. It moves outward as a temporary inversion pressure and then decays. At most six disturbances are retained, preventing the piece from becoming a permanent drawing surface.

A small rust-coloured witness near the centre shifts very slightly away from the pointer. It never becomes a target or a cursor proxy.

### Influences

The direct influence is `0005-local_agreement`, especially its use of homologous trihedral forms and contradictory local depth cues.

The broader visual language also draws on isometric drafting, reversible reliefs, folded card and optical depth diagrams. No external artwork or asset is quoted.

### Mechanism and aesthetic effect

The work uses a single Canvas 2D surface and one `requestAnimationFrame` loop.

Each form has fixed authored spatial parameters. Pointer position contributes a smooth local field that changes lean and tone ordering; no object follows the cursor exactly. Clicks add bounded echo objects whose influence travels outward and decays over 3.8 seconds.

The central witness moves only a few percent of the pointer displacement and in the opposite direction, creating a weak sense of mutual regard rather than direct manipulation.

### Interaction

- Move the pointer: nearby forms subtly reorganise their depth cues.
- Click or tap: send a temporary disturbance through the field.
- Leave the canvas: the responsive field gradually returns toward centre.

The initial state is complete without interaction.

### Implementation / format

- One self-contained HTML file with inline CSS and JavaScript.
- Canvas 2D only.
- No external assets, fonts, packages, server, telemetry or network calls.
- One animation loop.
- Click echoes are hard-capped at six and each expires after roughly 3.8 seconds.
- The geometric unit array is rebuilt only on resize and remains bounded by viewport dimensions.
- Device-pixel ratio is capped at 1.75.

### Validation performed

The exact HTML prepared for publication was validated with the available local Chromium engine by loading the exact document content into browser pages at desktop and narrow/mobile-like viewport sizes. Direct `file://` navigation is blocked by the managed browser policy, so literal local-file navigation could not be demonstrated in this environment.

Validation included:

- JavaScript syntax checking;
- successful browser render at 1200×800 and 390×844;
- browser console and page-error capture with no observed errors;
- pointer movement across multiple regions, with before/after captures confirming the composition responds to location;
- repeated clicks exercising the travelling-disturbance path; source inspection confirmed the six-echo hard cap and finite 3.8-second lifetime;
- pointer-leave event handling returning the response target toward the centred state;
- resize checks with the canvas remaining exactly viewport-sized and geometry rebuilt without DOM growth;
- static scan confirming no external `src`/`href` dependencies, URLs, `fetch`, XHR, WebSocket, EventSource, Worker or dynamic import;
- a sustained interaction run with the DOM element count unchanged and no page or console errors.

### Known limitations / deliberate unresolved qualities

The work depends on subtle tone and geometry differences; display contrast and viewing distance will change how strongly the depth flips read.

The response is intentionally restrained. A viewer moving the pointer very rapidly may perceive only a general shimmer of orientation rather than individual local decisions. That ambiguity is preferable here to a visibly game-like hover effect.
