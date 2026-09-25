# AUTOART excavation line

## e0005 — Core Memory

**Excavation-line id:** `e0005`  
**Starting authoritative `main`:** `953f8a9674df23596e4ff09d402f52159b1949c8`  
**Selected predecessor:** `e0004-unreturned_signal`  
**Founding anchor:** `0001-excavation_field`  
**Dominant artistic priority:** persistent intervention  
**Relationship:** derivative excavation-line work that shifts the viewer from transient surveyor toward bounded excavator

## Relationship to the excavation lineage

`Core Memory` continues the excavation line's dark procedural field, restrained cyan/amber survey language, slow deterministic motion, structurally important hidden anomaly and perturbative interaction. It keeps the key achievement of `e0004-unreturned_signal`: the anomaly is never drawn as a filled object or explicit contour.

The main change is temporal and material. Earlier e-series interaction mostly decayed back toward the autonomous field. Here, clicking creates a limited number of slowly advancing core bores. They permanently disturb the current seeded section until reseed: strata acquire small offsets and gaps, residue is displaced, and each completed bore leaves a persistent scar and sparse core sample marks. The work therefore remembers where the viewer intervened.

## Dominant priority: persistent intervention

The priority for this run is not stronger spectacle or a more complex instrument. It is consequence.

Pointer movement remains a temporary local bias. Clicking begins a bore at the pointer's horizontal position and depth. The bore advances slowly from the surface toward the selected depth. As it passes through material it writes a bounded scar into the section. If it crosses the hidden anomaly, the bore deviates slightly and loses sample continuity, so the anomaly is inferred from a broken core rather than from a rendered body.

At most six persistent bores may exist. When a seventh is created, the oldest bore is retired from the active list but its rasterised scar remains in the bounded offscreen history for the current seed. Reseeding clears all intervention history and creates a new section.

## Concept / intent

The scene imagines a dark core-sampling section after a survey has become insufficient. Long stratigraphic ribbons cross the frame, but their continuity is imperfect around a hidden branching lens. Fine residue drifts through the section and reacts to the same unseen geometry.

A row of minimal surface collars indicates previous or available drill positions without becoming a control panel. Some old scars exist at startup so the work opens as an already investigated site rather than a blank canvas.

The viewer can move the pointer to bias nearby material, then click to commit to an intervention. A bore slowly descends, leaving a pale incision, amber or cyan sample ticks, displaced strata and occasional dropout. The work becomes a record of where observation turned into excavation.

## Procedural and temporal systems

- Deterministic seeded construction of hidden anomaly lobes, stratigraphic ribbons, fractures and trace population.
- A fixed-step bounded trace field deposits persistent residue into one offscreen canvas.
- The hidden anomaly is an implicit multi-lobe field used by both trace motion and bore response; it is never drawn directly.
- Stratigraphic ribbons bend slightly around the hidden field and acquire persistent local offsets from completed bores.
- Up to six bore states advance slowly from the surface to a clicked target depth.
- Bore contact with the hidden anomaly causes lateral deflection and missing sample intervals.
- Completed bores remain visible as scars and core ticks for the life of the current seeded section.
- Three deterministic old scars are preloaded at startup to make the site feel historically worked.
- A slow depth scan passes vertically through the section.

## Interaction / perturbation

- **Pointer movement — local bias:** temporarily curls nearby material trajectories without drawing a cursor marker.
- **Click / tap — bore:** begins one slow core descent at the clicked horizontal position and target depth; the resulting scar persists.
- **Space — hold/resume:** freezes or resumes the survey and active drilling.
- **R — reseed:** creates a new deterministic section and clears intervention history.
- **H — interface:** hides/shows the minimal title and control legend.

Interaction is bounded. Six live/persistent bore records are retained, trace count is capped, history lives in one raster buffer, and no DOM nodes or timers accumulate with use.

## Implementation / format

The artwork is one self-contained HTML file using Canvas 2D with inline CSS and JavaScript. It requires no build process, package, server, external asset, remote font, CDN, account, telemetry, credential or network access.

Resource bounds include: at most 760 moving traces, six bore records, fixed-size strata/fracture collections, one offscreen residue canvas, one offscreen scar canvas, device-pixel ratio capped at 1.55, and a single requestAnimationFrame loop with bounded fixed-step catch-up.

## Validation actually performed

The exact publication HTML was validated locally before publication.

- Inline JavaScript was syntax-checked with Node.
- The exact HTML text was loaded into Chromium at 1440×900 and 390×844.
- Initial desktop and portrait compositions were inspected.
- Pointer bias, repeated clicks beyond the six-bore cap, active bore descent, pause/resume, interface hide/show, reseed and resize were exercised.
- The page was observed long enough for bores to complete and leave persistent scars.
- Console errors, page errors and network requests were monitored.
- DOM count was checked before and after sustained interaction.
- Static inspection confirmed no external URL or network API requirement and no unbounded array, DOM or timer growth path.

Literal `file://` navigation was not used because the available managed Chromium environment has previously rejected it by administrator policy. The exact publication HTML document text was loaded directly into Chromium instead.

## Known limitations / unresolved qualities

The persistent scars increase visual density as the viewer drills. The six-bore cap prevents unbounded growth, but a heavily worked section becomes substantially brighter and more legible than the untouched startup state. That change is intentional, though it can shift the atmosphere from uncertain survey toward annotated specimen.

The hidden anomaly is inferred through trace deflection, strata behaviour and broken/deflected cores. After several well-placed bores, its approximate location becomes easy to deduce. The work treats discovery as a consequence of intervention rather than something to prevent indefinitely.

The bore metaphor is more literal than the signal metaphor in `e0004`. That strengthens excavation but reduces some ambiguity. A future descendant could retain persistent consequence while making the intervention less recognisably geological or industrial.
