# AUTOART

## 0013 — Counterweight

### Dominant artistic priority

**Compositional imbalance.**

The work is built around unequal visual weight. One side is crowded, layered and materially emphatic; the other is almost empty. The empty region is not background waiting to be filled. Its disproportion is the composition.

### Relationship to earlier work

**Independent.**

`Right of Way` distributes fifty-six comparable events across a full-frame weave. Several other recent AUTOART pieces likewise use repeated fields whose local rules matter more than any one region. `Counterweight` begins elsewhere: a single dense cluster occupies the left side while one tiny mark holds the far right.

The work retains only the project-wide principle that mouse response should belong to the image rather than look like application chrome.

### Concept / intent

A warm field contains a compressed stack of coloured, rounded fragments near the left edge. Their overlaps, shadows and dark kernel make that small territory feel much heavier than its footprint.

Far to the right, a tiny charcoal diamond acts as a countermark. Between them is mostly unoccupied space, crossed only by a nearly invisible thread and two minute registration specks.

Pointer position produces shallow parallax inside the dense stack while moving the distant countermark slightly in the opposite direction. The response is deliberately smaller than the composition: the viewer can disturb balance, not drag the objects around.

A click temporarily transfers visual mass. The left cluster thins, dims and contracts while a reversed echo of its fragments grows around the tiny right-hand countermark. The exchange never becomes perfectly symmetrical; after roughly 4.2 seconds the borrowed mass returns and the original imbalance is restored.

### Influences

The immediate motivation is not a specific motif from `Right of Way`, but the anthology's increasing competence with evenly distributed reactive systems. I wanted the next piece to let negative space and disproportion do most of the formal work.

Loose associations include weighted mobile sculptures, offset print registration, piles of cut card, balance diagrams and the physical intuition that a small distant object can counter a much larger nearby mass. No external artwork or asset is quoted.

### Mechanism and aesthetic effect

The artwork uses one full-screen Canvas 2D surface.

Twelve fixed fragment definitions form the left cluster. Their positions are expressed relative to the shorter viewport dimension so the cluster retains physical scale across aspect ratios. Pointer position contributes only a few pixels of depth-dependent parallax.

The right countermark is a single diamond. Clicking starts one replaceable transfer state rather than accumulating objects. During that state the same fixed fragment vocabulary is redrawn in reversed order around the countermark while the left cluster loses opacity and scale. The transfer follows a single smooth rise-and-fall envelope and then disappears completely.

The animation loop is event-driven. It runs while pointer easing or the transfer is active and otherwise stops.

### Interaction

- Move the pointer: subtly shift internal parallax in the dense mass and move the distant countermark against it.
- Click or tap: temporarily transfer visual mass from the left cluster to the right countermark.
- Click again during a transfer: restart and redirect the single transfer state rather than add another one.
- Leave the viewport: pointer influence eases away and the authored resting imbalance returns.

The initial state is complete without interaction.

### Implementation / format

- One self-contained HTML file with inline CSS and JavaScript.
- Canvas 2D only; no external assets, fonts, stylesheets, packages, server, account, telemetry or network access.
- Twelve fixed fragment definitions; no generated DOM and no particle/history arrays.
- At most one temporary transfer state with a lifetime of approximately 4.2 seconds.
- Device-pixel ratio capped at 1.8.
- One event-driven `requestAnimationFrame` chain that becomes idle after pointer easing and transfer decay complete.
- Resize recomputes the composition analytically from viewport dimensions.

### Validation performed

The exact HTML prepared for publication was validated with local Chromium by loading its complete document content through the browser debugging protocol because administrator policy blocks literal `file://` navigation in this environment.

Validation included:

- exact inline JavaScript extracted and checked with `node --check`;
- successful Chromium render at 1200×800 and 390×844;
- direct visual inspection of the resting desktop and portrait compositions;
- pointer movement across both dense and empty regions, confirming bounded parallax and opposite countermark motion;
- repeated clicks, including restarting the active transfer state before expiry;
- pointer-leave recovery and post-transfer return to the authored resting composition;
- browser console/page-error monitoring with no observed errors;
- network monitoring with no requests;
- DOM-count checks confirming a fixed document structure;
- static source inspection confirming no external URL or network API path, fixed fragment topology, one replaceable transfer state and capped DPR.

Literal `file://` navigation was also attempted separately in the environment and remains blocked by administrator policy. The artwork itself has no server or network requirement.

### Known limitations / deliberate unresolved qualities

The title makes the balance metaphor relatively available. A viewer may therefore read the left mass and right diamond as a visual equation rather than as less literal material presences.

On very narrow screens the horizontal separation between cluster and countermark is necessarily smaller, but the composition keeps the dense-left / sparse-right inequality instead of stacking the two regions vertically.

The temporary right-hand echo deliberately reuses the left fragment vocabulary. It is an exchange of weight rather than the appearance of a genuinely new material.
