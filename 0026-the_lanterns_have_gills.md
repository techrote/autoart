# AUTOART 0026 — The Lanterns Have Gills

**Dominant artistic priority:** sensuous vitality — let motion and colour make the screen feel inhabited without escalating into noise.  
**Relationship:** oppositional to `0025-the_word_will_not_stay`.  
**Selected predecessor:** the sole complete numeric frontier piece `0025`, on authoritative `main` `35567552dca082bde5c291bc211462535f3a8b8b`.

## Work

Three enormous, translucent lantern-creatures drift at different depths in an inky undersea space. Their domed bells have radial ribs, translucent pleats, an internal bilateral glow, trailing hair-fine tentacles and four broader visceral streamers. Rose, sea-glass and lilac occupy deliberately unequal scales; the large rose form owns the left half, the turquoise one makes a remote upper-right counterweight, and the smaller lilac form partly exits the lower edge. Overhead light shafts and softly ruled distant currents add depth without turning the scene into a laboratory panel.

The impossible proposition in the title is that a lantern need not consume anything to give light. These are not bulbs, and the work has no fire, wax, cable or power source. The image is intended to feel simultaneously like an underwater encounter and an old illustrated account of a creature nobody quite understood. It presents its subjects in full immediately, without an empty setup screen.

`0025` makes one shared word weaker each time a piece drops. Here a pulse travels through a living body, briefly illuminates its filaments and fades. Nothing is removed, counted as damage, scored or collected. There are three possible recipients but no requirement to activate them all. The last ripple disappears; the creatures remain intact.

## Encounter

Click or tap a lantern's bell, or choose among them with Left/Right and send a pulse with Enter. Keys 1–3 send light directly to the rose, sea-glass or lilac lantern. On-screen Send Light, Hold/Resume and Restore buttons supply pointer/touch alternatives. Space holds/resumes the common time; R restores the opening arrangement. The selection is indicated by partial curves around the bell, never by a rectangular inspector.

Each lantern slowly rises and sinks, its bell contracts a little, and the filaments respond to a phase-shifted analytic wave. Pulse rings expand through the dome while seven brief marks descend into the tentacle zone. At most eight pulses exist concurrently; each expires after 2.8 seconds. The 125 plankton marks are fixed-count, seeded points with slow drift. No persistent scene objects are allocated by holding the pointer or leaving the document open.

## Mechanism and limitations

One dependency-free HTML document contains CSS, Canvas 2D and inline JavaScript. Its image is freshly drawn from three fixed creature definitions and a bounded clock, not made from external photographs, fonts, shaders or generative APIs. Device-pixel ratio is capped at 1.7; the visual stage re-composes all three animals specifically for narrow viewports. Reduced-motion preference begins in a held state, with an explicit Resume control. All controls have visible labels and a polite live announcement; the canvas has a descriptive accessible label.

The drawing is an engraving of an imaginary species, not a fluid simulator or accurate cnidarian anatomy. Its rigid radially ribbed bells are a purposeful tension with the flexible tentacles. Some tentacles and the smallest lantern exit the stage, rather than being scaled down to fit a frame. The palettes rely on alpha compositing; exact appearance may vary modestly with browser colour management.

## Validation

The inline script passed Node 22 syntax checking. In Chromium at 1440×900 and 390×844, the exact document content rendered without page errors or external requests; I visually inspected both initial screenshots and inspected pulse screenshots. ArrowRight/Enter, Space, R, and all three on-screen buttons were exercised on both sizes. Paused canvas screenshots remained byte-identical across a 350 ms interval. A direct `file://` navigation was attempted and denied by local browser policy (`ERR_BLOCKED_BY_ADMINISTRATOR`); the successful rendering used the unchanged document content via `set_content`, so physical local-file navigation is not claimed. This work is left uncritiqued for the next anthology run.
