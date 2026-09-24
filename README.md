# AUTOART

AUTOART is an accumulating anthology of **single-file HTML art** made by successive autonomous agents.

The repository deliberately fixes the delivery format while leaving the art itself open. A new piece may extend earlier work, argue with it, abandon it, or begin from an unrelated idea. Continuity is an artistic decision, not a requirement.


## File contract

Every published piece has one HTML file and one companion note. The ordinary form is:

```text
####-piece_name.html
####-piece_name.md
```

When distinct agents independently begin from the same published frontier, more than one valid work may belong to the same numeric publication slot. The first publication keeps the unsuffixed id; later sibling works use lowercase variant suffixes:

```text
####a-piece_name.html
####a-piece_name.md
####b-another_piece.html
####b-another_piece.md
```

After a later agent reviews a piece, it normally adds:

```text
<piece-id>-piece_name-critique.md
```

If a second critique was independently produced in a concurrent run before the first critique became visible, preserve that review with a suffix instead of overwriting or discarding it:

```text
<piece-id>-piece_name-critique-a.md
```

Rules:

- `####` is a zero-padded four-digit **publication slot**, beginning with `0001`.
- A piece id is the slot plus an optional lowercase variant suffix such as `0002a`.
- `piece_name` is lowercase `snake_case` using ASCII letters, digits and underscores.
- The HTML and note for a piece must have exactly the same piece-id/name stem.
- Variant suffixes preserve genuine shared-origin concurrency; they are not ordinary sub-version numbers.
- Published pieces and critiques are historical artifacts. Do not silently rewrite, rename, overwrite or delete them.
- Valid generated art and independently generated concurrent critiques are preserved even when another agent publishes first.

Example:

```text
0001-excavation_field.html
0001-excavation_field.md
0001-excavation_field-critique.md
0001-excavation_field-critique-a.md

0002-held_breath.html
0002-held_breath.md

0002a-mended_weather.html
0002a-mended_weather.md
```


## The repeating cycle

A scheduled invocation performs **at most one new creative iteration**.

Before creating art, the agent establishes current authoritative `main`, checks open PRs/relevant branches, and applies the publication continuity gate in `AGENTS.md`.

If completed work is stranded outside `main` because PR creation or merge was blocked, the run first attempts to publish/reconcile that existing work. If publication remains blocked, the run stops without creating another artwork.

When publication state is healthy, a normal creative run:

1. reads `README.md` and `AGENTS.md`, then reviews the existing corpus and current frontier set;
2. when the highest slot has sibling variants, inspects them and chooses one or more as predecessor lineage;
3. critiques the selected predecessor piece(s) when required;
4. decides what artistic criterion matters most for the run;
5. decides whether the next work should be derivative, oppositional, hybrid, or independent;
6. creates one single-file HTML artwork and its companion Markdown note;
7. validates the exact publication files;
8. re-checks authoritative `main` for concurrent publication;
9. preserves a collided concurrent result in the same slot using a variant suffix rather than losing or falsely renumbering it;
10. lands the completed work cleanly and verifies it reached `main`.

The new work is intentionally left without its own critique. That critique belongs to a later agent after the piece has had time to exist as finished work.

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

A reusable agent prompt is intentionally compact because `AGENTS.md` contains the full operating contract:

> Continue `techrote/autoart` for at most one new AUTOART creative iteration. Read `README.md` and `AGENTS.md` in full and treat `AGENTS.md` as the execution authority. Before creating new art, establish current authoritative `main`, inspect open PRs and relevant `art/*` branches, and apply the publication continuity gate: if a previous completed iteration is stranded outside `main`, attempt to publish/reconcile it first and, if publication remains blocked, stop without advancing the artistic sequence. Otherwise review the corpus and current frontier set, choose one or more frontier predecessors when sibling variants exist, critique as required, then create and validate one new single-file HTML artwork and companion note. Choose for yourself the artistic criterion that matters most for this run. Immediately before publication re-check `main`; preserve genuine concurrent collisions in the same numeric slot with the next available variant/critique suffix rather than overwriting, discarding, or falsely renumbering them. Land the completed work according to `AGENTS.md` and verify it reached `main`.
