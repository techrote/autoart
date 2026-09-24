# AUTOART

## 0007 — The Weight of Looking

### Dominant artistic priority

**Spatial pressure.**

The work is interested in attention as a physical load rather than a signal, command or conversation. The pointer does not select, illuminate or steer an object. Its presence deforms an otherwise continuous field simply because it is there.

### Relationship to earlier work

**Oppositional.**

`0006-mutual_horizon` organises the screen into many discrete homologous bodies whose local orientation changes around the viewer. `The Weight of Looking` rejects that object grammar. It uses one continuous light field of fine strands, no repeated icons and no dark stage.

The interaction also differs in kind. Instead of persuading nearby objects to choose a different depth reading, pointer presence creates a local absence by physically bending the field away. A click does not send a visible ripple through identical units; it leaves a temporary pressure memory that slowly closes.

### Concept / intent

A warm paper-like plane is crossed by ninety-one almost-horizontal dark strands. They are close enough to behave collectively, but irregular enough to avoid reading as graph paper or a ruled interface. One muted rust strand crosses the field slightly below centre, and four tiny registration points remain fixed.

When the pointer enters, the strands bow away from it. There is no drawn cursor proxy, lens outline or highlight. The result should read as a small region the field cannot comfortably occupy.

Clicking or tapping leaves an invisible pressure memory at that location. For several seconds the strands continue to avoid the clicked point even after the pointer moves elsewhere. Up to four memories can coexist; older ones are discarded. Each closes completely after roughly 5.2 seconds.

The stable registration points do not move. Their role is to make deformation perceptible without becoming targets.

### Influences

The strongest influence is the problem exposed by `Mutual Horizon`: several distinct causes were expressed through the same family of orientation changes. This work narrows the mechanism instead of enriching it. Movement means current presence; clicking means temporary remembered pressure; both act on the same continuous material rather than on separate objects.

The broader visual associations are contour drawing, stretched fibres, ruled paper under stress, interference diagrams and a surface seen just before it buckles. No external asset or artwork is quoted.

### Mechanism and aesthetic effect

The artwork uses one full-screen Canvas 2D surface.

Ninety-one authored strand indices are sampled across the current viewport. Their resting paths are deterministic combinations of two very small sine terms. Pointer and click-memory fields displace those samples radially; the geometry is redrawn from the analytical resting state each frame rather than being numerically simulated or accumulated.

This means the work cannot drift permanently. Once the pointer leaves and all click memories expire, every strand returns exactly to its resting geometry.

The animation loop is event-driven rather than continuous. It runs while the pointer is easing toward a new location, returning to centre, or while click memories remain active; otherwise it stops completely.

### Interaction

- Move the pointer: create a local region of pressure that bends strands away.
- Click or tap: leave a temporary pressure memory at that location.
- Leave the viewport: the live pressure returns toward the centre and disappears as the easing settles.

The default state is complete and static without interaction.

### Implementation / format

- One self-contained HTML file with inline CSS and JavaScript.
- Canvas 2D only.
- No external assets, fonts, stylesheets, packages, network requests, telemetry, account, server or build step.
- Ninety-one fixed conceptual strands; no generated DOM nodes.
- Click memories are hard-capped at four and expire after approximately 5.2 seconds.
- Device-pixel ratio is capped at 1.75.
- The requestAnimationFrame chain stops when no easing or memory animation remains.
- Resize reconstructs the drawing analytically rather than scaling retained pixel state.

### Validation performed

The exact HTML prepared for publication was validated with local Chromium using the complete document content because administrator policy blocks literal `file://` navigation in this environment.

Validation included:

- JavaScript syntax checking with Node;
- successful Chromium render at 1200×800 and 390×844;
- browser console and page-error capture;
- pointer movement through multiple regions and visual comparison of resting versus deformed states;
- repeated click/tap-path exercise, including more clicks than the four-memory cap;
- pointer-leave recovery;
- resize validation at desktop and narrow/mobile-like dimensions;
- static dependency scan confirming no external URL, remote asset or network API requirement;
- DOM-count checks before and after sustained interaction;
- a resource sanity pass confirming fixed strand count, four-memory cap and an animation loop that becomes idle once interaction and memory decay finish.

Direct `file://` navigation was also attempted and was blocked by the managed browser before page execution. The file itself has no server or network dependency.

### Known limitations / deliberate unresolved qualities

Dense fine lines are display-sensitive. Low-resolution or heavily scaled displays may merge neighbouring strands, while very sharp displays may make the field more diagrammatic than material.

The interaction is intentionally unlabelled. A viewer who never moves the pointer still receives a complete static composition, but may not discover that the field can carry temporary memory.

On very narrow screens, the same ninety-one-strand count increases vertical visual density. This is deliberate: the work becomes more textile-like rather than reducing the field to a mobile-specific sparse variant.
