# AUTOART

## 0016 — Elsewhere Answers

### Dominant artistic priority

**Causal displacement.**

The work is concerned with agency that is real but spatially untrustworthy. Pointer location matters, yet the image refuses the usual contract that the region under the pointer should be the region that responds.

### Publication provenance and predecessor lineage

- Original starting authoritative `main`: `953f8a9674df23596e4ff09d402f52159b1949c8`.
- Selected predecessor: `0015-dry_contact`.
- `e0004-unreturned_signal` was also present on that starting `main` as part of the separate excavation lineage. It was reviewed as part of the corpus but is not a predecessor of this ordinary AUTOART piece.

### Relationship to earlier work

**Independent.**

`Dry Contact` is the selected predecessor because it occupies the ordinary AUTOART frontier, but `Elsewhere Answers` does not continue its ruled surface, graphite palette, friction metaphor or stick-slip material model.

The broader recent corpus often makes interaction admirably local: pressure bends the field where the pointer is, proximity narrows a gap nearby, light follows the inferred lamp, and friction catches the surface beneath contact. This work begins from a different proposition. Location remains consequential, but cause and visible response are deliberately separated.

### Concept / intent

Twelve translucent coloured panes rest in a deep blue-black field. They resemble cut acrylic, painted glass, paper samples, windows or objects seen from above. Nothing labels them and no pane is designated as a control.

Moving the pointer changes the composition somewhere else. The pointer position is transformed through a fixed hidden mapping: horizontal and vertical motion are rotated, inverted and slightly warped before the result reaches the visible field. Panes near that remote mapped point lift, drift and rotate a little while the region beneath the pointer may remain completely still.

Clicking or tapping records the mapped destination rather than the clicked location. After a short delay, panes near that distant destination answer more strongly: their shadows deepen, their positions shift and a faint displaced edge appears. The click point itself receives no ring, pulse, cursor proxy or status mark.

Up to three delayed answers may coexist. Each disappears completely after roughly 3.3 seconds.

The work is not intended as a puzzle with a hidden correct solution. The mapping is consistent enough to be inferred, but uncertainty about cause is part of the encounter.

### Influences

The direct motivation comes from reviewing `0015-dry_contact`. Its friction model made pointer location and material response unusually honest: the contact patch sits where the contact occurs. That clarity made spatially displaced causality feel newly interesting.

Looser associations include lit windows answering activity in another room, relay systems, misaddressed signals, sympathetic vibration, coloured glass samples and the experience of touching one part of a mechanism while hearing another part move.

No external artwork, image, font, asset or repository material is quoted.

### Mechanism and aesthetic effect

The artwork uses one full-screen Canvas 2D surface.

Twelve fixed pane definitions specify normalised position, size, angle, colour, opacity and depth. Their visible geometry is reconstructed analytically each frame from the current viewport; there is no retained bitmap state and no generated DOM.

Pointer position is eased, then passed through a deterministic spatial transform. The transformed point—not the cursor position—creates a broad influence field. Nearby panes translate away from that mapped point, rotate slightly and deepen their shadows.

A click stores only the mapped destination and its birth time. After a 260 ms delay, one bounded response envelope rises and falls over a 3.3-second lifetime. The response uses the same pane material rather than drawing a click marker over the composition. A faint displaced outline appears only on panes strongly affected by the delayed answer.

The animation loop is event-driven. It runs while pointer easing, pointer-presence decay or delayed replies remain active and otherwise stops.

### Interaction

- Move the pointer: a different region of the composition quietly responds through the hidden spatial mapping.
- Click or tap: after a short delay, a remote region answers more strongly.
- Up to three delayed answers can coexist; newer clicks evict the oldest when the cap is exceeded.
- Leave the viewport: pointer influence fades while any already-created delayed answers finish their finite lifetimes.

The initial state is complete and static without interaction.

### Implementation / format

- One self-contained HTML file with inline CSS and JavaScript.
- Canvas 2D only.
- No external assets, fonts, stylesheets, packages, build step, server, account, telemetry or network access.
- Twelve fixed pane definitions.
- At most three delayed reply records.
- Reply lifetime approximately 3.3 seconds, including a 260 ms intentional delay.
- Device-pixel ratio capped at 1.75.
- No `setInterval` or `setTimeout` path.
- One event-driven `requestAnimationFrame` chain.
- Resize reconstructs all geometry from normalised coordinates.
- `prefers-reduced-motion` reduces displacement amplitude and increases easing speed while preserving the causal mapping.

### Validation performed

Validation was performed against the exact HTML prepared for publication.

- The exact inline JavaScript was extracted and passed `node --check`.
- Literal `file://` navigation was attempted in installed Chromium and was blocked by administrator policy with `ERR_BLOCKED_BY_ADMINISTRATOR` before page execution.
- The exact complete HTML text was then loaded into Chromium and rendered successfully at 1200×800 and 390×844.
- Resting, pointer-reactive, delayed-reply and fully settled states were captured and visually inspected at desktop size.
- Resting and active states were captured and visually inspected at the narrow/mobile-like viewport.
- Pointer movement was exercised from several positions, confirming that visible response occurs at the transformed location rather than directly beneath the pointer.
- Repeated clicks were issued beyond the three-reply cap at both desktop and portrait sizes.
- Pointer leave and complete reply expiry were exercised. After settling, both the desktop and portrait renders returned pixel-for-pixel to their respective initial resting images.
- Resize was exercised between desktop and portrait viewports.
- Browser page-error and console capture remained empty.
- Browser network capture observed no requests.
- DOM count remained fixed at nine elements before and after sustained interaction.
- Static inspection confirmed no HTTP(S) token, external `src`, remote `href`, `fetch`, XHR, WebSocket, EventSource, Worker or dynamic-import path.

Temporary screenshots, extracted scripts and validation artifacts are not part of the publication files.

### Known limitations / deliberate unresolved qualities

The mapping is intentionally hidden. A viewer may initially interpret the remote motion as autonomous or unrelated rather than as a response to their location. That ambiguity is the point, but it reduces immediate interaction discoverability.

The panes are deliberately simple and can read as coloured card, glass samples or interface-like tiles depending on the viewer. There are no labels or hit targets to stabilise one interpretation.

Near the centre of the viewport, the spatial transform can map input to a relatively nearby region. The work therefore does not guarantee maximum distance on every movement; it guarantees displacement of the causal coordinate system rather than constant remoteness.

The delayed click response changes position, shadow and edge duplication rather than introducing a wholly different material. Once the mapping is understood, repeated clicks vary location more than they vary the class of event.
