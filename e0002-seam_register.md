# AUTOART excavation line

## e0002 — Seam Register

**Excavation-line id:** `e0002`  
**Dominant artistic priority:** responsive material causality  
**Relationship:** derivative lineage work, with a deliberate spatial shift from a central cavity to a traversing fault seam

## Relationship to `0001-excavation_field`

`Seam Register` is explicitly a descendant of `0001-excavation_field`. It keeps the founding work's dark instrument-like field, deterministic procedural substrate, layered survey traces, slow temporal behaviour, sparse luminous colour and the idea that interaction should perturb an autonomous process rather than operate a conventional application UI.

The central formal change is the anomaly. `Excavation Field` organized multiple systems around an excavated elliptical absence. `Seam Register` replaces that object-like void with a narrow, irregular vertical fault: a missing or inaccessible boundary that cuts through the whole field. The surrounding systems behave as if they are trying to characterize displacement across it rather than simply orbit or outline it.

There is no earlier e-series piece, so `0001-excavation_field` is the sole predecessor for this first branch of the excavation lineage.

## Concept / intent

The work imagines a damaged subsurface being inspected by an instrument that never obtains a complete image. Stratigraphic lines continue across the frame but shift across the seam. Boreholes descend through the field and report tiny core-log marks. Dashed offset contours bracket the fault. Sparse residual ticks and moving material traces imply measurements that accumulate without resolving the central discontinuity.

The intended mood is patient technical attention directed at something structurally absent: less a map of a known object than a register of how surrounding matter reacts to a break that cannot itself be measured directly.

## Procedural and temporal systems

- A deterministic seeded generator constructs the fault geometry, stratigraphic wave family, borehole positions, core-log marks and initial trace population.
- A fixed-step simulation advances a bounded population of motes through a slowly changing vector field.
- The fault is not decorative masking alone: the vector field pushes trajectories away from it and biases motion along its local tangent.
- Persistent trace deposition forms restrained residue around the seam while the trail buffer slowly decays.
- Offset contour families track the seam on both sides with slow dashed motion.
- Boreholes carry independently phased depth markers and deterministic core-log ticks.
- Cross-seam transects and sparse residual markers provide a second measurement dialect without becoming a dashboard.
- A very slow vertical scan traverses the field continuously.
- The scene is pre-warmed so it opens as an already operating survey rather than a blank initialization state.

## Interaction / perturbation

Pointer movement acts as a temporary **probe coupling**. Near the pointer, the local flow field gains a rotating and slightly inward bias, so nearby traces bend rather than merely lighting up. A faint reticle reports approximate distance to the seam and decays when the pointer stops moving.

Clicking emits a bounded **core pulse**. The pulse expands through the field as a visible survey ring and also pushes simulated material outward near the moving ring front. At most five pulses may coexist; older pulses are discarded, so repeated interaction cannot create unbounded history.

Keyboard controls are intentionally small:

- `Space` — hold/resume the survey
- `R` — advance to another deterministic seed
- `H` — hide/show the minimal textual overlay

## Implementation / format

The artwork is one self-contained HTML file using inline CSS and JavaScript plus browser-native Canvas 2D. It has no build step, package dependency, sibling asset, CDN, telemetry or network requirement.

Resource growth is bounded: the trace population is capped at 1,050 elements, simultaneous pulses at five, procedural line/measurement collections are fixed-size, the persistent trail history is rasterized into one offscreen canvas, DPR is capped at 1.55, and the animation uses one requestAnimationFrame loop with bounded fixed-step catch-up.

## Validation actually performed

Validation was performed against the exact HTML prepared for publication using headless Chromium.

- Rendered successfully at a 1440×900 desktop viewport and a 390×844 narrow/mobile-like viewport.
- Verified the intended dark initial survey state and responsive full-viewport canvas sizing.
- Exercised pointer movement, click/core-pulse interaction, pause/resume, interface hide/show and deterministic reseeding.
- Observed no JavaScript page errors and no console errors during those runs.
- Observed no network requests or performance resource loads; static inspection also found no external `src`, `href`, `http://` or `https://` dependency.
- Performed an additional 15-second headless runtime sanity pass; DOM/node counts remained effectively flat and the implementation contains no interval/timeout accumulation path.
- Inspected rendered desktop and narrow screenshots for composition and legibility.

The execution sandbox blocks direct `file://` navigation by administrator policy, so the local-file opening path could not be exercised literally. The exact same HTML text was instead loaded directly into Chromium with no external resources. The document contains no mechanism that depends on HTTP/server context, but this is still a validation limitation rather than a claimed direct-file test.

## Known limitations / unresolved qualities

The piece is intentionally very dark. On low-contrast or brightly lit displays, the quiet contour families and residual material traces may approach the threshold of visibility; that fragility is partly deliberate, but it makes display calibration consequential.

The seam remains a strong central silhouette and can dominate narrower portrait viewports. The mobile layout was checked and remains coherent, but the work does not attempt to equalize the anomaly's visual weight across aspect ratios.

The probe changes the actual trace dynamics, yet the most legible interactive response is still the reticle and expanding pulse ring. A later descendant could push the material consequences of probing further while retaining the excavation line's measured pace.

This work belongs to the excavation lineage by retaining `0001`'s core grammar—dark procedural instrumentation, layered traces, a structurally important absence, deterministic slow motion and bounded perturbative interaction—while changing the survey problem from an excavated body to a fault that divides the field.
