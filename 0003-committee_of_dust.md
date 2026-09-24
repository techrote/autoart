# AUTOART

## 0003 — Committee of Dust

### Dominant artistic priority

**Comic timing.**

The criterion for this run was not visual novelty or technical complexity, but whether a very small sequence of delays, arrivals and reactions could make an abstract arrangement behave like a social situation.

### Relationship to earlier work

**Oppositional.**

`0001-excavation_field` is dark, technically dense and forensic. `0002-held_breath` answers it with pale stillness and near-ceremonial restraint. Both are serious, controlled works. `Committee of Dust` deliberately opposes that accumulated solemnity without abandoning formal care.

The new piece uses a brighter palette, recognizable group behaviour and a recurring minor embarrassment: one participant is conspicuously late and everyone else has to make room.

### Concept / intent

Twenty-two small capsule-like delegates sit around an oval table with one vacant position. A coral delegate waits awkwardly outside the meeting.

For much of each cycle, almost nothing important happens. Then the late delegate approaches the gap. Nearby delegates recoil and shuffle just enough to register discomfort; the central punctuation briefly changes from an indecisive ellipsis to an exclamation mark. The visitor stays for a moment, then leaves and the committee resumes its imperfect equilibrium.

The figures have no faces, names or dialogue. The humour depends on timing, spacing and the viewer's tendency to project social intention onto small geometric movements.

The title treats the delegates as both a bureaucracy and insignificant matter: a committee made from dust, solemnly rearranging itself around an agenda whose content never arrives.

### Mechanism and aesthetic effect

The visible work is a fixed inline SVG. Twenty-two ordinary delegates and one late delegate are authored directly into the document; no nodes are generated during animation.

A single `requestAnimationFrame` loop runs an 18-second choreography. The late delegate spends the first part of the cycle outside the meeting, enters over two seconds, remains briefly, and departs. Its arrival produces a short radial/angular “flinch” in nearby delegates. The response falls off with seat distance, so the social disturbance is local rather than a whole-scene effect.

Small independent idle offsets keep the seated delegates from becoming perfectly mechanical. The central punctuation is the only textual event: `· · ·` becomes `!` near the moment of arrival.

The palette and paper-like SVG filters keep the piece graphic rather than interface-like. There are no controls, labels or visible status indicators.

### Interaction

Press and hold anywhere to **call the meeting to order**.

The pressure value eases toward a fully ordered state: the late delegate takes the empty chair immediately, the other delegates stop their social recoil/idle drift, and the centre punctuation contracts to a single bullet. Release and the committee gradually returns to its autonomous awkwardness.

The interaction is optional. The initial composition and timed event are complete without configuration.

When the operating system requests reduced motion, the autonomous 18-second choreography is held at its initial state. The press-and-hold ordering interaction remains available.

### Validation performed

The exact HTML intended for publication received the strongest validation available in this execution environment.

- The inline JavaScript extracted from the exact HTML passed `node --check`.
- The exact inline SVG was rasterized successfully with Inkscape at 1200×800 and visually inspected. The initial state clearly shows the oval table, the vacant seat and the coral late delegate outside the ring.
- The `preserveAspectRatio="xMidYMid meet"` behaviour was simulated at a 390×844 mobile-like viewport and visually inspected. The full composition remains present; the deliberate consequence is substantial vertical letterboxing rather than cropped delegates.
- The animation script was executed in a minimal mocked DOM/RAF environment. Tests exercised the idle state, entry, impact, arrived state, press-and-hold ordering and release. The late delegate moved through the expected positions, nearby delegates changed transforms at impact, punctuation changed to `!` and then `•` under ordering, and the requestAnimationFrame queue remained exactly one callback deep.
- A 10,000-frame mocked run completed with the same fixed 22 regular delegate objects plus one late delegate and one queued animation callback; no arrays, DOM nodes or timers accumulated per frame.
- Static HTML inspection found 98 document elements, 22 fixed `.delegate` nodes plus one fixed `#late` node, no external `src`/`href` references, and no `http://`, `https://`, `fetch`, XMLHttpRequest, WebSocket, EventSource, Worker or dynamic-import path.

Faithful browser execution was not available: the installed managed Chromium rejects `file://`, `data:` and localhost navigation by administrator policy. I therefore do not claim browser-console or real pointer-event validation that did not occur. The absence of browser execution is an environment limitation; the file itself has no server or network dependency.

### Known limitations / deliberate unresolved qualities

On tall narrow screens, preserving the complete meeting through `meet` makes the artwork physically smaller and leaves broad background above and below. This was preferred to cropping the late delegate or reflowing the composition into a different mobile artwork.

The social reading is intentionally fragile. A viewer may see coloured capsules orbiting an ellipse and nothing more. The piece does not add labels or faces to force the joke; it relies on timing and displacement to carry the anthropomorphism.
