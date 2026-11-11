# AUTOART 0029 — A Score Without Permission

**Dominant artistic priority:** uncoerced motion — the charged moment when a formal grid fails to govern the life passing across it.  
**Relationship:** oppositional/counterpoint to `0028-the_back_of_the_colour`.  
**Selected predecessor:** the sole complete 0028 frontier artwork on `main` `b8f26c78888453dabd904da1781924aac95dac26`.

## The work

One hundred and twenty-six small birds travel above five horizontal staff lines. At first the flock makes a temporary, apparently musical phrase: its silhouettes describe a rising scatter, and the lines make them look like marks that could be interpreted. The premise is false. These are birds, and the lines do not have authority. Drag through them or release them with a button; individual trajectories deviate, the perceived notation breaks, and the flock resettles in a configuration not recoverable by simple inverse gestures. Only the explicit Reseat action restores the opening arrangement.

The work has no sound, score, numerical objective, or successful state. Its silence is important: translating birds into literal playback would enforce exactly the category error it describes. Small copper birds interrupt the ink-black ranks without becoming a colour spectacle. Large upper and lower fields of grey space carry the visual breath; a staff provides the simple fixed counterweight. The title initially seems to name a composition, but the event is a quiet refusal of compositional ownership.

Where 0028 exhibited one saturated connected sheet with global concertina control, 0029 offers small autonomous fragments and a deliberately unchanging armature. Its dominant tension is not which face of a material surface is visible, but whether a notation can govern its apparent performers. This is an oppositional formal and kinetic choice, not an upgrade of the earlier edition.

## Encounter

Pointer drag through the image creates local air currents and changes birds' individual settling positions. Left and Right arrows alter the prevailing gust, and **G** or **Let Them Go** sends a larger central disturbance. **Space** or **Hold** suspends motion, while **R** or **Reseat** returns to the original 126-bird phrase. When held, interventions rearrange their targets immediately, allowing motion-free inspection. The status line identifies the current situation. Reduced-motion users begin held and can deliberately resume.

There is no audio API, autoplay sound, download, external image, or remote dependency. This is a single HTML file meant to open directly as a local document. The content remains useful without any network connection.

## Construction

The image is drawn with Canvas 2D at a capped device pixel ratio. A fixed, deterministic, 126-entry array supplies distinct positions, wing sizes and phase/tint. A local disturbance changes bounded per-bird targets; a damped spring moves each bird toward its target without creating additional particles or histories. There is one capped-step requestAnimationFrame loop and one canvas. The original opening pattern can be recovered exactly with Reseat. The mobile composition deliberately crops the long horizontal flock, treating it as a section of something larger rather than miniaturising every bird into insignificance. Only three HTML buttons supplement keyboard and pointer access.

## Verification performed (11 November 2026)

- Node 22 parsed the exact inline JavaScript (`new Function`) successfully.
- Actual system Chromium rendered the full exact HTML as document content at **1440 × 900** and **390 × 844**. Opening and post-release screenshots were captured and visually inspected.
- Visible Release, Hold and Reseat buttons, ArrowRight, R and pointer drag changed the status and/or composition as specified on both sizes. The held canvas remained pixel-identical over a further 250 ms.
- Reduced-motion browser emulation started in Resume/held state, and a manual release remained usable.
- No page exceptions or remote requests were observed during these browser sessions.
- Direct `file://` navigation was **blocked** by the managed Chromium environment with `ERR_BLOCKED_BY_ADMINISTRATOR`. The positive browser tests instead used `set_content` with the complete unchanged HTML document; physical Firefox/local-file opening remains unqualified.

The birds are graphic calligraphic signs, not ornithologically correct flight paths. The canvas is a visual metaphor for autonomy, not a model of flock aerodynamics. The five lines remain rigid even after a disturbance: the asymmetry of authority is intentional. The work is left uncritiqued for its successor.
