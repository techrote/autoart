# AUTOART excavation line

## e0003 — Buried Potential

**Excavation-line id:** `e0003`  
**Starting authoritative `main`:** `26fae36b9f28cb3af5a47d5f1fbf0a95146101e9`  
**Selected predecessor:** `e0002-seam_register`  
**Founding anchor:** `0001-excavation_field`  
**Dominant artistic priority:** inference through disturbance  
**Relationship:** derivative lineage work that shifts from mapping a visible fault to inferring a buried resistive body

## Relationship to the excavation lineage

`Buried Potential` belongs explicitly to the excavation line. It preserves the dark procedural field, sparse luminous traces, layered survey dialects, deterministic slow motion, bounded intervention and structurally important absence established by `0001-excavation_field` and refined by `e0002-seam_register`.

The main change is epistemic. `Excavation Field` presents an excavated void directly. `Seam Register` presents a visible fault seam and measures the displacement around it. `Buried Potential` makes its anomaly less available: a buried resistive body is mostly inferred from bent strata, current-trace avoidance, offset echo contours, station readings and cross-sections. The instrument knows the surrounding field better than it knows the object.

## Dominant priority: inference through disturbance

The central artistic priority for this run was to make intervention change the evidence rather than merely annotate it.

Pointer movement acts as a temporary current-injection probe. It enters the same vector field that moves the persistent current traces, bending nearby trajectories and briefly increasing local instability. Clicking plants a bounded temporary electrode pulse. Its expanding potential front changes the same field and therefore redirects simulated material as it crosses the survey.

There is still a small probe crosshair and resistivity-style readout, but they are intentionally faint. The main response should be found in the trajectories and the way measurement marks around the buried body become disturbed.

## Concept / intent

The piece imagines a subsurface electrical-resistivity survey over something that refuses to resolve into a clean object: perhaps a collapsed chamber, a buried machine casing, a mineral body, a tomb, a void filled with different material, or simply a computational lesion in an otherwise continuous field.

The anomaly is not a bright specimen. It is a dark resistance around which current trajectories bend and from which stratigraphic and contour evidence mis-registers. Survey stations descend through the field, slow cross-sections pass through the suspected region, sparse residual marks accumulate and a very slow scan traverses the surface.

The mood is intended to be one of patient technical suspicion: the system has enough evidence to know something is present, but not enough to say what it is.

## Procedural and temporal systems

- A deterministic seed constructs the buried anomaly, stratigraphic family, station positions and initial current-trace population.
- A fixed-step bounded particle field produces persistent current-like residue in one offscreen raster buffer.
- The buried body is part of the flow equations: traces are pushed away from its interior and bent along its shell.
- Stratigraphic lines are locally warped around the anomaly rather than merely drawn behind it.
- A sparse potential mesh bends around the same region and drifts slowly through dashed phase offsets.
- Survey stations carry independently phased depth indicators.
- Five cross-sections and small deterministic sample ticks provide another measurement dialect without becoming a dashboard.
- Six irregular echo contours surround the buried body with slow phase drift.
- A slow horizontal scan passes across the field.
- The simulation is pre-warmed before the first displayed frame, so the work opens as an already-running survey.

## Interaction / perturbation

- **Pointer movement — inject:** a temporary local current source alters the vector field and bends nearby current traces.
- **Click / tap — electrode:** emits one expanding potential pulse that both appears faintly and materially pushes trajectories near its moving front.
- **Space — hold/resume:** freezes and resumes the survey.
- **R — reseed:** advances to another deterministic buried site.
- **H — interface:** hides/shows the minimal status text.

Electrode state is hard-capped at four simultaneous pulses. Older pulses are discarded rather than accumulated indefinitely.

## Implementation / format

The work is one self-contained HTML file using browser-native Canvas 2D plus inline CSS and JavaScript. It requires no build step, package, server, external asset, font, CDN, account, telemetry or network access.

Resource use is bounded: current traces are capped at 920 particles, electrode pulses at four, survey/strata/echo collections are fixed-size, persistent history is held in one offscreen canvas, device-pixel ratio is capped at 1.55, and one `requestAnimationFrame` loop uses bounded fixed-step catch-up.

## Validation actually performed

Validation was performed against the exact HTML prepared for publication.

- Inline JavaScript was syntax-checked successfully with Node.
- Direct `file://` navigation was attempted in installed Chromium and was blocked by administrator policy before page execution.
- The exact same complete HTML text was then loaded directly into Chromium and rendered successfully at 1440×900 and 390×844.
- The initial dark survey state was visually inspected at both sizes.
- Pointer injection, repeated click/electrode pulses, pause/resume, interface hide/show and deterministic reseeding were exercised.
- Resize behaviour was exercised when switching from desktop to the narrow viewport; the canvas remained exactly viewport-sized.
- No page errors or console errors were observed.
- No network requests or performance resource loads were observed.
- DOM count remained fixed at 14 elements during interaction and a multi-second runtime sanity pass.
- Static inspection found no external URL, remote asset or network API requirement.
- Source inspection confirms bounded particle count, four-electrode cap, finite pulse decay, capped DPR and no timer/DOM accumulation path.

The inability to navigate the exact file with `file://` is an environment limitation rather than a server requirement, but it remains a validation limitation and is not described as a successful direct-local-file test.

## Known limitations / unresolved qualities

The work is deliberately very dark. The finest potential mesh and residue marks are near the threshold of visibility on low-contrast displays. This supports the sense of partial evidence, but display calibration materially affects how much structure is available.

The buried body's dark central mass is still visible enough that the viewer does not have to infer its location entirely from surrounding distortions. The piece moves farther toward indirect diagnosis than `Seam Register`, but does not eliminate direct silhouette altogether.

The pointer crosshair and `ρ` readout remain a small explicit instrument layer. They are quieter than the material response, but a later descendant could remove the probe marker entirely and make intervention legible only through the field.

The survey stations span the whole frame evenly, so the composition retains some instrument-grid regularity. A future excavation-line work could let measurement density itself become adaptive or damaged without turning into uncontrolled visual noise.