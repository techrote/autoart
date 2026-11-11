# AUTOART 0030 — The Fruit Does Not Open Evenly

**Dominant artistic priority:** embodied abundance — make the interior of one material object visually compelling before any gesture, and let interaction expose the unevenness of its construction rather than scatter its parts.  
**Relationship:** oppositional to `0029-a_score_without_permission`.  
**Selected predecessor:** the sole complete numbered frontier piece `0029`, on authoritative `main` `28fe5f02c8fe0acbd104dff0cdd4812d119f0331`. Noncanonical edition files and the open 0025 alternate-edition Draft were not considered anthology frontier or missing critiques.

## The artwork

A single pomegranate cut into five chambers dominates a warm botanical print. Two hundred and twenty-five individually shaded ruby arils remain lodged inside irregularly edged cream pith. The viewer can part one chamber or all five; each wedge withdraws along its own radial direction and at a different speed. The result is not a fruit being eaten or emptied. No aril drops; no inventory decreases. The narrow dark fissures reveal the underlying fibrous centre before the pieces return. The fruit can be made to open, but it refuses a single agreed rate of opening.

The subject was selected precisely because it is almost the inverse of 0029. The predecessor placed many tiny, dark, apparently independent birds on a pale grid. Here the many small signs are *seeds* contained inside a giant coherent object. A red-gold body, not a horizontal notational line, supplies their larger structure. The enclosing rind, pale connective membranes, glossy irregular jewels, darker centre and papery crown all share a physical scale. The composition borrows the formal confidence of an old botanical plate without claiming anatomical fidelity. Its title is also the work's observable mechanical proposition, not an instruction to solve a puzzle.

## Encounter

Click or tap a chamber, or use keys **1–5** to part a specific wedge. Arrow Left/Right select a chamber, and Enter parts or returns it when focus is not on a button. **Part This Chamber**, **Open All Five**, **Hold/Resume** and **Restore** are visible buttons. **A** parts or returns all; Space holds time; **R** restores the entire fruit. A status line announces chamber and action. When time is held, parting jumps to its chosen arrangement immediately, making a stable close inspection possible. Reduced-motion preference starts in the held state; the viewer may explicitly resume.

The five wedges have different bounded relaxation rates; the darkest gaps become visible asynchronously. At rest nothing needs to happen. There is no automatic tally, win condition, sound or falling-particle shower. The work is meant to be looked at as much as operated.

## Construction

The one HTML file contains all styling, Canvas 2D drawing and JavaScript. Seed positions, saturation and sizes are generated from a fixed deterministic formula at startup; the 225 seed records and 110 paper flecks are fixed in number. Five chamber records hold bounded openness and target values. Each frame redraws five irregular closed cut wedges, their flesh gradients, arils, pith ridges and the shared plum-and-gold fibrous cavity. The device-pixel ratio is capped. At rest a drawing is only requested when an intervention or resize occurs; one capped-step requestAnimationFrame loop provides time for transitions.

At narrow widths the page reflows to a vertical exhibition print. The full fruit remains visible rather than being cropped, while fine colophon text inside the canvas is omitted. Every graphic is authored with local geometry. There are no external assets, font downloads, telemetry, network calls, audio APIs or persisted settings.

## Validation performed — 11 November 2026

- Node 22 successfully parsed the exact inline script with `new Function`.
- System Chromium loaded the complete unchanged HTML document content at 1440×900 and 390×844, plus a reduced-motion context at 1280×800. Opening and parted screenshots were captured and inspected. No page errors, remote requests or horizontal overflow were observed in those tests.
- Visible buttons parted the first wedge, opened all five, held transitions and restored the initial fruit. Paused canvas pixels remained identical across the observed interval, both desktop and mobile.
- Number key 5, ArrowRight, Enter on the artwork, A and R were exercised with announced state changes. A pointer press on the canvas selected and parted its corresponding wedge.
- The reduced-motion context entered with **Resume** shown and allowed deliberate controls. The stage remains usable at ordinary and narrow widths.
- The managed browser refused direct `file://` navigation; the successful tests used the *complete unchanged HTML as document content* in Chromium. Physical Firefox or OS-local-file opening has not been qualified. There is no browser screenshot claim about a physical desktop GUI.

## Unresolved

The segments are an illustration of sections, not a physically or botanically accurate dissection. Their geometric edges are deliberately regular enough to read as five chambers, while the outer rind and seed placements introduce small organic irregularities. The response is intentionally modest after the first full opening; this is a finite close-looking experience, not an infinite procedural instrument. The abundance of similar seeds is deliberate and may feel decorative to someone who requires every small form to move independently. The work is left without a critique for the next artist.
