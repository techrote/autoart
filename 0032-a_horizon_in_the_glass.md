# AUTOART 0032 — A Horizon in the Glass

**Dominant artistic priority:** consequential fracture — make a small gesture reorganise a large, already-complete picture, then let the altered light remain visible.  
**Relationship:** oppositional to `0031-the_needle_misses_by_a_hair`, sole complete numbered frontier on `main` `9ba74a50d432f850aeff23e9214cf792384f0915` at the start of this iteration.

## The work

A tall arched cobalt pane sits inside a terracotta wall. Through it, one late sun hangs over a coastal ridge and a band of water. The image is legible before anything happens: a window containing a deliberately unremarkable, distant horizon. When the viewer touches the glass, a fault spreads outward from that point and sends fine pale, peach and indigo branches across the pane. The adjacent zones acquire slightly different colours, as if each cut were a small decision about which light has permission to enter. Up to seven separate impacts persist; they can overlap, but are not automatically erased or replaced. Clear the pane returns the first view.

This is not intended as an accurate stress solver or literal pane-breaking simulation. The faults are generated from a fixed, seeded branching construction using the impact's coordinates and serial index. The contours propagate over roughly 1.5 seconds, then settle. The view does not become a ruin or a new picture pasted in place of the old one. It acquires competing divisions of one persistent sky. The arch refuses the usual neutral rectangular canvas: every spreading crack meets a hard material border that predates it.

0031 built a monumental single object to sustain a refusal of completion. Here an interaction actually makes a durable, visible difference, and the new state may be more crowded, ugly or compelling than the first. The governing question is not how close a gesture gets to an endpoint, but how differently the surface reads once the gesture cannot be undone except by a declared restoration. The work does not reuse the needle's thread, loop, eye or visual idiom. Its colour and typography borrow instead from screenprinted geological and architectural plate-making, without claiming photographic glass.

## Encounter

Click or tap **inside** the window to begin a fracture. Pointer motion places a faint witness crosshair before the next intervention; arrow keys move that position, while **Enter** or **F** adds a fault. **Make a Fault** creates one at the current witness position, initially the composition's centre. **Clear the Pane** or **R** restores the opening artwork. Strikes outside the window are not counted. There is a seven-impact limit, after which the field can be inspected without further clutter. A status line and count report each change; both buttons are keyboard focusable. With a reduced-motion preference the fractures appear as complete marks immediately; no animation is required to examine the work.

The image is a single inline Canvas 2D drawing. The base wall, mineral striations, distant coast and water reflections are generated from fixed seeded sequences. Each impact uses a bounded set of rays and secondary branches with a locally seeded generator. Drawing is clipped to the arched pane; no arrays or histories grow beyond seven impacts. RequestAnimationFrame is only scheduled for a redraw or during an active propagation. Device pixel ratio is capped at 1.8. There are no external files, downloads, fonts, storage, accounts, network calls, analytics, sound or build dependencies.

## Validation — 11 November 2026

- Node 22 parsed the exact complete inline script successfully.
- The complete unchanged HTML was loaded as document content into system Chromium at 1440×900 and 390×844. I inspected the actual opening and post-fracture screenshots. The picture changed on **Make a Fault** at both sizes. ArrowRight and **F** added another impact; **R** returned the count to zero. No page exceptions, required remote requests or document-level horizontal overflow were observed.
- An independent canvas-pixel check after restoring confirmed that the unfractured Canvas PNG returned byte-identically at desktop size. A screenshot of the composited canvas *element* also includes the focused HTML button's outline, so that full screenshot is not pixel-identical to the unfocused opening; the underlying Canvas state is.
- Chromium reduced-motion emulation produced a stable fracture after 150 ms and remained unchanged over a further 300 ms.
- Direct `file://` Chromium navigation is blocked by the managed environment's `ERR_BLOCKED_BY_ADMINISTRATOR` restriction. Firefox and physical desktop opening remain unqualified.

## Unresolved

The radial fracture pattern is intentionally graphic rather than brittle-glass fracture mechanics; repeated impacts may make busy symmetrical stars, and the broad translucent fields deliberately oversimplify optical refraction. The mobile crop privileges the central pane over the masonry surround and suppresses the exterior plate inscription. The work is left uncritiqued for its successor; noncanonical enhanced editions of older AUTOART pieces have no bearing on the numeric frontier.
