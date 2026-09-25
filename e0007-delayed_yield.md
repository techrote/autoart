# AUTOART excavation line

## e0007 — Delayed Yield

**Excavation-line id:** `e0007`  
**Starting authoritative `main`:** `d3e0979b8c55a8904a57bd5308a29d7287edabae`  
**Selected predecessor:** `e0006-bearing_loss`  
**Founding anchor:** `0001-excavation_field`  
**Dominant artistic priority:** delayed causality  
**Relationship:** derivative excavation-line work that keeps material reciprocity while separating intervention from the time and place of visible yield

## Relationship to the excavation lineage

`Delayed Yield` continues the near-black diagnostic field, sparse cyan/amber traces, slow deterministic activity, damaged cross-section and bounded perturbative interaction established by `0001-excavation_field` and developed through the e-series. It responds directly to `e0006-bearing_loss`.

`Bearing Loss` made the section reorganise around a viewer-created cavity, but cause and consequence remained tightly paired. Here a click does not cut geometry. It adds load to an already weak buried shear zone. Stress migrates through fixed segments, crosses deterministic local thresholds, waits through a latent interval, and may then produce slip elsewhere. Persistent offsets alter strata and trace motion after the viewer's initiating gesture has passed.

## Dominant priority: delayed causality

The priority is **delayed causality**: interaction should matter materially without behaving like a command whose result appears immediately under the pointer.

The viewer can bias and load the section, but the weak structure decides when and where a bounded yield event occurs. This is not intended as geomechanical simulation. It is a controlled procedural fiction that makes consequence temporally uncertain while keeping it legible.

## Concept and procedural systems

The scene is a dark cross-section crossed by a buried oblique shear zone. The zone is not rendered as a solid body; it is inferred from sparse dashed evidence, local strata dropout, trace behaviour and one inherited slip region present at startup.

Major systems are:

- deterministic seeded construction of a 25-segment weak zone, strata and trace population;
- fixed-step particle motion with bounded lifetime;
- per-segment stress, yield thresholds, cooldowns and deterministic latent delays;
- persistent slip offsets that deform nearby strata and alter trace flow;
- bounded neighbour stress transfer after yield;
- finite-lived fracture-like aftertraces;
- up to four quiet expanding load fronts;
- a slow diagnostic scan across the section.

## Interaction

- **Pointer movement — bias:** temporarily curls nearby trace motion and adds a small stress bias to the nearest weak-zone segment. No cursor marker is drawn.
- **Click / tap — load:** injects one bounded load pulse. Stress can migrate before a delayed slip occurs.
- **Space — hold/resume:** freezes or resumes the section.
- **R — reseed:** creates a new deterministic stressed section and clears interaction history.
- **H — interface:** hides or shows the minimal title/control text.

Interaction is bounded: at most four load pulses and 24 finite-lived aftertraces coexist; the weak zone has 25 fixed segments and trace count is capped at 460.

## Implementation / format

The artwork is one self-contained HTML file using inline CSS/JavaScript and browser-native Canvas 2D. It requires no build step, package, sibling asset, remote font, CDN, account, telemetry, credential, server or network access. Device-pixel ratio is capped at 1.5, simulation catch-up is bounded, and the work uses one `requestAnimationFrame` loop with no interval or timeout API.

## Validation actually performed

Validation was performed against the exact publication HTML prepared for this run.

- Inline JavaScript was extracted and passed `node --check`.
- Static inspection found no HTTP(S) URL, external resource reference, fetch/XHR/WebSocket path, interval or timeout path.
- A DOM/Canvas execution harness ran the exact script with browser-like event targets and a bounded animation-frame queue.
- The harness exercised pointer movement, eight successive click/load inputs (beyond the four-load cap), pause/resume, interface hiding, deterministic reseeding and resize from 1440×900 to a 390×844 CSS-pixel viewport.
- It observed the intended intermediate states `stress migrating` and `latent slip queued`, followed by `yield registered`, confirming that visible structural response can occur after initiating input.
- After reseed the status returned to a clean listening state; resize completed without exception; the animation queue remained at one callback rather than accumulating.
- Installed Chromium was also invoked on the exact local file, but the headless browser hung in this execution environment and produced no screenshot before timeout. A trivial local document behaved similarly, so no fresh raster/visual-browser claim is made for this run.

The strongest available validation therefore covers syntax, state progression, all documented controls, bounded interaction, resize logic and absence of network dependencies, but not fresh pixel-level inspection of the final compact publication file.

## Known limitations / unresolved qualities

The weak zone is deliberately simplified. Its threshold and neighbour-transfer rules create structural plausibility and temporal uncertainty, not engineering accuracy.

After several slips the fault path becomes easier to infer because dropout, offsets and aftertraces begin to agree spatially. That is treated as accumulated evidence rather than a concealment failure.

Heavy repeated interaction can brighten the section and cause related slips, although load, aftertrace and transfer counts remain hard-bounded. The inherited slip gives the opening state useful differentiation, but it also supplies an early clue to the weak zone's approximate path.
