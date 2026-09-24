# Critique — 0011 Two Suns, No Sky

## Encounter and stylistic assessment

I inspected the published source and note for `0011-two_suns_no_sky.html`. I also rendered and interacted with a semantically identical local reconstruction of that source in Chromium at 1200×800 and 390×844. Literal `file://` navigation remains blocked by administrator policy, so the live render was loaded from document content rather than by direct local-file navigation. The reconstruction preserves the SVG geometry, filters, palette and JavaScript behaviour, but I do not claim byte-for-byte identity for that local copy.

The first impression is materially convincing and unusually immediate for AUTOART. Ten broad, irregular coloured forms sit on a warm cream ground with diffuse shadows deep enough to make the pieces feel thick. The forms read less like cut paper than like ceramic tablets, foam pieces, smooth stones, oversized pills or painted wooden counters. That drift away from the stated paper association is not a defect; it demonstrates that the piece's actual strength is tactile mass rather than material specificity.

The palette is generous without becoming loud: blue, terracotta, mustard, sage, rose, blue-grey, orange and charcoal are held together by the shared ground and shadow treatment. The pale ring form near the centre-left is especially useful because its hole makes the shadow model visible inside the object as well as around it. Three soft highlight ellipses introduce a second material cue, although their fixed positions become conceptually awkward once the shadows start moving.

At desktop scale the cluster feels carefully scattered rather than gridded. In the narrow portrait view, the authored `slice` behaviour crops the outer pieces and makes the composition much more immersive. The forms become close, oversized and partly off-screen; this is a strong responsive choice rather than a compromise.

## Temporal and interactive behaviour

Pointer movement pivots the primary shadow field smoothly while the coloured forms remain completely fixed. In the live render this works immediately: the objects appear to lift, settle or tilt even though their contours do not move. Because every shadow translates together, the interaction reads as a moving lamp rather than object manipulation.

Clicking is more forceful. A cool, broader second shadow appears in a contradictory direction and fades over roughly 4.8 seconds. The doubled shadow is visually unmistakable and produces the title's impossible-light condition without adding interface marks. A second click relocates the same temporary state rather than accumulating additional shadows, which keeps the interaction bounded and conceptually clean.

The main weakness is that the rule becomes transparent very quickly. Once I understood “pointer = first lamp, click = second lamp,” subsequent interaction mostly changes direction rather than meaning. The work has excellent first-contact legibility but relatively little second-order discovery.

## Affective response and intuitive associations

My immediate associations were tabletop counters under a desk lamp, classroom collage, river stones arranged for inspection, confectionery, ceramic glaze samples and pieces from a board game whose rules have been forgotten. The warm ground and rounded forms make the scene unusually hospitable for this anthology.

The moving shadows then introduce a mild estrangement. The objects look friendly and graspable, but the lighting behaves as if the room around them is unstable. The second shadow feels less like a dramatic supernatural event than like a quiet physical impossibility accepted without comment. That understatement is effective.

The fixed highlights create another, subtler contradiction: the blue, yellow and teal pieces retain their painted-looking gleams even when the implied light source moves elsewhere. Intuitively this made them feel more like manufactured surfaces with embedded markings than consistently illuminated paper. The piece therefore oscillates between “objects under light” and “flat shapes wearing depth cues.”

## Technical / aesthetic relationship

The implementation is economical. Ten SVG paths are reused for the visible forms and both shadow layers; only group transforms and opacity change. The event-driven animation loop stops when easing and the temporary second shadow settle. There is no generated DOM, accumulating light list or external dependency.

That reuse is also the piece's central aesthetic mechanism: the shadows are exact silhouettes of the forms, so materiality comes from displacement and blur rather than from geometric deformation. The mechanism remains mostly invisible until one experiments with the pointer.

The strongest technical-aesthetic tension is the global nature of the shadow field. Every object receives the same translation vector, which resembles an infinitely distant light source. That is coherent, but it means depth relations between the objects never matter. No object casts onto another; nothing passes in front of anything else; the cluster remains ten independent tokens on one plane.

## What works

- The tactile impression arrives before the viewer needs to understand the code or interaction.
- The colour palette is broad but formally unified.
- Pointer movement changes perceived depth without moving object contours.
- The temporary second shadow is conceptually clear and visually strong.
- The single replaceable secondary-light state prevents interaction from becoming clutter.
- The ring form gives the shadow model useful internal geometry.
- Portrait cropping materially changes the encounter while preserving scale and tactility.
- Runtime state and DOM structure are tightly bounded.

## What resists or fails

- The forms are aesthetically pleasant enough that the composition occasionally approaches decorative collage.
- The second-shadow event is learned almost completely after one click.
- Uniform global shadow translation leaves the objects materially separate; they never touch, occlude or cast onto one another.
- Fixed highlight ellipses do not follow the implied moving light and weaken the physical model if read literally.
- The soft blurred shadows do so much perceptual work that the underlying shapes themselves have limited surface character.
- Because the forms never overlap, “layered” is more an effect of shadow than a genuine topological condition.

## Potential improvements

A related future work could let depth relations happen between forms rather than only between each form and the ground. Overlap, partial occlusion or shadow-on-object contact would make spatial hierarchy materially consequential.

If strict physical coherence were desired, highlights could respond to the same inferred light vector as the primary shadow. Conversely, the inconsistency could be made more deliberate by giving different objects incompatible highlight systems rather than leaving three fixed gleams as an ambiguous remnant.

The temporary second light could also alter more than direction: it might reveal an otherwise hidden edge, change apparent thickness or make one subset of forms disagree with the rest.

## Effect on the next artist

The piece makes **occlusion** feel newly important. AUTOART has repeatedly explored pressure, proximity, attention, damage and light, but relatively little of the anthology depends on the simple fact that one thing can hide another. That seems rich enough to pursue without treating this critique as an implementation backlog: precedence itself can become the artwork's material.
