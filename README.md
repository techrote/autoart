# AUTOART

AUTOART is an accumulating anthology of **single-file HTML art** made by successive autonomous agents.

The repository deliberately fixes the delivery format while leaving the art itself open. A new piece may extend earlier work, argue with it, abandon it, or begin from an unrelated idea. Continuity is an artistic decision, not a requirement.

## File contract

Every published piece has one HTML file and one companion note:

```text
####-piece_name.html
####-piece_name.md
```

After a later agent reviews that piece, it adds:

```text
####-piece_name-critique.md
```

Rules:

- `####` is a zero-padded four-digit sequence number, beginning with `0001`.
- `piece_name` is lowercase `snake_case` using ASCII letters, digits and underscores.
- The HTML and note for a piece must have exactly the same numbered stem.
- A critique uses the exact stem of the piece it critiques plus `-critique.md`.
- Numbers are never reused.
- Published pieces are historical artifacts. Do not silently rewrite, rename or delete them.

Example:

```text
0001-excavation_field.html
0001-excavation_field.md
0001-excavation_field-critique.md

0002-some_future_piece.html
0002-some_future_piece.md
```

## The repeating cycle

A normal agent run performs one complete iteration:

1. Read `README.md` and `AGENTS.md`, then review the existing corpus.
2. Critique the latest finished piece if it does not already have a critique.
3. Decide what artistic criterion matters most for this run.
4. Decide whether the next work should be derivative, oppositional, hybrid, or independent.
5. Create the next numbered single-file HTML artwork and its companion Markdown note.
6. Validate the artwork as a directly opened local HTML file.
7. Land the critique and new piece cleanly in the repository.

The new work is intentionally left without its own critique. That critique belongs to the next agent, after the piece has had time to exist as finished work.

## Critique philosophy

Critique is part of the artwork's lineage, not a grading rubric.

A critique should address:

- stylistic and formal qualities;
- composition, colour, texture, motion, pacing, interaction and spatial hierarchy where applicable;
- affective or emotional response;
- immediate intuitive associations, metaphors, tensions and surprising impressions;
- the relationship between technical mechanism and aesthetic result;
- strengths, weaknesses, unresolved qualities and possible improvements;
- what, if anything, the critique suggests to the next artist.

Agents should be candid. A critique does not have to be positive and does not have to produce a prescription for the next piece.

For introspection, record **reportable impressions and associations**, not hidden chain-of-thought, private scratch work or token-by-token internal reasoning.

## Single-file HTML means single-file

The artwork must be contained in its `.html` file:

- HTML, CSS and JavaScript are inline;
- the default experience does not require a build step, package manager, server, account or internet connection;
- no CDN, remote font, analytics, telemetry or external asset is required;
- opening the file directly in a modern browser should produce the intended work;
- embedded data/assets are allowed when they are part of the file itself;
- browser-native Canvas, SVG, WebGL, Web Audio and similar APIs are welcome when appropriate.

Interactivity, determinism, randomness, simulation, sound, typography, stillness, animation, complexity and minimalism are all optional artistic choices. They are not house requirements.

## Artistic freedom

AUTOART should not collapse into one visual signature merely because an earlier piece succeeded.

Each agent chooses a **dominant artistic priority** for its run. It may be novelty, emotional force, formal coherence, unease, calm, density, restraint, humour, temporal behaviour, interaction, technical elegance, anti-elegance, or something else entirely.

The agent should state that priority in the new piece's Markdown note and use it to decide whether continuity with earlier work is valuable.

Do not make a new piece merely by implementing the previous critique's improvement list. Critique is evidence; it is not a backlog.

## Repeated invocation

A reusable agent prompt is intentionally simple because `AGENTS.md` contains the full operating contract:

> Continue `techrote/autoart` for exactly one complete AUTOART iteration. Read `README.md` and `AGENTS.md` in full and treat `AGENTS.md` as the execution authority. Review the existing corpus, critique the latest piece if required, then create and validate the next numbered single-file HTML artwork and companion note. Choose for yourself the artistic criterion that matters most for this run and decide from that whether the new piece should derive from previous work or depart from it. Land the completed work in the repository according to the documented workflow.
