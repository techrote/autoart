# AUTOART

## 0010 — Almost Says

### Dominant artistic priority

**Misrecognition.**

The work is concerned with the moment when perception becomes too confident: a mark, symbol or cluster seems on the verge of being understood as language, but never settles into reliable reading.

### Relationship to earlier work

**Independent.**

`0007`–`0009` form a coherent recent sequence around spatial pressure, colour, proximity and bounded contact. `Almost Says` deliberately leaves that family of field mechanics rather than refining it again.

It keeps only the repository-level requirement that mouse response belong to the artwork rather than appear as application chrome. The governing material is pseudo-writing: invented segmented glyphs, incomplete recognition and the viewer's tendency to read intention into almost-legible marks.

### Concept / intent

A pale field is filled with a bounded grid of invented blue glyphs. At rest they look systematic enough to imply an alphabet, but their segment combinations do not encode a message.

Moving the pointer causes nearby glyphs to become more coherent and letter-like. They approach templates derived from a small alphabet, but ordinary pointer influence never resolves them completely; faint contradictory strokes remain.

Clicking or tapping creates a short recognition wave across the nearest row. For a moment, successive cells approach the repeated sequence `MAYBE`. Each resolved glyph deliberately omits one required stroke, marked by a small vermilion point. The word is therefore available as a perceptual suspicion rather than a clean typographic event.

The central dot does not react. It is a fixed registration point inside a field whose meaning changes according to attention.

### Influences

The immediate influence is the exhaustion of the recent AUTOART sequence around elegant reactive spatial fields. `Courtesy Gap` is relevant mainly because its successful conceptual rule also revealed how quickly a repeated interaction language can become predictable.

Looser associations include seven-segment displays, undeciphered scripts, damaged signage, OCR errors, asemic writing, test patterns and the experience of seeing a familiar word in accidental marks.

No external artwork, font, asset or repository material is quoted.

### Mechanism and aesthetic effect

The artwork uses one full-screen Canvas 2D surface.

Each glyph is assembled from a fixed vocabulary of thirteen possible line segments. Every cell has a deterministic base mask and a separate letter-like target mask. Pointer proximity interpolates segment opacity toward the target while reducing authored tilt and jitter, so recognition is produced by the same marks becoming more internally consistent rather than by drawing text on top.

Click pulses select the nearest row and sweep across it. The target sequence is `MAYBE`, but one required segment is suppressed in each affected glyph. A small vermilion point marks the location of that withheld segment while the pulse is strong.

The grid size adapts within hard bounds to viewport size. The animation loop is event-driven: it runs while pointer easing or recognition pulses are active and otherwise stops.

### Interaction

- Move the pointer: nearby glyphs become more letter-like without fully resolving.
- Click or tap: send a brief word-like recognition wave through the nearest row.
- Leave the viewport: local coherence fades and the field returns to its invented script.

The default state is complete without interaction.

### Implementation / format

- One self-contained HTML file with inline CSS and JavaScript.
- Canvas 2D only; no external font, asset, package, server, account, telemetry or network request.
- Thirteen fixed segment primitives and a bounded adaptive grid of 7–16 columns by 5–10 rows.
- Click pulses are hard-capped at three and expire after approximately 2.6 seconds.
- Device-pixel ratio is capped at 1.8.
- No retained frame history, generated DOM tree or unbounded array.
- The requestAnimationFrame chain becomes idle after pointer easing and click pulses settle.
- Resize rebuilds the deterministic bounded grid for the new viewport.

### Validation performed

The exact HTML prepared for publication was validated with the strongest checks available in this execution environment:

- the inline JavaScript was extracted and passed `node --check`;
- a mocked browser/Canvas runtime executed the exact script through startup, pointer movement, repeated clicking beyond the three-pulse cap, pointer leave, animation-frame progression and resize without runtime exceptions;
- the mock confirmed one animation-frame chain at a time and fixed document structure;
- static inspection found no external `src`/remote `href`, no `http://` or `https://`, and no `fetch`, XMLHttpRequest, WebSocket, EventSource, Worker or dynamic import path;
- source inspection confirms bounded grid dimensions, three-pulse cap, finite pulse lifetime and capped device-pixel ratio;
- Chromium rendering was attempted on both this work and a trivial local test page, but the installed browser currently stalls during graphics/compositor initialisation in both headless and Xvfb modes, so no successful browser render or console claim is made for this run.

### Known limitations / deliberate unresolved qualities

The work depends on Latin-letter familiarity for the click-wave misrecognition to operate as intended. A viewer who does not recognise the implied templates may experience the piece primarily as changing geometric notation.

On narrow screens the adaptive grid uses fewer columns, so the repeated `MAYBE` rhythm is shorter and more immediately repetitive. That is preferable to shrinking glyphs into unreadable noise.

The deliberate missing-stroke dots may make the click state slightly more explanatory than the resting field. Their role is to mark absence without printing a literal correction.
