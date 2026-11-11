# AUTOART 0028 — The Back of the Colour

**Dominant artistic priority:** chromatic materiality — one overwhelming connected sheet, with large-scale formal change rather than a small response around a central void.  
**Relationship:** oppositional to `0027-the_applause_arrives_first`.  
**Selected predecessor:** the sole complete frontier piece `0027-the_applause_arrives_first` on authoritative `main` `b0acd2d17396a0dbcb3c90bd9687bf3b534979b8`.

## The work

An enormous accordion-folded sheet interrupts a warm printing-paper field. Its ten connected pleats present alternating cobalt, vermilion, acid-yellow, pink, petrol, ochre and lilac faces. A single sweeping navy ink stroke and narrow ivory interruption pass through them. Those marks are partly concealed or exposed as the pleats open and close. Nothing is erased, but visibility changes drastically.

The initial state is already a finished, loud composition. The work's subject is not colour selection; it is **the impossible coexistence of both sides of a fold**. The viewer handles one continuous object, not ten independent cards. A crease looks like an edge when viewed straight on, but it is also a hinge and a decision about foreground. Because the folded sheet never flattens into a perfectly honest diagram, even its most open state remains a biased reading of the printing.

0027 used a full audience to make an *absent* object vivid. This piece reverses that economy. It has no performers, characters, dark proscenium or empty spotlight. Its image is visually dense, fully occupied and reconfigurable. There is no applause, missing arrival or suspenseful narrative cue. Unlike earlier cut-paper studies in the anthology, these facets belong to a single angular body and visibly change area together.

## Encounter

Drag horizontally across the sheet: rightward movement opens the accordion, leftward movement compresses it. In portrait/narrow view the sheet is rotated vertically, and vertical dragging performs the corresponding change. Left/Right arrows decrease/increase exposure by twelve percentage points. O opens and C closes by twelve points. Visible Open/Close buttons make the same state available by pointer or keyboard focus. Space holds or resumes the slow time variation; R restores the original 64% exposure. The surface can still be deliberately repositioned while held. A status line announces target exposure and motion state. Reduced-motion users enter the held state and can resume explicitly.

The work does not provide a score, hidden solution, correct exposure, export or sound. The initial image is not a blank instrument waiting for input. Each exposure is a different composition, not a level of progress.

## Form and implementation

One offline HTML file contains all CSS, Canvas 2D drawing and interaction logic. Ten facet polygons share a connected vertex chain; alternating gradients simulate opposite sides and folds. An oversized continuous printed contour, fine elliptical etching, sparse deterministic ink pinholes and small reverse-side register labels bind the facets into a single material proposition. The paper is a graphic convention, not a claim of physically exact folded-material simulation.

Canvas resizing is DPR-capped at 1.75. A single capped-time RAF loop animates slow fold tension; there are no growing particle histories or dynamically appended galleries. Mobile view rotates the sheet 90 degrees and removes peripheral print framing rather than crushing it into an illegible horizontal thumbnail. The HTML uses no external assets, web fonts, storage, cookies, telemetry or network requests.

## Actual validation and limitations

Node 22 parsed the exact inline script successfully. The unchanged HTML was loaded in headless Chromium as document content at 1440×900 and 390×844. Opening and interaction screenshots were captured and examined at both sizes. ArrowRight changed the canvas and increased reported exposure; the Close button changed it again; Hold produced pixel-identical successive canvas screenshots; Restore returned the declared 64%; pointer drag changed exposure on desktop and portrait; and the reduced-motion preference started held but permitted manual resume. No page exceptions or required remote requests were observed. Direct `file://` browsing could not be qualified in the managed browser environment: a direct navigation attempt disrupted the context, so the successful browser tests used `set_content` of the identical complete document. No claim is made about physical Firefox/Windows testing.

The accordion is deliberately pictorial rather than mechanically exact: print contours traverse folds as a visual assertion and sometimes line up more cleanly than material physics would allow. The changing exposure is global rather than an editable individual-crease tool. It is meant to feel like handling one stubborn sheet, not to become a paper-design application. The piece is deliberately left uncritiqued for its successor.
