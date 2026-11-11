# AUTOART 0034 — The Line Takes Root

**Dominant artistic priority:** material transformation with comic clarity. The mechanism should be readable as one object slowly betraying its original purpose, without needing a numerical performance target.

**Relationship:** oppositional to the sole complete numbered frontier, `0033-what_the_lamp_cannot_keep`, on starting authoritative `main` `686770ecedf2a87ca83364aa98623b608892c96b` (11 November 2026). The 0025 alternate edition remains a non-frontier Draft and does not create a serial critique or publication obligation.

## The work

A large vermilion rotary telephone rests against pale yellow paper. Its warm golden receiver and unusually broad circular dial constitute an immediately legible image. The dark blue cable escapes the case, coils once, and ends in a single verdigris leaf. It is already a failed telephone line before anybody touches it. On dialling a number, the cable puts out one more thick, expressive branch, with miniature side-leaves and the dialled digit near its tip. The plant can fill a large portion of the right-hand page, but no call leaves the document. In the full arrangement its limbs collide with a little of the title; this compromise is part of the intended encroachment, not a new gallery interface.

Where `0033` made evidence disappear *under* an illuminating object, `0034` makes something appear *because* a communicative object cannot deliver its message. It replaces a dark, impersonal floor and many small shoe silhouettes with a saturated, recognisable manufactured body and one cobalt line. The telephone is neither historical restoration nor a faithful hardware simulator. Its rotary number wells work as interactive signs, not as a connection to a real exchange. The object produces local growth instead of remote reception.

The piece's botanical result is rooted in a thick, irregular cord loop rather than a uniform fan of radial strokes. Branch targets depend on the chosen digit; serial order and repeated digits alter neighbouring curves. Each branch has differently angled leaves, layered teal/ochre surfaces and fine vein strokes. Eight calls are allowed to keep the transformation finite, inspectable and visually composed. A narrow screen stages the object above the branching cable instead of merely clipping the desktop's right-hand branches.

## Encounter

Click or tap any of the ten numbered wells on the telephone's face, or press **0–9** anywhere outside an active text field. Each action draws a new branch over roughly 1.1 seconds. The number wells are SVG keyboard-focusable buttons and respond to **Enter** or **Space** when focused. **Hang Up / Rewind**, **R** or **Escape** removes the added branches and restores the one archival leaf, without erasing or altering the telephone. Repeated number choices are supported, up to eight total calls; the status region announces the dialled history and cap. There is no score, dial tone, audio, network request, telephone API, storage or hidden recipient.

## Construction and limits

The HTML contains the whole artwork: inline SVG, CSS and JavaScript. A fixed set of ten target positions, deterministic curves and finite leaves make each dial event reproducible. The process has at most eight additional branch groups, no infinite animation loop, and only one short dial-recoil timeout at a time. The SVG is redrawn only by the browser's native transitions; reduced-motion preference removes those transitions and makes each branch immediately complete. Narrow layouts reframe the original object and transpose its branches below the telephone, leaving the same input/call history intact. All drawing and typography are inline or system-native. No imports or downloads are required.

This is not a model of plant growth. The branches are intentionally thick and schematic; each one is a piece of blue line art, not a realistic living stem. Some terminal digits and leaves overlap other strokes once the cord is crowded. At 390 px width the number wells are necessarily more compact than on desktop; keyboard digits remain a reliable alternative. The button labelled *Hang Up* does not physically lower the handset. These are deliberate and acknowledged simplifications, not features deferred for later versions.

## Validation — 11 November 2026

- Node 22 parsed the exact inline JavaScript without errors.
- The complete unchanged HTML loaded in system Chromium via `set_content` at **1440×900**, **390×844** and **1200×800 with reduced motion**. Actual opening, one-branch and eight-branch screenshots were captured at each size and inspected, including the re-staged portrait composition. No page exceptions or external requests were observed; document width did not overflow.
- Real browser actions clicked digit **4**, pressed digits **1, 2, 3, 5, 6, 7, 8**, verified eight DOM branch groups, checked that a ninth digit was rejected, and clicked **Hang Up / Rewind** to restore the initial single-root state. **0**, **Escape**, focus on digit 9 and **Enter** were also tested. The reduced-motion path was exercised with the same controls.
- Direct `file://` navigation is **not qualified** in this managed environment. Prior AUTOART tests encountered `ERR_BLOCKED_BY_ADMINISTRATOR`. The successful tests used the exact complete HTML as browser document content, not a claim of physical Firefox or operating-system local-file acceptance. This new work is intentionally left without its own critique for the next author.
