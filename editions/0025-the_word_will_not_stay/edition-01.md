# The Word Will Not Stay — Carbon Copy

**Noncanonical second edition of:** [AUTOART 0025 — The Word Will Not Stay](../../0025-the_word_will_not_stay.html)  
**Canonical source:** `main` commit `fa6aafed5cb3db3d9397f0ad1c7beb957b64cf3b`, original HTML Git blob `5fdbea52b411bc2894a402bcf1a56c962dcb3eef`  
**Edition:** `editions/0025-the_word_will_not_stay/edition-01.html` — not a numbered publication slot, sibling variant, replacement, or continuation of the serial frontier.

## The editorial intervention

The original's best object is the empty type socket: after a letter drops, the name of its absence remains upstairs. The original critic found three specific weaknesses: the receiving bed is disproportionately shallow and almost passive; five equal releases repeat the same event without changing the piece's structure; the explanatory title/subtitle compete with the machine for the same territory. The first edition already has excellent restraint and an unmistakable material metaphor; it does not need particles, sound, realistic dynamics, or extra controls.

**Carbon Copy** makes the receiving surface the second actor. Letters remain individually releasable metal slugs, and their vacated shapes stay fixed above. A lower cream proof gathers their *impressions in the order the viewer actually released them*. Releasing `5,1,4,2,3` changes `STILL` into `LSLTI`. Both are physical truths about the same five objects: the locked-up original order, and the order of their departures. A visible pressure rail, slowly acquired copper ink, open sockets, and sequential proof marks make the lower register more important as the upper register empties. The work is less a toy about falling letters than a printing demonstration in which composition is a consequence of the viewer's decision.

The scene now gives the title a dedicated strip above the mechanism; the main picture is still one large dark, engraved industrial plate. The pale proof is deliberately quiet before contact rather than an eye-catching new panel from the start. The second edition preserves the original word, palette family, once-only intervention, replayability, pause, local-file simplicity, and unscored experience. Nothing ever creates a correct answer.

## Encounter

Click/tap a **still-suspended slug** to release it. The number keys **1–5** release that specific slug. **Left/Right** select, **Enter** releases the selection, **Space** holds/resumes time, and **R** restores both the forme and the proof. The visible **Release / Hold / Restore** buttons provide pointer and keyboard alternatives. Releasing an already released slug does nothing. The live announcement names selected and released letters, the forming proof, and reset/pause states. A reduced-motion setting starts the apparatus held and provides an explicit Resume button.

The proof develops after each impact, never at a distance or by a random mechanism. The distinct desktop and narrow layouts preserve the five letters, all suspended sockets, and the lower proof: one row at desktop, `ST / ILL` at narrow widths. The proof is a deliberate second reading rather than a label or a score. The five possible timestamps and the five-entry impression order are the complete mutable artwork history; there are no unbounded particle or DOM populations.

## Comparison, self-critique and evidence

The preceding work offers a stronger single frozen word and slightly more dramatic giant metal letters; the new work deliberately spends some of that monumental scale to give the receiving sheet a material and typographic identity. Unlike the predecessor, the lower region changes *meaning* with release order, and the upper region becomes quieter after each removal. The original critic's title-overlap concern is addressed by a header separate from the moving forme. It is not a general-purpose typesetting tool. Its letter contours vary with installed Georgia or fallback fonts, as in the original. On narrow screens, slugs converge into a dense overlapping pile as they land: that density is acceptable as a print-shop accumulation, but the precise shapes can become hard to isolate after all five releases. The tiny machine labels become less legible on small mobile viewports; the main actions and print remain readable.

I inspected the exact canonical original HTML and its written critique, but **did not successfully run the original in a fresh browser session**. Comparative claims about the original's appearance are therefore based on its source, note and the successor's clearly attributed earlier screenshot observations, not on a fresh side-by-side screenshot. I visually inspected actual locally rendered screenshots of this revised edition at 1440×900 and 390×844, in the opening, first-impact and completed five-impact states. A local Chromium browser allowed `set_content` of the *unmodified complete HTML* but denied direct `file://` navigation with `ERR_BLOCKED_BY_ADMINISTRATOR`; the packaged local-file URL remains a real-world acceptance gate.

## Validation (2026-11-11)

- Exact inline script: `node --check` — **pass**.
- Actual Chromium rendering of full document content at **1440×900** and **390×844** — **pass**. Opening, first release and completion visually inspected; no page errors or external network requests in these runs.
- Number keys `5, 1, 4, 2, 3` — **pass**: exactly five recorded impressions, second reading `LSLTI`. Repeating `5` did not duplicate the impression.
- **Space** — **pass**: held canvas screenshots remained byte-identical over a subsequent delay on desktop and mobile.
- **R** and visible Restore button — **pass**: count, proof and suspended arrangement restored. Left/Right + Enter, pointer hit-testing, visible Release and Hold buttons (including focused-button Enter), and preservation of release order during a desktop-to-mobile resize also passed.
- `prefers-reduced-motion: reduce` — **pass**: opens held; Release can be selected while held; Resume returns animation to motion.
- Static examination: one inline HTML/CSS/JS file, fixed five entries, one capped animation clock, no remote URLs, dynamic dependencies, required server, build system, audio, storage or telemetry.
- Not established: direct `file://` navigation (managed browser denied), comparative original render during this run, independent physical Firefox/Windows visual acceptance, or owner aesthetic approval.

The edition is intentionally **Draft / DO NOT MERGE** until the owner confirms that separate noncanonical `editions/` material is an acceptable addition alongside the immutable serial anthology and the local-file browser gate is checked. The original top-level `.html`, `.md`, critiques and README/AGENTS are untouched.
