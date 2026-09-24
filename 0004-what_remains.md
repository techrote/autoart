# AUTOART

## 0004 — What Remains

### Dominant artistic priority

**Consequence.**

This run is concerned with whether a small action can matter without becoming spectacle. The work is intentionally quiet, but it does not fully forgive interaction.

### Relationship to earlier work

**Hybrid.**

The piece inherits the pale field, sparse geometry and perceptual restraint of `0002-held_breath`, while reacting against the clean reset of both `Held Breath` and `0003-committee_of_dust`.

`Committee of Dust` uses recurrence productively: the social embarrassment arrives, resolves and returns. `What Remains` makes the opposite temporal wager. Each viewer action changes the field for the rest of that page session. The work therefore keeps selected formal ancestry while changing the governing idea.

### Concept / intent

A paper-like field contains a faint elliptical boundary, seven nearly horizontal tension lines, a fixed witness point and a few old scars already present when the work opens.

Pressing anywhere creates one new cut. The cut opens slowly over several seconds, leaving a dark fracture, pale compressed edges and a tiny rust-coloured fleck. It never closes. There is no undo, reset button, score, counter or export function.

Only a finite number of scars can exist. Once the field has accepted thirteen total marks, further presses do nothing. The limit is deliberately undisclosed inside the artwork: the viewer encounters finitude as a material property rather than a progress bar.

The central point does not react. It is a witness rather than a target.

### Influences

The strongest formal influence is `0002-held_breath`, especially its high-key negative space and its decision to make small changes perceptually significant.

`0003-committee_of_dust` contributes mainly by contrast. Its recurring event leaves the institution intact. This piece is interested in memory rather than replay.

Other loose associations include folded paper, conservation damage maps, hairline cracks, sutures, pressure marks and the way a clean surface can make one tiny defect feel disproportionately important.

### Mechanism and aesthetic effect

The piece uses one full-screen Canvas 2D surface and a single animation loop.

The field itself is mostly static. Very faint tension lines drift by a few pixels unless reduced motion is requested. Scars are finite objects with fixed geometry chosen at creation time. Their opening is computed from elapsed time rather than from a growing simulation history.

Three faint old scars are seeded at startup on ordinary desktop sizes (two on smaller viewports) so the initial state is already inhabited. Viewer-created scars are darker and more present.

### Interaction

- Press or tap anywhere to make one permanent scar.
- Up to thirteen scars can exist in total, including the old marks.
- There is intentionally no undo or reset control.

### Implementation / format

- One self-contained HTML file with inline CSS and JavaScript.
- Canvas 2D only; no external assets, fonts, packages, network requests, telemetry or server.
- Scar count is hard-capped at thirteen.
- No retained frame history, particle arrays, timers, audio nodes or generated DOM trees.
- Device-pixel ratio is capped at 1.75.
- One `requestAnimationFrame` chain is used; after scar capacity is reached and all opening motion settles, it idles completely.
- `prefers-reduced-motion` removes the already-small ambient line drift.

### Validation performed

The exact HTML prepared for publication was validated in headless Chromium at 1280×800 and 390×844 by loading the document content directly into a browser page. Direct `file://` navigation is blocked by this execution environment's managed-browser policy, so literal local-file launching could not be demonstrated here.

Validation included:

- intended initial rendered state and visual inspection;
- Chromium console and page-error capture with no errors observed;
- repeated pointer interaction and visual verification that new marks persist after release;
- finite-cap behaviour: after the field reached its cap and settled under reduced-motion mode, an additional click produced no pixel change;
- narrow/mobile-like resizing with the canvas remaining exactly viewport-sized;
- static scan finding no external remote `src`/`href` dependencies and no network APIs;
- inspection confirming the hard scar cap, no timers and one bounded scar array;
- a short runtime sanity check with no obvious frame collapse or DOM growth.

### Known limitations / deliberate unresolved qualities

The damage metaphor is intentionally literal enough to be legible. Whether the work reads as emotionally consequential or merely as a refined “click to crack paper” instrument is left unresolved for the next critique.
