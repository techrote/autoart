# AUTOART 0021 — The Unfaithful Shadows

**Dominant artistic priority:** misattribution — making a stable body coexist with evidence of an incompatible identity.  
**Relationship:** oppositional to `0020-the_unreliable_orchard`.  
**Selected predecessor:** the sole complete ordinary frontier piece `0020-the_unreliable_orchard`, published on `main` at `bb095ac81f2a2537f97718ebb9e52d2beedc380b`.

## Artistic intent

The preceding orchard transforms the specimen itself, then allows it to return unharmed. This piece leaves its five museum artifacts untouched. Their shadows, however, cannot be trusted: an urn is assigned a fish; a chair, a tree; a bell, a bird; a sculpted hand, a key; a lamp, an architectural stair. Click one plinth and its impossible shadow travels to the next, crossing another shadow on the way. The two arrive at each other's stations and remain there, as though a registrar had corrected the wrong paperwork. There is no legitimate final alignment and no win condition.

The opening is a full nocturnal gallery rather than a blank instrument. Five arched bays are deliberately unequal in width and height; low plinths, warm ceramic/metallic objects, theatrical lamps and almost-black oversized silhouettes establish two incompatible inventories. Deep aubergine, old rose, bone and oxidized brass displace the orchard's sunny natural-history printing. A slow sway of lights makes the borrowed projections appear restless even when nothing has been exchanged. During an exchange, the two shadow silhouettes cross on distinct high and low trajectories, so the movement reads as a real transfer rather than an instantaneous palette swap. The artifacts never follow.

This piece is not a photorealistic theory of cast shadows; it is a staged lie about causation. The silhouettes are intentionally flat, almost cut from theater paper. The contradiction is allowed to be visually obvious.

## Encounter and controls

- Click or tap a plinth (within its visible bay) to exchange its shadow with the next; the fifth exchanges with the first, across the collection.
- Left/right arrows choose a plinth. Enter exchanges its shadow with the next. Keys 1–5 directly select. The dashed gold frame indicates keyboard/active selection.
- Space pauses and resumes all motion, including transfers; R restores the original incorrect assignments.
- One exchange takes 2.4 seconds; a second exchange is refused until the first completes. The status live region communicates selection, travel, rejection and reset. On a narrow screen, selection also shifts the camera to the chosen bay.

Reduced-motion preference starts the gallery motionless; Space explicitly resumes movement. No sound, web font, network permission, server or sibling file is required. The entire artwork is one HTML file with inline CSS and bounded Canvas 2D JavaScript. It draws five fixed objects, five fixed shadow silhouettes, at most two travelling shadows, one animation loop and no accumulating history or DOM nodes. DPR is capped at 1.75.

## Validation

The exact candidate script passed `node --check` with Node 22. Chromium loaded the complete exact authored HTML text with Playwright (direct `file://` navigation was attempted and returned `ERR_BLOCKED_BY_ADMINISTRATOR`). At 1440×900 and 390×844, I inspected actual opening screenshots. On desktop I also inspected an in-progress exchange and its settled state. Playwright exercised mouse selection, arrow/Enter exchange, Space hold/resume, R restoration and mobile keyboard selection/exchange. Neither viewport produced page/console errors or external requests. A real `file://` execution, rather than loading the exact document text into Chromium, remains unverified because of the managed browser policy. (Temporary screenshots and test scripts are not publication assets.)

## Unresolved qualities

The museum is an impossible, visually legible tableau, not a physical light simulation. Some cut-out silhouettes are very literal, especially the fish and key; their readability is the price of the central contradiction. On narrow portrait screens, the exhibition is cropped intentionally into a moving window on a larger room, not squeezed into a five-column thumbnail. The slow automatic lamp drift is subtle; viewers who never exchange shadows will encounter a composed but largely still stage. The title and instructions frame the joke explicitly, risking less ambiguity than an entirely unlabeled collection might carry.
