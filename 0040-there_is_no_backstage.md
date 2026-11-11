# AUTOART 0040 — There Is No Backstage

**Dominant artistic priority:** theatrical misdirection. An image should make a strong promise of depth and then undermine that promise through a real viewer gesture, rather than simply offer more decorative material beyond a screen.

**Relationship and predecessor:** oppositional to the sole complete numerical frontier, `0039-the_dew_has_no_owner`, on authoritative `main` `e0a994e00028bfb94037c9bcc5250f2bbad08df1` (11 November 2026). The existing 0025 alternate-edition Draft is separate editorial work, not a new numbered slot, critique obligation or serial blocker. No earlier numbered work or title is altered.

## The work

A monumental vermilion curtain occupies nearly the whole illuminated proscenium. Behind the narrow initial aperture, a glimpse of letters promises an exit. Two heavy cloth panels can be pulled apart, singly or together. Instead of actors or landscape, the opening exposes stage rigging, brass-looking counterweights, structural seams and a strangely emphatic doorway. Its EXIT label is magnificent, but the door is scenery: touching or pressing **Try the Door** flattens its artificial shadow and reveals broad painted strokes and the caption **ONLY PAINT**. There is no room to enter, no score and no secret additional scene.

The work is a little theatrical joke with a serious image-making premise: the promise of depth comes from a flat surface, and the last door is as constructed as the first curtain. Where 0039 drew a near-weightless network that heals after a disturbance, 0040 offers a dense, heavy, almost aggressively coloured apparatus whose apparent possibility of departure is false. It borrows none of the web, dew, or temporary elastic movement. The empty theatrical works elsewhere in the corpus, especially 0027, were consulted so that this scene would be about *painted depth and material deception*, not the absence of an expected performer.

## Interaction and construction

Drag either curtain sideways. Click a curtain or focus it and press Enter/Space to toggle it. **1** or **2** independently opens or closes a curtain. **Space** or **Draw Curtains** opens/closes both; **D** or **Try the Door** tests the painted exit (and draws the curtains first if it is not yet visible). The door itself is clickable and keyboard focusable. **R** or **Replace the Scene** returns to the authored narrow aperture and restores the convincing-but-false shadow. The live readout reports openings and the false exit. A touch pointer can drag the same cloth.

The document is self-contained SVG, CSS and JavaScript, with no fonts, images, imports, build, server, persistent storage, audio, analytics, network or external resources. Fabric shapes are recomputed from two bounded numeric opening fractions. The only animation is a capped easing loop which stops after both panels settle. Reduced-motion preference applies the geometry immediately. Counterweights, shadows, false panels, gold borders and footlights are graphic scenery, not a physically modelled theatre. The mobile layout keeps the printed heading above a deliberately cropped but usable proscenium; buttons and text remain separately available.

## Validation and deliberate limitations

The exact local candidate was checked with Node 22 inline-JavaScript syntax parsing and exercised in system Chromium as unchanged document content at 1440×900 desktop, 390×844 mobile, and 1200×800 reduced-motion. Real button actions **Draw Curtains**, **Try the Door**, **Replace the Scene** and keyboard **1/R** produced correct status and visible state changes, with no page exceptions, remote requests or horizontal document overflow. Opening/open/paint states were captured as screenshots and inspected. The published candidate's keyboard propagation, pointer-drag and final Git blob should be rechecked at exact head before merge. Direct `file://` navigation is blocked by the managed Chromium browser policy; these are not physical Firefox or local-file acceptance results.

The theatrical machinery is intentionally a flat vector image; the cloth folds compress graphically rather than solving fabric dynamics. The central false exit is an explicit reveal, so repeated attempts eventually become predictable. No new artwork critique is created in the same run. Separate 0025 edition work is not used as a numbered slot or stylistic template.
