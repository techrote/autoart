# AUTOART

## 0015 — Dry Contact

### Dominant artistic priority

**Friction.**

The work is concerned with resistance rather than smooth responsiveness. Interaction should feel as though the image catches, drags and briefly retains local strain instead of following the pointer with perfectly elastic obedience.

### Publication provenance and predecessor lineage

- Original starting authoritative `main`: `c671022c66b49d265e3d0906307710856954a099`.
- Selected predecessor: `0014-held_on_a_technicality`.
- The active excavation-line branch `art/e0004-unreturned_signal` was observed as separate concurrent work; it contains only the unpublished `e0003` critique at this starting point and is not part of this piece's lineage.

### Relationship to earlier work

**Independent.**

`Held on a Technicality` is the selected predecessor because it occupies the current ordinary frontier, but `Dry Contact` does not extend its mobile, palette, suspension metaphor or reversible slip mechanism.

The review of `0014` made clean recovery newly conspicuous, but this work begins from a broader corpus-level observation: AUTOART has become very competent at elegant, bounded, smoothly easing interaction. `Dry Contact` keeps the discipline of bounded state while deliberately making the visible response less polite. The governing material is a dry ruled surface that appears to snag rather than glide.

### Concept / intent

Fifty-eight graphite-like horizontal strokes cover a warm grey-beige surface. Their spacing is regular enough to suggest ruled paper, woven fibres, machining passes or repeated abrasion, but each line carries small deterministic roughness. One saturated blue strand interrupts the mostly neutral field without functioning as a control or target.

Moving the pointer creates an invisible patch of drag. Nearby strokes bunch, kink and shear, but the response does not continuously track every pixel. The internal contact point sticks until enough horizontal difference accumulates, then releases most of that difference at once. The visible result is a local patch of broken rhythm rather than a soft lens or cursor halo.

Clicking or tapping plants a temporary snag. Nearby lines remain displaced and a bounded scatter of dry crumbs appears around the contact. A snag holds at full strength for several seconds, then releases nonlinearly. Up to five can coexist; additional clicks discard the oldest state rather than accumulating indefinitely.

When interaction and snag memory finish, the field returns exactly to its authored resting image.

### Influences

The direct AUTOART lineage is intentionally weak. `The Weight of Looking` demonstrated that a whole field can respond to an invisible pointer without application chrome, but its material is elastic and smooth. `Dry Contact` changes that physical intuition to catch-and-release.

Loose associations include graphite rubbed across rough paper, drypoint burrs, worn drafting sheets, abrasive belts, combed fibres, pressure-sensitive copying paper and a record needle briefly mistracking across a groove.

No external artwork, font, image, repository asset or library is quoted.

### Mechanism and aesthetic effect

The artwork uses one full-screen Canvas 2D surface.

The fifty-eight resting strokes are analytical and deterministic. Each is sampled across the viewport with small seeded roughness and two shallow sinusoidal deviations. One fixed row is drawn in ultramarine blue; the rest use varied low-opacity charcoal.

Pointer state is intentionally not ordinary interpolation. Vertical position eases smoothly, but horizontal position uses a small stick threshold: the internal contact point remains still while the gap to the target is small, then releases most of the accumulated difference once the gap exceeds that threshold. The displacement field around that point adds short, tooth-like kinks to nearby strokes.

Click snags are finite records containing position, direction and one deterministic variation value. They affect the same stroke geometry rather than drawing a separate circular indicator. Eighteen tiny crumb marks per active snag are generated analytically each frame from the snag record; they are not retained objects and cannot accumulate beyond the five-snag cap.

The animation loop is event-driven. It runs while pointer state is settling or any snag remains alive, and otherwise stops.

### Interaction

- Move the pointer: drag a local patch of the surface; nearby lines stick and then release into a kinked shear.
- Click or tap: leave one temporary snag that holds nearby strokes out of register.
- Up to five snags can coexist; newer clicks evict the oldest when the cap is exceeded.
- Leave the viewport: live pointer pressure fades; existing snags continue their finite release.

The initial state is complete and static without interaction.

### Implementation / format

- One self-contained HTML file with inline CSS and JavaScript.
- Canvas 2D only.
- No external assets, fonts, stylesheets, packages, build step, server, account, telemetry or network access.
- Fifty-eight fixed conceptual rows.
- At most five temporary snag records.
- Snag lifetime: approximately 6.2 seconds, with a long hold followed by a quadratic release.
- Eighteen analytically generated crumbs per active snag; no retained crumb arrays.
- Device-pixel ratio capped at 1.75.
- No `setInterval` or `setTimeout` path.
- One event-driven `requestAnimationFrame` chain.
- Resize reconstructs the surface analytically for the new viewport rather than scaling retained pixels.
- `prefers-reduced-motion` shortens the response time but preserves the interaction language.

### Validation performed

Validation was performed against the exact HTML prepared for publication.

- The exact inline JavaScript was extracted and passed `node --check`.
- Literal `file://` navigation was attempted in installed Chromium and was blocked by administrator policy with `ERR_BLOCKED_BY_ADMINISTRATOR` before page execution.
- The exact complete HTML text was then loaded into Chromium and rendered successfully at 1200×800 and 390×844.
- Resting, pointer-deformed, multi-snag and fully settled states were captured and visually inspected at both viewport sizes.
- Pointer movement was exercised across several regions.
- Nine clicks were issued in each viewport to exceed the five-snag cap deliberately; the document remained stable and no DOM growth occurred.
- Pointer leave and full snag expiry were exercised. After 6.5 seconds, the settled desktop and portrait screenshots were byte-for-byte identical to their respective initial resting screenshots.
- Resize was exercised after interaction; the backing canvas and CSS size both tracked the new viewport dimensions.
- Browser page-error and console capture remained empty at both viewport sizes.
- Browser network capture observed no requests.
- DOM count remained fixed at nine elements before interaction, after repeated clicking and after complete settling.
- Static inspection found no HTTP(S) token, external `src`, remote `href`, `fetch`, XHR, WebSocket, EventSource, Worker or dynamic-import path.
- Static inspection also confirmed the five-snag hard cap, 6.2-second snag lifetime and absence of timer APIs.

Temporary screenshots, extracted scripts and validation artifacts are not part of the publication files.

### Known limitations / deliberate unresolved qualities

The resting image is intentionally close to ruled material and may initially look plain. The blue line supplies one chromatic interruption, but the main visual event only becomes apparent when the pointer creates local drag.

The horizontal stick threshold means very small pointer motions may produce no new horizontal response. This is intentional friction, but a viewer expecting exact cursor following may interpret it as latency.

The click crumbs are visually subordinate and can be difficult to see on low-contrast displays. They are meant to read as dry residue rather than particle spectacle.

On narrow portrait screens the same fifty-eight-row count creates much denser vertical spacing. This changes the piece toward fabric or hair-like texture rather than simplifying the composition for mobile.
