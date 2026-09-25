# AUTOART

## 0014 — Held on a Technicality

### Dominant artistic priority

**Fragility.**

The work is interested in structures that look calm only because very small connections are continuing to do their job. The aim is not catastrophe. It is the low-grade awareness that a stable arrangement may be depending on joints much smaller than the things they hold.

### Publication provenance and predecessor lineage

- Original starting authoritative `main`: `9b74b1e9025c7f6c084361aae414e4a00f80da0a`.
- Selected predecessor: `0013-counterweight`.
- The recovered historical sibling `0002a-mended_weather` was reviewed as part of the corpus but is not a direct predecessor of this work.

`0013-counterweight` is already published on `main`; the surviving `art/0013-counterweight-publish` branch is historical and has no commits ahead of `main`.

### Relationship to earlier work

**Hybrid.**

`Counterweight` supplies the immediate concern with balance, visual mass and a small element carrying disproportionate responsibility. This work keeps that concern but changes the structure completely. Instead of a left/right visual equation connected by a faint thread, the image is a narrow hanging mobile whose apparent coherence depends on a handful of tiny joints.

The work also rejects `Counterweight`'s temporary duplication of mass. When something goes wrong here, nothing new is created. One existing connection simply slips out of alignment for a while.

### Concept / intent

A spare kinetic mobile hangs in a large warm field.

Seven muted coloured weights are carried by hairline rods. The largest shapes are not especially heavy-looking, but the joints holding them are tiny circles and short thread segments. The whole object therefore reads as composed and slightly implausible at the same time.

Pointer position behaves like weak moving air. It does not select or drag anything. The top bar, side branches and central drop rotate by different small amounts, so the mobile becomes more or less balanced depending on where the viewer is.

Clicking or tapping briefly lets one part of the structure slip. A left, centre, right or top joint is chosen from the click region; the corresponding assembly sags a few pixels away from its seat and rotates before slowly returning. The gap is intentionally small. The piece is about the possibility of failure more than a spectacle of failure.

There is no score, cursor proxy, status marker or permanent damage.

### Influences

The direct AUTOART influence is `0013-counterweight`, specifically the intuition that a tiny mark can carry more structural meaning than its size suggests.

Looser associations include Calder-like mobiles, improvised hanging repairs, fishing swivels, model-making wire, suspended samples, and the moment when a hook looks a little too small for what is hanging from it.

No external artwork, asset, font or repository material is quoted.

### Mechanism and aesthetic effect

The visible work is a fixed inline SVG. Its geometry is authored rather than procedurally generated: rods, seven coloured weights, small joints and three near-invisible registration specks.

JavaScript changes only four group transforms:

- the top assembly;
- the left branch;
- the right branch;
- the centre drop.

Pointer position supplies two bounded values—horizontal wind and vertical lift—which ease into small rotations. Clicking creates one replaceable `slip` state with a 4.6-second lifetime. During a slip, one group gains a small vertical offset plus a few degrees of rotation, visibly separating it from the short connector above it.

The animation loop is event-driven and becomes idle after pointer easing and slip recovery finish.

### Interaction

- Move the pointer: introduce a weak breeze through the mobile.
- Click or tap: briefly let one nearby structural region slip and sag.
- Click again during a slip: replace the current slip rather than accumulate failures.
- Leave the viewport: the mobile gradually returns to its authored resting balance.

The initial state is complete and static without interaction.

### Implementation / format

- One self-contained HTML file.
- Inline CSS, SVG and JavaScript only.
- No external assets, fonts, stylesheets, packages, build step, server, account, telemetry or network access.
- Fixed SVG document structure; no runtime node creation.
- Seven fixed visible weights.
- At most one temporary slip state.
- Slip lifetime approximately 4.6 seconds.
- One event-driven `requestAnimationFrame` chain.
- `prefers-reduced-motion` makes easing faster without removing the pointer/click relationship.
- `preserveAspectRatio="xMidYMid slice"` keeps the narrow vertical mobile at material scale on portrait screens while the wide desktop state retains large empty side fields.

### Validation performed

The exact publication candidate was validated with the strongest available checks in this execution environment:

- HTML parsed successfully;
- the extracted inline JavaScript passed `node --check`;
- the inline SVG, with its script removed for static rasterisation, parsed and rasterised successfully with Inkscape at 1200×800;
- the same authored SVG was rasterised in a 390×844 portrait frame using its `xMidYMid slice` behaviour and visually inspected;
- a minimal mocked SVG/DOM/requestAnimationFrame runtime executed the exact script through startup, pointer movement, clicks in left/centre/right/top regions, click replacement, pointer leave, slip expiry and resize without exceptions;
- the mock confirmed a single animation-frame chain, one replaceable slip state, bounded scalar pointer state and return to idle;
- static scanning found no external `src`, remote `href`, HTTP(S) URL, `fetch`, XHR, WebSocket, EventSource, Worker or dynamic-import path;
- a fresh direct Chromium attempt was made in this run, but the installed Chromium stalled during graphics/compositor initialisation even for a trivial control page. No live-browser render, console or real pointer-event claim is therefore made.

Temporary validation artifacts were not included in the repository.

### Known limitations / deliberate unresolved qualities

The mobile metaphor is readily legible. The work relies on the scale mismatch between tiny joints and larger suspended forms rather than on conceptual ambiguity.

On very narrow portrait screens, `slice` intentionally crops most of the empty side field so the central mobile retains useful physical scale. The composition therefore changes from "small object in a large room" toward "close view of a narrow object."

The click mapping is spatial rather than object-perfect: broad screen regions choose which assembly slips. This avoids visible hit targets, but a click near a visual boundary may affect a neighbouring branch rather than the exact shape the viewer had in mind.
