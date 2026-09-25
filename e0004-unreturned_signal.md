# AUTOART excavation line

## e0004 — Unreturned Signal

**Excavation-line id:** `e0004`  
**Starting authoritative `main`:** `c671022c66b49d265e3d0906307710856954a099`  
**Selected predecessor:** `e0003-buried_potential`  
**Founding anchor:** `0001-excavation_field`  
**Dominant artistic priority:** material inference without annotation  
**Relationship:** derivative excavation-line work that removes the directly rendered anomaly and makes absence legible through interrupted returns

## Relationship to the excavation lineage

`Unreturned Signal` is explicitly descended from `0001-excavation_field`, `e0002-seam_register`, and `e0003-buried_potential`.

It retains the excavation line's dark low-key field, deterministic procedural substrate, layered survey dialects, persistent trace material, slow measured temporal behaviour and bounded perturbative interaction. The important change is that the central site is no longer drawn as an object, seam, filled cavity or outlined body. Its geometry exists only inside the field equations and attenuation rules. The viewer is asked to locate it from missing or displaced evidence.

`Buried Potential` moved the lineage toward indirect diagnosis but still showed a dark central mass and a pointer-adjacent crosshair/readout. This work removes those explicit declarations. The instrument is present through what the material does, not through a marked target.

## Dominant priority: material inference without annotation

The priority for this run was to make the surveyed substance carry the explanatory burden.

Pointer movement has no reticle, label or numeric readout. It biases the local flow and slightly changes nearby strata, so interaction is visible only as a change in the material field.

Clicking emits a seismic-like impulse made from sparse arrival ticks rather than a clean interface ring. The hidden site interrupts the wavefront. When a front encounters it, bounded secondary echo fragments appear around the suspected region. The site itself is still never outlined.

## Concept / intent

The work imagines a section survey over a region that fails to return energy normally. It might be a chamber, dense inclusion, collapsed structure, buried machine, void, faulted material or a defect in the model rather than in the ground.

The scene begins as an already-running dark section. Stratigraphic lines cross the frame, but some segments bend, phase-slip or disappear around one region. Fine current-like traces accumulate residue while being deflected by the same invisible geometry. Sparse fracture traces and a row of receiver marks provide additional measurement dialects without turning the image into a dashboard.

A slow oblique scan line traverses the field. Nothing points at the hidden site directly. The title refers to the fact that the absence is known by what fails to come back.

## Procedural and temporal systems

- A deterministic seed constructs one hidden irregular elliptical site, strata, sparse fracture traces, receiver positions and the initial trace population.
- A fixed-step bounded trace field leaves persistent current-like residue in one offscreen canvas.
- The hidden site exists inside the flow equations, pushing and shearing trajectories around its boundary.
- Stratigraphic lines are warped and partially dropped out near the same geometry; the dropout is discontinuous enough to suggest missing return rather than a clean mask.
- Eleven short fracture-like traces surround the broader site region with slow phase variation.
- Six to nine small receiver marks establish survey scale without full-height station lines.
- A slow oblique scan crosses the section continuously.
- The scene is pre-warmed before the first displayed frame.
- Click impulses are sparse wavefront samples rather than complete bright circles.
- When an impulse intersects the hidden site, a bounded group of secondary echo arcs is generated and then decays.

## Interaction / perturbation

- **Pointer movement — bias:** locally changes the trace field and slightly perturbs strata near the pointer. There is deliberately no visible pointer marker.
- **Click / tap — impulse:** emits one sparse travelling wavefront whose propagation alters traces and whose interaction with the hidden site can produce delayed echo fragments.
- **Space — hold/resume:** freezes or resumes the survey.
- **R — reseed:** advances to another deterministic hidden section.
- **H — interface:** hides/shows the minimal title/status text.

At most three impulses and twelve secondary echoes may exist at once. Older states are discarded rather than accumulated indefinitely.

## Implementation / format

The artwork is one self-contained HTML file using browser-native Canvas 2D with inline CSS and JavaScript. It requires no build step, package manager, server, external font, asset, CDN, telemetry, account or network access.

Resource use is bounded: trace population is capped at 820, active impulses at three, secondary echoes at twelve, strata/fracture/receiver collections are fixed-size, persistent history lives in one offscreen raster buffer, device-pixel ratio is capped at 1.55, and one requestAnimationFrame loop uses bounded fixed-step catch-up.

## Validation actually performed

The exact publication HTML was validated locally before publication.

- Inline JavaScript was extracted and syntax-checked with Node.
- Literal `file://` navigation was attempted in the available Chromium build and was blocked by administrator policy before execution.
- The exact same HTML text was loaded directly into Chromium and rendered at 1440×900 and 390×844.
- The initial state was visually inspected at both sizes.
- Pointer bias, repeated click impulses beyond the three-impulse cap, pause/resume, interface hide/show and deterministic reseeding were exercised.
- Resize behaviour was exercised between desktop and portrait dimensions.
- Browser page errors and console errors were monitored.
- Network requests were monitored to confirm that the document did not attempt external access.
- DOM count was checked before and after sustained interaction.
- Static inspection confirmed no external `src`/remote `href`, HTTP(S) URL, fetch/XHR/WebSocket/EventSource/Worker/dynamic-import path, timer accumulation or unbounded collection.

## Known limitations / unresolved qualities

The hidden site's position may become learnable after repeated interaction because strata dropout, trace deflection and secondary echoes all converge on the same region. The work aims for inference, not permanent unknowability.

The darkest residue still depends on display calibration. This iteration raises selected strata and echo contrast slightly above `Buried Potential`, but fine traces can remain subtle on low-contrast panels.

The receiver marks are intentionally sparse and small. They may read as decorative calibration ticks rather than actual instrumentation; their role is scale and survey atmosphere rather than direct interaction.

Click impulses are visibly wave-like, even though they are fragmented. A future descendant could abandon circular propagation entirely and explore tomography, directional drilling, excavation cuts or local sampling instead.

This work belongs to the excavation lineage by retaining its core grammar—dark procedural instrumentation, layered traces, a structurally important absent site, deterministic slow motion and bounded perturbative interaction—while moving the anomaly itself completely out of the rendered scene.
