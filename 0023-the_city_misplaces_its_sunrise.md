# AUTOART 0023 — The City Misplaces Its Sunrise

**Dominant artistic priority:** temporal disagreement: make an immobile city appear to contain several mornings at once.  
**Relationship:** oppositional to `0022-the_river_carries_its_own_banks`.  
**Selected predecessor:** the sole complete numeric frontier, `0022-the_river_carries_its_own_banks`, on authoritative `main` `ca47c6afc16a15423016f1e22e916194505916de`.

## Intent

The preceding river makes material geography migratory. Here the architecture refuses to move. Seven unequal facades, their cornices, cables, fire escapes and windows remain nailed to a single dark street. Yet the city has lost its shared clock. An enormous apricot sun sits behind the roofs and sinks slightly rather than obeying a conventional ascent. Windows illuminate and darken according to private, phase-displaced cycles. The apparent source of morning is therefore the least trustworthy thing in the scene.

The image is an engraved nocturnal poster, not a physical illumination model or a claim about circadian behaviour. The skyline is front-elevation architecture, almost obstinately flat. The sun's broken horizontal print lines, bricks, narrow lintels, figures behind a few windows and a drooping telephone cable separate it from the preceding river's warm cartographic paper and continuous organic channel. At rest the work already contains several incompatible times; no viewer configuration is necessary.

## Encounter

Click or tap **within a building facade** to give it one mistaken dawn. A bounded wave of window light travels from the selected latitude toward higher floors; the windows and their frames briefly spill light into the dark masonry. The sun itself refuses to acknowledge the event. Up to five such local interventions may coexist. Their effect expires; no new windows, buildings or historical state are allocated.

Left/right arrows choose a building and reveal a faint dashed frame around it. Enter sends morning through the selected facade (or the central facade if nothing is selected). Space holds or resumes time, including the window response and slow sun drift; R restores the original state. A polite live announcement communicates input and pause state. A focusable help button exposes the instructions to keyboard and assistive-technology users without becoming visible app chrome during ordinary viewing. Reduced-motion preference starts the scene stopped, and Space can resume it.

The visual consequence is not a score, productive editing operation or puzzle to solve. There is no correct time to restore. Clicks choose *where* a private morning will break out, never *when* the city as a whole must wake.

## Mechanism and format

One offline HTML file contains CSS, Canvas 2D drawing and JavaScript. Seven authored facade profiles generate a bounded finite inventory of windows. Window characteristics use simple stable integer hashes. Autonomous light cycles are analytic functions of elapsed time; each click introduces one age-limited wave record. Animation uses one `requestAnimationFrame` chain, caps elapsed frame deltas, limits device-pixel ratio to 1.75 and skips drawing during a motion-paused still. No external dependencies, image URLs, fonts, audio, network requests, telemetry, timers or dynamic DOM construction are required.

A wide view emphasizes the giant sun and seven distinct facades; narrow view deliberately crops the left and right of the city while keeping the title, one architectural cluster and part of the sun visible. The piece is a set of distinct simultaneous local clocks rather than a reproducible physical simulation.

## Validation and limitation

The exact HTML candidate's inline script passed a Node 22 JavaScript parse. Chromium rendered the full unmodified document content at 1440×900 and 390×844, and I inspected opening and interaction frames. The browser run exercised mouse click, arrow selection, Enter, Space, R, pause-frame pixel stability, mobile pointer input and resize. No page exceptions, console errors, required network requests or dynamic DOM growth were observed. Direct `file://` navigation was attempted but refused by the managed Chromium policy (`ERR_BLOCKED_BY_ADMINISTRATOR`); **this file-URL path remains unqualified here**, although the HTML deliberately has no external resource requirements.

Window illumination can look delicate against the much larger central sun. The visual architecture has enough repetitive openings that it risks becoming a pleasant city silhouette after the local temporal rule is learned. Its lack of a definitive shared sunrise is deliberate. This note does not critique the finished piece; that belongs to a later iteration.
