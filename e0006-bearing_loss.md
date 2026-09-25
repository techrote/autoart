# AUTOART excavation line

## e0006 — Bearing Loss

**Excavation-line id:** `e0006`  
**Starting authoritative `main`:** `db70ea9eb0bf98c2989aa34cdef8a7fd45673d3f`  
**Selected predecessor:** `e0005-core_memory`  
**Founding anchor:** `0001-excavation_field`  
**Dominant artistic priority:** material reciprocity  
**Relationship:** derivative excavation-line work that keeps persistent intervention but makes the surrounding material redistribute around the wound

## Relationship to the excavation lineage

`Bearing Loss` is descended directly from `e0005-core_memory` and, through it, from `0001-excavation_field`.

It retains the excavation line's dark cross-sectional field, sparse cyan/amber survey language, slow deterministic activity, layered traces, faulted geometry and materially relevant pointer/click interaction. It also preserves `Core Memory`'s move from transient surveying toward consequential intervention.

The transformation is that the intervention no longer behaves primarily as a record. A click removes material by opening a bounded cavity. Strata bend away from it, moving residue diverts around it, load paths form above and below it, and short fracture filaments emerge as the cut settles. The viewer still changes the section, but the site now visibly reorganises because it has been changed.

## Dominant priority: material reciprocity

The artistic priority for this run is **material reciprocity**: the site should answer intervention rather than merely retain it.

`Core Memory` established persistent consequence through bore scars. Its strongest conceptual limitation is that the ground largely accepts those scars. `Bearing Loss` shifts from sampling to removal. The cavities are visually explicit acts of excavation, but their surrounding response carries as much weight as the void itself.

The result is intended to feel less like a logging instrument and more like a cross-section under changing load: part geological section, part structural diagnostic, part archaeological cut that has begun to alter what it is measuring.

## Concept / intent

The piece presents an already damaged section containing two inherited cuts and a weak oblique fault. Long stratigraphic lines cross the frame while fine stress residue moves through the material.

Pointer movement applies temporary local pressure. It does not draw a reticle; nearby strata and residue deform instead.

Clicking excavates a small irregular elliptical cavity. The cavity opens over several seconds rather than appearing instantaneously. As it opens, neighbouring strata displace, luminous arch-like load paths form around its top and underside, and sparse fractures extend from its edge. These secondary structures strengthen gradually as the cut settles.

At startup, two older cuts are already present so the section feels historically worked rather than pristine. A slow diagonal scan continues across the field regardless of interaction.

## Procedural and temporal systems

- Deterministic seeded construction of a weak oblique fault, stratigraphic family, trace population and inherited cuts.
- Fixed-step bounded trace simulation deposited into one slowly decaying offscreen raster.
- A hidden material-displacement field that combines fault slip, cut-induced displacement and temporary pointer stress.
- Up to six cavity objects, each with deterministic geometry, fractures and settling phase.
- Cavity opening is eased over roughly 150 simulation steps rather than stamped instantly.
- Each cavity generates paired cyan/amber load-path arches whose strength increases as the excavation settles.
- Short fracture filaments extend from cavity edges without growing unboundedly.
- Strata are omitted through excavated interiors and displaced in the surrounding stress field.
- The weak fault remains visible only as a faint dashed discontinuity and as altered motion near its path.
- A slow oblique scan traverses the section continuously.
- The scene is pre-warmed before first display.

## Interaction / perturbation

- **Pointer movement — stress:** applies a temporary local pressure field that displaces nearby strata and redirects moving residue. There is no pointer marker.
- **Click / tap — excavate:** opens one bounded cavity at the selected location. The cut changes subsequent strata, trace and load-path behaviour.
- **Space — hold/resume:** freezes or resumes the section.
- **R — reseed:** creates another deterministic section and clears interaction history.
- **H — interface:** hides/shows the minimal title and control legend.

Cavity state is hard-capped at six. When the cap is exceeded, the oldest cavity is fully removed from both visual and dynamic state before the new one is added, so there is no hidden mismatch between a visible historical scar and a forgotten physical influence.

## Implementation / format

The artwork is one self-contained HTML file using browser-native Canvas 2D with inline CSS and JavaScript. It has no build step, package, sibling asset, external font, CDN, telemetry, account, credential, server or required network access.

Resource use is bounded: at most 640 moving traces, six cavity records, fixed-size strata and fracture structures per cavity, one offscreen residue raster, device-pixel ratio capped at 1.55, and one requestAnimationFrame loop with bounded fixed-step catch-up. No interval or timeout accumulation is used by the artwork.

## Validation actually performed

The exact publication HTML was validated before publication.

- Inline JavaScript was extracted and syntax-checked successfully with Node.
- Static inspection found no HTTP(S) URL, fetch/XHR/WebSocket/EventSource/Worker/dynamic-import path, interval or timeout accumulation path.
- A lightweight DOM/Canvas stub executed the exact script, exercised repeated clicks beyond the cavity cap, pointer motion, pause/resume, interface hiding, reseeding and resize without runtime exceptions.
- The exact HTML document text was loaded into Chromium 144 through the Chrome DevTools Protocol at 1440×900 and 390×844.
- Initial desktop, interacted desktop and narrow/mobile-like states were rendered and visually inspected.
- Pointer stress and nine successive excavations were exercised, exceeding the six-cavity cap.
- `H`, `Space`, `R`, reseeded interaction and resize were exercised.
- Chromium reported no runtime exceptions or log errors during that validation pass.
- The document produced no network/resource requests.
- DOM count remained fixed at 14 elements after sustained interaction and resize.
- The final narrow viewport canvas matched the requested 390×844 viewport exactly.

Literal `file://` navigation was also attempted in the available managed Chromium build. Chromium rejected it with `net::ERR_BLOCKED_BY_ADMINISTRATOR` before document execution. The work itself has no server or network dependency, but direct local-file execution could not be witnessed in this environment because of that administrator policy.

## Known limitations / unresolved qualities

The visual field remains deliberately dark. The cavities and load paths are more legible than the finer residue, but low-contrast displays can still suppress much of the secondary motion.

The load-path arches are intentionally diagrammatic. They communicate structural redistribution clearly, but their symmetry can make some cuts feel more engineered than geological. A future descendant could make secondary response less idealised without losing causal readability.

Removing the oldest cavity immediately when the six-cut cap is exceeded is computationally clean but temporally abrupt at extreme click rates. Under ordinary measured interaction the cap is rarely reached quickly enough for this to dominate the encounter.

The work makes the excavated void explicit again after `e0004` and `e0005` had pushed the lineage toward inference. That is deliberate: the uncertainty has moved from “where is the anomaly?” to “what will the section do after material is removed?”
