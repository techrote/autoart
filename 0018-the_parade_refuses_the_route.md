# AUTOART 0018 — The Parade Refuses the Route

**Dominant artistic priority:** comic disobedience through visible collective motion.  
**Relationship:** oppositional to `0017-pending_room` (sole selected frontier predecessor).  
**Source frontier:** `main` at `74ad3abd373f8979cc3cf624173ebe7f2b74f2da` before this iteration.

## Intention

Where `Pending Room` made the viewer wait for an almost invisible answer, this piece answers loudly before it is asked anything. Forty-nine little flag-bearers traverse a dark printed route, but a subset consistently wanders beyond the marked lane. The official arrow, registration circle and revision number claim the authority of a plan; the procession behaves like a collection of individuals who never signed it.

The composition borrows the graphic vocabulary of inexpensive parade leaflets and misregistered screenprints: ink-blue road, coral headline, mustard/turquoise pennants, cream newsprint, emphatic typography and imperfectly regimented characters. Their bodies are blocky signs with legs, flags and different routes of refusal, not realistic people. The mood aims for mischief instead of dread, without making the participants into a conventional game.

The title is a deliberate return to an unfulfilled possibility implied by an existing, empty `art/0018-the_parade_refuses_the_route` branch; that branch was identical to the starting `main` and contained no unpublished art. This work was authored afresh on a separate branch.

## Mechanics and encounter

A stable analytical road curves diagonally upward. Each of 49 bounded, deterministic characters samples its own phase on that road, with a different local sway. Several are permanently disobedient, travelling off-route; others appear to be following before veering. The visual joke is that a route intended to coordinate everyone mostly makes their independence measurable.

A click or tap diverts a local cluster for eight seconds while up to six bounded ripple records remain visible. Some depart in mutually opposite directions. A keyboard marker can be positioned with the arrow keys and triggered with Enter; holding Shift increases marker step size. Space pauses/resumes, and R restarts the same procession. The initial image is already composed and does not require input. When reduced motion is requested, autonomous movement is held until explicitly resumed; tapping or pressing Enter produces a static diversion cue instead of a continuously ticking effect.

The dominant action is deliberately immediate, a counterpoint to `Pending Room`'s long unpublished wait. The road and printed typography do not change: only the little beings making use of them do.

## Format and validation

One HTML file with inline Canvas 2D, CSS and JavaScript; no fonts, images, network access, server, package manager, services or telemetry. The number of figures is fixed at 49, pointer-event history is capped at six, device-pixel ratio at 1.75, and there is at most one animation-frame chain. No intervals or timeout queues are used. The portrait layout reprints the headline within the visible column rather than cropping the wide poster typography into illegibility.

The exact candidate HTML script passed `node --check` and static checks for external/network dependencies. Chromium rendered its full contents at 1200×800 and 390×844; screenshots were actually inspected. Desktop animation, click, arrow-key marker, Enter, Space, R and viewport resizing were exercised with no reported page exceptions, console warnings/errors, remote requests or DOM growth. Literal local-file navigation was attempted but blocked by managed browser policy; therefore *direct `file://` execution is not claimed*. These local preview screenshots are deliberately not published as artwork or mistaken for separate canonical exports; the HTML itself is the complete piece.

## Deliberate limits

The participants' differences are graphic rather than narrative. Their flags do not have text, names, hierarchies or biographies. On narrow portrait screens only a central segment of the longer route is visible, by design, while the headline is reprinted so the subject remains legible. There is no win condition and no attempt to simulate crowd physics.
