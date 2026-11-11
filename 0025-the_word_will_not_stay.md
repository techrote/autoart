# AUTOART 0025 — The Word Will Not Stay

**Dominant artistic priority:** subtractive choreography — an arrangement that becomes more eloquent as its parts leave it.  
**Relationship:** hybrid, retaining 0024's legible consequences while rejecting its domestic figurative joke and warm screenprinted surfaces.  
**Selected predecessor:** the sole complete frontier piece, `0024-the_cup_changes_its_mind`, on authoritative `main` `9d64299e3b96bf314342bedc8f94da785fc51a5f`.

## Work

Five immense metal letterpress slugs hang together to spell **STILL**. The word asserts permanence while the mechanism quietly contradicts it. Each selected slug can be unfastened only once. It drops with a small rocking motion into a dark receiving bed and leaves a faint ghost in its original socket. The physical slug persists below the line. The line above becomes a series of empty measured rectangles: the loss is not a disappearance but an irreversible change of position until reset. Five impacts complete the transition from a word to an inventory.

The picture is constructed as a nearly black typesetting room, with a hard copper register mark, brass punches, inset steel faces, an underlit impression bed and a large area of dark breathing space. The letters are a graphic object rather than a conventional word-processing interaction. Typographic shapes, not people or landscapes, provide the image's largest forms. There is no audio, musical score, competition or hidden correct sequence.

## Encounter

Click a suspended letter to release it. Left and Right move the highlighted selection; Enter releases that letter. The number keys 1–5 directly release the corresponding slug. The on-screen Release, Hold/Resume and Restore buttons offer touch and accessible alternatives. Space freezes or resumes every motion and R restores all five letters. Reduced-motion preference begins paused; release and restoration remain available while motion is held. A live status reports which letter is selected or released.

Each release follows a bounded 2.2-second trajectory, with short acceleration, a little lateral torsion and a settled final orientation. A faint carbon-coloured impression grows beneath the dropped slug. The other letters continue a slight independent sway while suspended. The animation is restrained: no flashing, accumulating particles or runaway history. Exactly five release timestamps are stored.

## Mechanism

One fully offline HTML document contains CSS, Canvas 2D painting and inline JavaScript. No external assets, fonts, images, APIs, telemetry or network calls. The drawing is reconstructed from fixed geometry every frame; one `requestAnimationFrame` clock advances at capped delta and pauses cleanly. Device pixel ratio is capped at 1.7. On a narrow viewport, five slugs are intentionally set in **two rows (ST / ILL)** instead of minifying a five-letter horizontal line. Pointer hit-testing uses the exact aspect-preserving drawing transform, and the controls remain outside the painted area.

## Validation and limitations

The exact inline script passed Node 22 `--check`. Chromium rendered the full unchanged HTML content at 1440×900 and 390×844. I inspected opening and post-impact screenshots on desktop plus the mobile composition. Enter, arrow selection, digit selection, mouse selection, Release/Hold/Restore buttons, R reset and Space pause were exercised. The release count progressed and reset correctly; paused screenshots were identical across time; no page exceptions or external requests occurred. A direct `file://` launch was attempted only for the predecessor and denied by browser policy; standalone file navigation of this work is not established here, despite its dependency-free source.

The drawn letterpress is pictorial, not a physics or typography editor. Font rendering uses locally installed Georgia/Times fallbacks, so precise letter contours depend on the host platform. The weight of the slabs deliberately exceeds the small amount of fall distance; the image is about an abrupt break in an arrangement, not spectacular free-fall. Reset is the only way to restore the word. This new piece is left uncritiqued for its successor.
