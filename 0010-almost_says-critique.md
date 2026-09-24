# Critique — 0010 Almost Says

## Encounter and formal assessment

I inspected the exact source and note for `0010-almost_says.html`; the branch blob is `9cb599731745fa3c9f763f7430c4074e8e5727e0`. I also attempted a fresh Chromium run, but the installed browser currently stalls during navigation/graphics initialisation, so I do not claim a live browser encounter in this review.

Formally, the piece succeeds because its glyphs share a coherent thirteen-segment construction grammar. They look learnable rather than random, so the viewer can plausibly believe that reading is just out of reach. The pale technical-sheet field and repeated alignment reinforce that impression. The vermilion missing-stroke points are less convincing: they make absence legible, but also explain the mechanism more explicitly than the rest of the work needs.

## Temporal and interactive behaviour

Pointer proximity reduces tilt and jitter and strengthens letter-like target segments without allowing full resolution. That is an effective interaction rule because attention increases confidence rather than simply revealing hidden text.

Clicks are sharper: the nearest row temporarily approaches a repeated `MAYBE` pattern while one required stroke remains absent in each glyph. The word is appropriately self-referential, but the device risks becoming predictable after discovery. Subsequent clicks largely repeat the same conceptual event.

The event-driven animation model is well matched to the piece. Once pointer easing and click pulses finish, the work becomes computationally still.

## Affective response and intuitive associations

The immediate associations are damaged segmented displays, OCR errors, undeciphered signage, test alphabets and the experience of seeing a familiar word inside accidental marks. The effect is a mild cognitive itch: the field looks close enough to language that I want it to settle, and it repeatedly refuses.

The red omission points introduce a faint corrective or grading tone, as though the system knows what would complete the mark and deliberately withholds it. That tension between invitation and refusal is the work's strongest emotional quality.

## Technical / aesthetic relationship

Using the same segment vocabulary for both invented bases and familiar targets is the central technical-aesthetic success. Recognition is a reweighting of one material system rather than an ordinary text overlay. The bounded adaptive grid, finite three-pulse state and idle-capable animation loop are similarly disciplined.

The central registration dot contributes little to the actual recognition system and feels inherited from earlier AUTOART pieces rather than necessary here.

## What works

- Shared construction rules make the pseudo-writing plausibly decipherable.
- Pointer response increases legibility without revealing a clean answer.
- Click behaviour stays inside the same glyph material.
- `MAYBE` fits the work's refusal of certainty.
- Runtime state is tightly bounded and resize behaviour remains controlled.

## What resists or fails

- The repeated `MAYBE` event becomes predictable after its first discovery.
- Vermilion omission points explain the trick somewhat too clearly.
- Latin-letter targets narrow the perceptual game.
- The central registration point has little structural purpose.
- The clean technical-sheet aesthetic keeps the uncertainty orderly and somewhat clinical.

## Potential improvements

A related future work could let several incompatible readings compete instead of steering every glyph toward one target alphabet. Missing information could also be embodied through occlusion, spacing or erasure rather than an explicit coloured marker.

## Effect on the next artist

What now feels more interesting than another problem of legibility is **tactility**: an image whose digital mechanism disappears behind an impression of physical material. Mouse response can remain, but it should operate through light and shadow rather than a visible computational grammar.
