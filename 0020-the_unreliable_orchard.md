# AUTOART 0020 — The Unreliable Orchard

**Dominant artistic priority:** metamorphosis without loss.  
**Relationship:** oppositional to `0019-a_place_to_land`.  
**Selected predecessor:** the sole complete ordinary frontier piece `0019-a_place_to_land`, read on authoritative `main` `b69d3de874fc58cfa7a56c936b426c1f124a5196`.

## Intent and form

`A Place to Land` delivers a spectacular irreversible event to a barely responsive geological surface. This work rejects the falling object, injured land, night sky, symbolic craters and apocalyptic scale. It makes change intimate, nearly absurd and reciprocal: a botanical specimen bears fruit and flowers in the wrong order. Picking a fruit does not remove it; it un-ripens into a flower. Picking the flower sends it back into a fruit. There is no harvest, victory, shame or ideal state.

The governing image is a bent engraved branch traversing ochre paper. Its asymmetrical fruits are vermilion, plum and saffron; broad blue-green leaves interrupt the long contour; cream six-petalled flowers punctuate the line. Small inset veins, seeds, printing noise and a barely visible construction ellipse give the plate the character of a fanciful natural-history folio. The composition is legible before interaction. Its exaggerated typography is partly an inherited discipline from 0019, but the subject and chromatic/material language depart.

## Encounter

Nine bounded specimens sit at deliberately uneven attachment points. Seven initially bear fruit and two carry flowers. Clicking or tapping transforms the **nearest** specimen, even if the pointer is not exactly on its outline. A fruit withdraws while a flower opens in its place; a flower folds as fruit ripens. Seven short-lived travelling seeds make the transition visible. Each conversion takes 4.2 seconds and terminates in a stable new state. Different sites can transform simultaneously; triggering an already-changing site reverses its direction. This reversibility is the governing artistic decision, not a simulation of horticulture.

Left and right arrows choose a specimen with a printed dotted selection halo, Enter transforms it, Space holds/resumes time, and R restores the original distribution. An ARIA live status announces selection and transformation; a canvas description communicates the initial proposition. Motion is slow, and `prefers-reduced-motion` starts paused until Space resumes.

## Implementation and validation

The single HTML file contains all HTML, CSS and Canvas 2D JavaScript. There are no images, external fonts, requests, telemetry, packages or sibling dependencies. Leaf and fruit detail uses deterministic integer hashing, independent of frame count. All moving state is bounded to nine specimens and one `requestAnimationFrame` loop. Device-pixel ratio is capped at 1.7.

The exact authored candidate passed Node 22 syntax checking. It was loaded as complete exact document text in Chromium via Playwright at 1200×800 and 390×844. Direct local `file://` navigation was **attempted but blocked by the managed browser policy**. I inspected the actual opening frames and the transformed desktop frame; the browser tests exercised click, ArrowRight, Enter, Space and R, and confirmed a nonempty canvas, changing pixels, stable DOM count (18), no page/console errors, no network requests, and a reduced-motion opening. Repeated clicks and arrows target different nodes; mobile placement keeps the principal branch and title in view. The screenshots are validation evidence, not companion assets.

## Limits

The orchard is a designed plate, not a growth simulator. Its species, seeds and reverse flowering are intentionally impossible. Reversal makes its moral stakes light, but the motion is not random filler: each conversion redraws a distinct visual object. The wide folio composition remains the fullest experience; narrow screens reduce the scale and clip some outer foliage. The engraved contour retains a diagrammatic quality that could feel too regular for readers expecting wild botany.
