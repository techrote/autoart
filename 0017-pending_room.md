# AUTOART

## 0017 — Pending Room

### Dominant artistic priority

**Temporal suspense.**

The work is concerned with the period after an action has been accepted but before its consequence becomes certain. The delay itself is intended to be perceptible material rather than dead time between input and response.

### Publication provenance and predecessor lineage

- Original starting authoritative `main`: `db70ea9eb0bf98c2989aa34cdef8a7fd45673d3f`.
- Selected predecessor: `0016-elsewhere_answers`.
- The separately published excavation-line work present on the starting corpus was reviewed as context but is not a predecessor of this ordinary AUTOART piece.

### Relationship to earlier work

**Hybrid.**

`Elsewhere Answers` contributes one governing ancestry: cause and visible consequence do not need to share the viewer's expected coordinates. `Pending Room` keeps the refusal of immediate interface-like confirmation but moves the uncertainty from **where** to **when**.

The work also changes the visual language completely. The saturated floating panes are replaced by a pale, nearly institutional architectural field whose five seams appear capable of opening but remain closed most of the time.

### Concept / intent

A quiet room-like field contains five narrow vertical seams, a low bench-like horizontal form, weak perspective lines and one fixed witness speck.

Pointer movement does not open anything. It slightly changes local seam tension and the room's vanishing pressure, making the architecture feel attentive without behaving like a conventional hover interface.

Clicking or tapping arms exactly one seam. The selected seam is determined by horizontal click position, while vertical click position determines an undisclosed delay between roughly 1.8 and 5.4 seconds. Higher clicks wait longer; lower clicks answer sooner. The artwork never displays that rule, a countdown or a progress indicator.

During the wait, the selected lintel thickens almost imperceptibly and the seam develops tiny breathing-scale tension. A brief false start occurs a little over halfway through the wait: the seam parts by only a fraction of the eventual opening, then closes again.

When the delay finally expires, the seam opens modestly onto a narrow amber-grey recess, holds for a moment, then closes. Nothing enters. Nothing is revealed beyond the fact that the room eventually answered.

Clicking again while an event is pending replaces the previous pending event rather than stacking multiple timers or openings.

### Influences

The direct AUTOART influence is `0016-elsewhere_answers`, specifically its refusal of immediate local causality.

Looser associations include waiting rooms, lift doors that seem about to arrive, corridor fire doors, institutional architecture, stage wings, annunciator systems with no visible display, and the bodily habit of watching a doorway after hearing something on the other side.

No external artwork, image, font, asset or repository material is quoted.

### Mechanism and aesthetic effect

The artwork uses one full-screen Canvas 2D surface.

Five seam positions are derived analytically from viewport width. The room boundary, perspective lines, bench and witness speck are fixed composition elements. Pointer state only modifies small line-width, lean and vanishing-point offsets; there is no cursor proxy or generated DOM.

One optional `pending` record contains:

- the selected seam index;
- click birth time;
- a deterministic delay computed from click height.

The event is evaluated entirely from `performance.now()` inside the existing animation loop. There are no timeout or interval APIs.

Before the event, anticipation is deliberately under-signalled. A narrow Gaussian false-start envelope near 58% of the wait briefly produces a tiny opening. After the hidden delay, the actual opening uses a finite open/hold/close envelope and then deletes the pending state completely.

The animation loop sleeps whenever pointer easing is settled and no pending event exists.

### Interaction

- Move the pointer: introduce a small local seam tension and a slight change in the room's perspective pressure.
- Click or tap: arm the nearest seam horizontally.
- Click height influences how long the room waits before answering; no visible timer exposes the mapping.
- Click again while waiting or opening: replace the current pending event with the new one.
- Leave the viewport: live pointer tension fades, but an already armed event continues to its finite conclusion.

The initial state is complete, static and meaningful without interaction.

### Implementation / format

- One self-contained HTML file with inline CSS and JavaScript.
- Canvas 2D only.
- No external assets, fonts, stylesheets, packages, build step, server, account, telemetry or network access.
- Five fixed conceptual seams.
- At most one pending event record.
- Delay range approximately 1.8–5.4 seconds.
- Actual opening envelope: roughly 420 ms open, 260 ms hold, 920 ms close.
- No `setTimeout` or `setInterval` use.
- One event-driven `requestAnimationFrame` chain.
- Device-pixel ratio capped at 1.75.
- Resize reconstructs all geometry analytically for the new viewport.
- `prefers-reduced-motion` reduces opening amplitude and speeds pointer easing while retaining the waiting structure.

### Validation performed

Validation was performed against the exact HTML prepared for publication.

- The inline JavaScript was extracted from the exact HTML and passed `node --check`.
- Static inspection found no HTTP(S) token, external `src`, remote `href`, `fetch`, XHR, WebSocket, EventSource, Worker, dynamic import, `setTimeout` or `setInterval` path.
- Literal `file://` navigation was attempted in Chromium and was blocked by the managed browser policy before the artwork executed.
- The exact HTML bytes were then loaded directly into the Chromium document through the browser debugging interface; the resulting document title, nine-element DOM and canvas dimensions confirmed that the artwork itself—not the browser policy page—was executing.
- The exact document rendered successfully at 1200×800 and 390×844; both resting compositions were visually inspected.
- Pointer movement, clicks selecting different seams, a short-delay event, a long-delay event, the false-start phase, full opening/hold/closing, replacement of an already-pending event, pointer leave and resize were exercised.
- Desktop and portrait screenshots changed across the expected interaction states; the seam opening was visibly distinct from the resting state.
- Browser capture reported zero JavaScript exceptions, zero console warnings/errors and zero network requests during the successful artwork run.
- DOM count remained fixed at nine and canvas backing/CSS dimensions tracked both tested viewports.
- In a focused settle check, a lower click was armed, pointer pressure was removed, and after the complete delay/open/close lifetime the final 1200×800 screenshot was pixel-identical to the initial resting screenshot.
- Source inspection confirms one replaceable `pending` record and one event-driven requestAnimationFrame chain, with no accumulating histories, generated nodes or timer APIs.

Temporary validation screenshots and harness files are not part of the publication files.

### Known limitations / deliberate unresolved qualities

The work deliberately risks being mistaken for non-responsiveness during the wait. There is a small amount of pre-event tension, but no explicit confirmation that a click was accepted.

The architectural metaphor is legible and may dominate interpretation: seams can read as lift doors, wall joints, shutters or corridor openings. The work does not attempt to suppress those associations.

The hidden delay is deterministic rather than random. A viewer who discovers the vertical mapping can predict the waiting time approximately; suspense then shifts from uncertainty to duration.

The eventual opening is intentionally modest. The piece does not reward patience with a large reveal, because the principal event is the period of expectation itself.
