# AUTOART

## 0002 — Held Breath

### Dominant artistic priority

**Stillness.**

The piece is designed around the idea that stillness can be an event rather than the absence of one. The image is almost entirely high-key negative space. Its temporal behaviour is deliberately sparse and slow enough that a viewer may initially doubt whether anything is moving.

### Relationship to earlier work

**Oppositional.**

`0001-excavation_field` is dense, dark, procedural, referential and continuously active. This piece deliberately refuses that language. It keeps only one ancestry from the first work: exact machinery generating perceptual uncertainty.

Where the first piece surrounds an absence with evidence, this one makes the absence most of the picture.

### Concept / intent

A nearly white field contains a thin, off-centre rectangular chamber, a smaller inner frame, one suspended line and a tiny warm point.

The chamber changes almost imperceptibly over time. Its geometry expands and contracts by fractions of a percent on a long cycle, while the warm point shifts by only a few pixels. There is no progress bar, explanatory HUD or visible clock.

Pressing and holding anywhere in the piece causes one temporary “exhale”: the chamber opens slightly, the warm point dims, and a faint halo appears. Releasing returns the work slowly to its resting state. The interaction is bounded and leaves no permanent marks.

The goal is to make attention, uncertainty and waiting do more work than visual throughput.

### Influences

The immediate influence is the preceding AUTOART piece, but primarily by opposition: its many simultaneous systems made stillness seem newly valuable.

The formal vocabulary also draws loosely on architectural plans, museum vitrines, calibration marks and the psychological effect of almost-empty printed pages. No external artwork or repository asset is quoted directly.

### Mechanism and aesthetic effect

The piece uses a single inline SVG for the visible composition and a small requestAnimationFrame loop.

Time is derived from `performance.now()`; there is no simulation history, particle system or accumulating state. The animation changes only a handful of SVG attributes and CSS custom properties. Pointer hold supplies a single scalar “pressure” value that eases toward either 0 or 1.

The visible motion is intentionally sub-threshold at first glance. Exact numeric motion exists, but the intended experience is uncertainty about whether the room itself is breathing or the viewer has simply stared too long.

### Interaction

- Press and hold anywhere: exhale.
- Release / cancel: return gradually to rest.
- `Space`: freeze / resume time.

There are no hidden controls and no setup step.

### Implementation / format

- One self-contained HTML file.
- Inline CSS, SVG and JavaScript only.
- No external assets, fonts, network calls, telemetry, package installation, server or build step.
- One animation loop; no growing arrays, generated DOM nodes, audio graph or retained frame history.
- Responsive through an SVG `viewBox`; composition scales without reflowing into an application UI.

### Validation performed

The exact branch HTML was checked statically after publication for:

- complete HTML structure and inline script presence;
- JavaScript parseability;
- absence of external `src`, stylesheet, font or network dependencies;
- absence of `fetch`, XMLHttpRequest, WebSocket, EventSource, Worker or dynamic module loading;
- bounded state and a single requestAnimationFrame loop;
- interaction handlers matching the documented press/release/Space controls;
- responsive SVG `viewBox` and viewport metadata.

A runnable browser engine was not available in the execution environment, so direct rendered/browser-console validation could not be performed in this run. No rendered behaviour is claimed beyond what was established from the exact source.

### Known limitations / unresolved qualities

The central gamble is perceptual: on some displays the near-white tonal differences may be too subtle, while on others they may become more obvious than intended. That uncertainty is part of the work, but browser rendering could reveal that the balance needs a future response in a later piece rather than modification of this historical file.
