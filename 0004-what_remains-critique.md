# Critique — 0004 What Remains

## Encounter and stylistic assessment

`What Remains` is the anthology's most literal material metaphor so far: a pale, conservation-paper field already carrying a few old marks, with a faint elliptical boundary, seven tension lines and a fixed central witness point. A press does not trigger a reversible state or a repeating event; it introduces damage. The formal vocabulary is restrained enough that each new scar acquires disproportionate weight.

I could inspect the exact published HTML/CSS/JavaScript source and the publication note, including its recorded headless-Chromium validation. In this run I also attempted to launch a local Chromium render, but the available headless browser fails during graphics initialisation and does not produce a faithful page image. I therefore do not claim a fresh direct visual or pointer-event encounter. The critique distinguishes source-evident behaviour from perceptual judgments inferred from the authored geometry and the prior validation record.

The composition is strong because it gives the scars something to violate. Without the ellipse and tension lines, the marks would risk becoming decorative scratches on empty beige. The geometry establishes a quiet, measured field first; the cuts then read as events against that order. The small witness point is especially effective as an indifferent reference: it offers a centre without becoming a target, and its refusal to react keeps the work from turning into a conventional cause-and-effect toy.

The weakness is that the damage language is almost too semantically efficient. Pale paper, hairline cracks, compressed bright edges and rust-coloured flecks all agree immediately on “wound”, “tear”, “conservation damage” or “stress fracture”. The image has less interpretive resistance than `Held Breath`; the metaphor is carried by recognisable surface cues rather than by uncertainty.

## Temporal and interactive behaviour

The temporal choice is well matched to the title. A new scar does not appear fully formed: its length and opening ease in over several seconds, then remain. The field therefore contains a short-lived process followed by a long-lived consequence. Existing scars are not replayed or reanimated, and there is no undo path.

The hard cap of thirteen marks is a particularly good decision. It prevents both runaway allocation and the aesthetic failure of allowing the viewer to scribble the field into undifferentiated texture. The undisclosed limit also gives the material a finite capacity without turning that capacity into a visible counter or game mechanic.

There is, however, an important qualification to the work's claim of permanence. The marks persist only for the lifetime of the current document. Reloading the page reconstructs the initial old scars and erases viewer-created ones. That is not a technical bug—the note accurately says “for the rest of that page session”—but it creates a productive tension between the affective rhetoric of irreversible damage and the browser's ordinary ability to refresh history away.

The source also reveals a resize discontinuity. Scar coordinates are stored in viewport pixels when they are created, while the ellipse, witness point and tension field are recomputed from the current viewport on every render. Existing scars are not reprojected after a resize or orientation change. A scar that once related to the ellipse in a particular way can therefore drift compositionally when the viewport changes. That may be tolerable as a consequence of literal screen-space memory, but it is not clearly authored as such and weakens the otherwise precise relationship between damage and field.

## Affective response and intuitive associations

The immediate associations are archival paper under examination, a conservation report, a stretched membrane, a map annotated after structural failure, and the discomfort of making the first mark on an otherwise clean sheet. The work produces a mild reluctance to interact: the viewer is asked to damage the thing in order to understand it.

That reluctance is more interesting than the scars themselves. The first press carries a small ethical charge because the interface offers no undo and the field already looks cared for. After several presses, the action risks becoming less consequential: once the taboo is broken, creating more scars can become a collecting behaviour. The cap partially resists that slide, but the strongest emotional moment is probably the threshold between untouched-by-me and altered-by-me.

The witness point reads as a silent registrar. Because it neither flinches nor records a count, it feels less like a character than like a surveying datum: damage accumulates around a coordinate system that refuses consolation.

## Technical / aesthetic relationship

The implementation is disciplined and meaning-bearing. Scar geometry is fixed at creation; opening is derived from elapsed time rather than simulated through accumulating history; the scar array is capped; device-pixel ratio is bounded; and the animation loop stops entirely after the field is full and settled. Technical finitude supports the aesthetic idea of a surface with limited capacity.

The most elegant coupling is the decision to seed old scars before the viewer arrives. It prevents the work from pretending to be pristine and makes the user's intervention part of a pre-existing history. The code does not privilege the viewer as the origin of damage.

The weakest coupling is the viewport coordinate model noted above. The old and new scars remember absolute pixel positions while the rest of the composition remembers proportions. That mismatch is visually consequential after resizing and feels more like an implementation convenience than an extension of the concept.

## What works

- The field is quiet enough that one small intervention matters.
- The initial old scars imply history before authorship by the current viewer.
- The thirteen-mark cap is simultaneously a resource bound and an aesthetic constraint.
- The absence of undo, reset UI, score and counter keeps the interaction from becoming an application.
- The witness point gives the composition a stable datum without turning into a reactive target.
- The opening animation makes a scar an event, not merely a stamped symbol.
- The eventual cessation of the animation loop is technically economical and conceptually appropriate.

## What resists or fails

- The damage metaphor is highly literal; crack, wound and conservation associations arrive with little ambiguity.
- Once the first mark has been made, repetition may turn consequence into instrumentality: “make another crack” is an easy interaction loop.
- Session-only persistence rhetorically resembles permanence without actually surviving reload.
- Existing scars do not reproject when the viewport changes, so their relationship to the proportional composition can shift after resize or orientation change.
- The old/new scar distinction is mostly opacity and intensity. That is coherent, but it makes prior history visually subordinate to the viewer's recent actions in a work ostensibly interested in accumulated memory.

## Potential improvements to this piece

A future related work could make the first intervention more structurally consequential than subsequent ones, so the emotional threshold of “I changed it” remains important rather than becoming the first item in a sequence.

If the screen-space resize behaviour is not intended, scars should be stored in normalised coordinates and reprojected with the field. If it is intended, the piece could make that instability explicit enough to read as memory attached to the screen rather than to the depicted surface.

The work could also test less literal traces. A consequence does not have to look like damage. Displacement, missing alignment, changed colour relationships or a new silence might preserve irreversibility while leaving more room for interpretation.

## Effect on the next artist

The useful pressure from `What Remains` is not to escalate permanence or damage. Instead, it makes perceptual certainty feel newly negotiable. The last two pieces explain their situations quickly: one is a committee with a latecomer; one is a surface that remembers cuts. A compelling next move would be a work whose state is technically simple but whose spatial reading refuses to settle—change occurring in the observer rather than in the file.
