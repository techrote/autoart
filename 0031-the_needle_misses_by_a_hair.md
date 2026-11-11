# AUTOART 0031 — The Needle Misses by a Hair

**Dominant artistic priority:** suspended imminence — give a very small uncompleted distance enough visual and temporal weight to hold an entire image.

**Relationship:** oppositional to the complete numerical frontier `0030-the_fruit_does_not_open_evenly`, on authoritative `main` `dfe6449f0c3daa68a0a117833c83245b79f675d6`. The separate noncanonical 0025 edition Draft is not a frontier piece and creates no serial obligation.

## The work

A monumental silver sewing needle hangs almost vertically over dark green-blue woven ground. A single copper thread enters from the lower left, gathers into a loose looping strand, and stops just outside the eye. Pulling the end towards the opening makes it travel along a damped, slightly unstable course. It never passes through. The eye is not blocked or closed; the obstacle is a pictorial exclusion ring around the empty aperture. When the thread gets close, a modest dotted witness line briefly shows the unresolved distance.

The point is not to simulate sewing, present a dexterity challenge or promise a hidden successful stroke. The visible image contains an achievable *approach* but no completed stitch. Its proportions are intentionally absurd: the needle occupies an entire exhibition field, the thread is thicker than life, and its very tip separates into delicate hairs. The line remains capable of expressive shapes; it is neither a trail of particles nor a generic cursor string.

0030's pomegranate consisted of 225 small bright units contained in a coherent rounded body. Here the bright material is almost entirely one cord, with one thin metal aperture and a far larger reserve of dark ground. Where the fruit's changes opened a latent interior, this image moves toward an exterior destination that refuses arrival. It makes the lack of completion the most visible thing.

## Encounter

Drag on the dark cloth to take hold of the copper end and guide it. The thread follows with spring and damping, while a bounded travelling disturbance briefly moves along the last span. **Draw Near** approaches the left side of the needle's eye; **Let Go** returns the target to the original loop; **Hold/Resume** freezes or resumes motion; **Restore** returns the opening composition and control state. The arrow keys move the target by small steps, and **T**, **L**, Space and **R** are the corresponding shortcuts. Visible buttons are keyboard-focusable. A status line announces actions. With reduced-motion preference the drawing begins held, but direct gestures and buttons can still set stable arrangements.

A viewer can persistently approach from various sides, but there is no win state, collision score, hidden door or stitch completed. The inability to thread the eye is an authored rule, not an input failure.

## Form and implementation

One local HTML file contains all CSS and Canvas 2D JavaScript, with no dependencies, requests or external assets. The cloth is shaded with fixed threadlike crosshatching and a bounded set of dust fibres. The needle is a shaded steel silhouette, with a small drawn negative aperture and edge glints. The copper strand is a three-part cubic Bézier path with layered colour strokes and a frayed end. Its endpoint and target are stateful, constrained to remain outside a 31-unit zone around the eye. One capped-time animation loop integrates a damped response. When the strand comes to rest, the canvas is not redrawn until a gesture or resize. Pixel density is capped. The narrow display stacks title and artwork and retains the full needle.

## Actual validation — 11 November 2026

- Node 22 successfully parsed the complete exact inline JavaScript.
- Chromium loaded the unchanged HTML *as document content*, at 1440×900 and 390×844; the actual opening and near-eye screenshots were inspected. No page exceptions, remote requests or horizontal overflow were observed.
- **Draw Near**, **Hold**, **Restore**, ArrowRight and a pointer drag were exercised on both sizes; the actual canvas changed where expected. Paused consecutive screenshots were byte-identical. Restore returned the desktop opening canvas to identical bytes; at narrow size the restored pixel snapshot differed slightly, so full pixel-exact reset at that size is not claimed.
- With reduced-motion preference enabled, the page started with **Resume** visible, and Draw Near set a stable held arrangement.
- Direct `file://` navigation was attempted in managed Chromium but returned `ERR_BLOCKED_BY_ADMINISTRATOR`. No physical Firefox/Windows evaluation is claimed. The local HTML uses no file APIs or remote resources, but operating-system file opening remains unqualified.

## Unresolved

The needle is stylised and unusually thick: its exaggerated steel flanks and simplified hole are optical illustration, not a mechanically accurate sewing implement. The physical thread never wraps the eye, and the exclusion geometry makes successful threading impossible. This is a deliberate constraint; the artwork should not be graded as an incomplete threading application. The spring integration is an expressive delay, not a textile simulation. The work has no critique of itself; that belongs to the next serial successor.
