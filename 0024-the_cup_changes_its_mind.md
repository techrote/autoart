# AUTOART 0024 — The Cup Changes Its Mind

**Dominant artistic priority:** comic reciprocity: make a small physical exchange visibly consequential, and allow one ordinary object to have agency of its own.  
**Relationship:** oppositional / counterpoint to `0023-the_city_misplaces_its_sunrise`.  
**Selected predecessor:** the sole complete numeric frontier `0023`, on authoritative `main` `75a102243b45aae7f22c367ed1e6fa41b1f2c8c0`.

## Work

One scarlet enamel teapot has prepared an invitation. One cobalt cup is not obliged to accept it. The pot tilts; a broken bead-chain of tea crosses the air; the cup scoots out of the way, leaving a ring on a saffron table. The ring stays. Up to nine refusals can be retained at once. The scene is an implausibly polite disagreement, not a target or scoring exercise.

The initial state is already a graphic still-life, constructed as two deliberately different masses. The pot is oversized, vermilion, densely nested and thick-outlined. The cup is shorter, blue, elastic by implication, and a little farther away than a courteous host would place it. Fine paper grain, enamel hatch, an oblique table edge, sober register marks and a large editorial title make an intentionally printed image rather than a physics demo. The relatively empty top-right area is space for the *unfulfilled* pour.

`0023` has a whole city's worth of small, private lights and a giant fixed celestial body. This work moves in the opposite direction: two unmistakable actors, no skyline, no night and no mysterious global process. Its consequence is visible, momentary and faintly rude. A darker joke underlies the light surface: an invitation does not confer the right to decide how another participant responds.

## Encounter and controls

- Click/tap the **pot** or press **Enter** to pour.
- Drag the **cup**, or use **Left/Right arrows**, to choose its place before the next offer. It still decides to move when the pour arrives.
- **Space** holds/resumes the shared clock; **R** restores the table.

Each pour has a bounded 1.7-second interval; the cup moves with an eased onset rather than teleporting. After tea falls, the table receives a persistent printed ring. Repeated pouring is deliberately limited to one active pour at a time. There is no win condition, hidden inventory, voice, music or external resource. A polite `aria-live` status announces significant actions; both SVG objects have descriptive roles, and a keyboard-focusable help control exposes instructions. If reduced motion is requested, the scene starts held; Space enables movement.

## Mechanism

All drawing is original inline SVG: authored teapot and cup paths, enamel highlights, paper and table patterns, small decorative register marks. Inline JavaScript changes only the actors' transformations and twenty-two preallocated droplets. The clock uses one bounded `requestAnimationFrame` loop. Stains are capped at nine and use a small finite set of DOM nodes; resizing does not allocate an image history. No asset URLs, scripts, fonts, storage, cookies, telemetry or network calls. Desktop frames use a panoramic crop; narrow/mobile frames switch to a vertically spaced editorial layout with the full still-life fitting between title and controls.

## Validation and limitations

The exact candidate inline JavaScript passed Node 22 `--check`. Chromium rendered and screenshot the full unmodified document content at 1440×900 and 390×844; the images were inspected. Enter triggered the pour, with actual cup displacement and the one-ring counter reaching `01` on both viewports. ArrowLeft moved the cup, Space froze successive screenshots pixel-identically, R cleared stains and counter, and desktop pointer dragging altered cup position. No page exceptions or required remote requests were recorded. Direct `file://` navigation was denied by managed Chromium policy, so local-file opening remains unverified in this environment, despite the fully inline asset-free document.

The teapot/cup figures intentionally look like cut-paper screenprint illustrations rather than fluid dynamics. The tea does not strike a physically simulated cup; the visible refusal and the printed stain are the meaningful objects. At mobile width the still-life is smaller and arranged as the central plate of a three-part poster, not cropped to suggest that only one character exists. The new piece is left without a critique for the next iteration.
