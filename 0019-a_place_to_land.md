# AUTOART 0019 — A Place to Land

**Dominant artistic priority:** irreversible grandeur.  
**Relationship:** counterpoint/oppositional.  
**Selected predecessor:** `0018-the_parade_refuses_the_route` (the sole complete ordinary frontier at initial `main` commit `6c0d0d08cd6473cf86231e42b214741a6a16e5ee`).

## Intent

The previous piece made disobedience communal, colourful and immediately funny. This work removes the marchers, the road, the social joke and the expectation that movement can continue without leaving a trace. A single hot, patterned stone descends through an enormous dark astronomical plate and strikes a layered coast. Its movement is not a toy-like procession: the first fall takes about fifteen seconds and changes the material surface. Each impact exposes one durable ring and radiating hairline fractures. The surface keeps only the five most recent scars, preventing unlimited accumulation without presenting a score or an undo history.

The first frame is already a composition: a carved crimson-and-cream body, very faint orbital ellipses, a narrow luminous geological contact, a tiny survey stake, and much unused sky. Colour is concentrated in the falling body and in the sediment edge. This is not a simulated astrophysical event. The size, speed, debris arc and crater are pictorial rather than physical; they aim to make arrival feel weighted without claiming accurate impact dynamics.

## Mechanism and encounter

The audience can choose *where* the next mark will land but cannot cancel the act of landing. Clicking or tapping sets a marked impact longitude; left/right arrows move the keyboard marker, and Enter applies it. The stone steers gradually toward a changed destination, so a late input does not teleport it and may not fully redirect the imminent fall. A collision produces a four-second ring/debris aftermath, followed by the next isolated descent. The sequence varies the incoming origin and scale modestly on each cycle. `Space` pauses or resumes; `R` clears the scars and restarts the authored initial state.

The title and commands are printed over the scene as a restrained colophon, not a dashboard. Impacts announce themselves through a screen-reader status. The subject is singular and the interaction concerns consequence rather than continuous visual turbulence.

## Format and validation

One completely self-contained HTML file with CSS and Canvas 2D. It requires no network, build, fonts, images, sibling files, package manager, service or telemetry. Scratch texture uses deterministic integer hashing; animated state is bounded to one falling stone, five durable scars and one requestAnimationFrame chain. Device-pixel ratio is capped at 1.8. In `prefers-reduced-motion`, the initial composition is held until the viewer explicitly resumes it.

The exact candidate HTML was syntax-checked using Node 22 and tested in local headless Chromium at 1200×800 and 390×844. Direct `file://` navigation was **attempted and blocked by browser administrator policy**, so the same exact document text was loaded with Playwright's `set_content` for actual rendering and interaction. Desktop/mobile initial and changed compositions were captured and inspected. Click/tap-equivalent pointer, arrows, Enter, Space, R, and viewport layout passed; the live status changed appropriately. A Chromium virtual-clock run crossed the first actual impact after 16.2 seconds and the reset/new-descent transition after 21.6 seconds. There were no reported page exceptions, console errors or remote requests, and the DOM count remained 18. These validation screenshots were not committed: the HTML is the artwork.

## Limits

The earth is a graphic cross-section with a shallow surface, not a physics engine. There is no audio, score, simulated gravity or user inventory. Early marks eventually leave the finite five-mark memory. If the destination is changed just before contact, the impact will land between the current trajectory and the new request rather than jumping instantly; the slight mismatch is intentional. The initial dark expanses ask for attention but never hide the object that is doing the work.
