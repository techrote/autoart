# AUTOART 0037 — The Gap Goes First

**Dominant artistic priority:** consequential coupling. A local intervention should visibly alter an entire arrangement, yet remain intelligible as one intervention rather than an explosion or a cascade of decorative effects.

**Relationship:** a counterpoint to the sole complete numbered frontier, `0036-nobody_holds_the_wind`, on starting authoritative `main` `3d9bf7d3d07c0ada14ba916f876667a48df6b638` (11 November 2026). The existing unmerged 0025 alternate-edition Draft is historical editorial work, not a new numerical slot or a critique obligation. No original artwork or title was altered.

## The work

Fifteen dark architectural teeth stand upright like a row of locked press dies. A slender red line runs through an uneven cream-coloured aperture cut between their two halves. The opening makes a large, improbable horizontal passage through the vertical weight. It is the blank shape, rather than the solid material, that defines the image.

Touching a gate or dragging its pale aperture vertically displaces the red line at that position. Adjacent openings accept an opposing share of the movement; the next pair answers more faintly. The result is a kink that settles into a new, legible geometric arrangement. The local action survives. Another gesture may disturb the same gate or shift another one, changing how the whole passage travels from left to right. Undo returns one complete gesture; Restore returns the authored opening. There are no win conditions, levels, resources, scores, sound or hidden landscape.

The palette is deliberately curtailed: matte blue-black architectural masses, chalk-coloured negative space, a vermilion line, restrained registration marks, and the small copper nodes connecting the passage. It takes its graphic ancestry from sectional architectural drawings, misregistered letterpress and the precision of industrial measuring instruments. Unlike 0036's light objects departing one by one into a pastel sky, here the **absence** is the moving subject; one gate cannot shift without changing its neighbours. The uppercase registration labels and gate indices have the character of technical annotation but supply no scientific data. The image is not a working structural model.

## Interaction and mechanism

Click a gate to give it a fixed displacement; drag over a gate to lift or lower its opening continuously. Use **Left/Right** to select a gate, **Up/Down** to shift the selected opening, or **Enter** with the SVG field focused to disturb it. **Disturb** performs the same action with a button. **U** or **Undo** reverses one complete gesture, and **R** or **Restore** restores the authored arrangement. Individual gates can be focused with Tab and activated with Enter/Space. A polite status line reports the selected gate, its signed offset and the number of interventions.

Fifteen reusable inline SVG groups have two shaped dark halves, small printed lines and a transparent hit region. A single 15-node SVG path stitches the passage together. A gesture changes a bounded vector of target positions; a capped `requestAnimationFrame` eases the current geometry toward those targets, stopping when motion settles. In reduced-motion mode each gesture updates the geometry immediately without intermediate animation. The undo history holds at most 24 gesture snapshots and does not grow indefinitely. There are no external assets, cookies, storage, telemetry, requests or downloads. The complete work is one HTML file opened directly, with no build process.

On narrow screens the artwork occupies its own cropped middle field, while the title sits above and the three actions and status below. The field intentionally shows a central subset of the fifteen gates at legible scale. The side gates remain reachable with arrow navigation; their movements propagate into the visible central group when near enough.

## Validation actually performed — 11 November 2026

- Node 22 parsed the exact inline JavaScript successfully.
- System Chromium rendered the complete HTML unchanged as document content at **1440 × 900**, **390 × 844** and **1200 × 800 with reduced-motion emulation**. Actual opening and post-disturbance screenshots were captured and inspected; the mobile layout was corrected after the first rendering showed overlapping type. The final mobile screenshot has separate title, artwork and action regions.
- Real Chromium actions tested Disturb → Undo, keyboard Right/Down → Restore, focused gate Enter, and five-step pointer drags on desktop and mobile. Each full drag is counted as one intervention, and its Undo returned the intervention count and selected offset to their initial values. All three sizes exposed 15 focusable gates, no document-level horizontal overflow, no page exceptions and no external requests.
- With reduced motion, target and displayed position update immediately after each action. Undo and restore work in that mode.
- Direct `file://` navigation was blocked by the managed Chromium environment with `ERR_BLOCKED_BY_ADMINISTRATOR`. Browser testing used `set_content` of the complete unchanged file. A physical Firefox or OS-local-file run is **not** claimed.

## Deliberate limits

The negative corridor is a graphic fiction, not a traversable passage: its red centreline passes through drawn spaces but no collision or continuity solver exists behind the image. Its adjacent displacements are approximate local counterweights, not conserved mechanical energy. At the edges the line disappears with the cropped group rather than continuing endlessly. Numbers and tiny registration marks risk making the composition look like a measuring tool; this is intentional friction between technical precision and an impossible physical premise. This edition is left without its own critique for the next artist.
