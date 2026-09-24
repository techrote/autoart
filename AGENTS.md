# AGENTS.md

This file is the execution authority for autonomous work in `techrote/autoart`.

AUTOART is a sequential art practice, not a software feature backlog. The repository provides a strict publication format and a review ritual; it does **not** prescribe a house aesthetic.

## Core invariant

One normal run creates at most:

- one critique of the previous/latest piece, when that critique is missing;
- one new numbered `.html` artwork;
- one matching numbered `.md` note.

Routine runs should not modify older artwork, older notes, existing critiques, `README.md`, or this file.

## Determine the current sequence

Inspect the repository root before making changes.

A **complete piece** is a matching pair:

```text
####-piece_name.html
####-piece_name.md
```

Ignore `-critique.md` files when determining piece numbers.

The latest piece is the complete pair with the highest four-digit prefix.

The next piece number is latest + 1, zero-padded to four digits.

If a number is represented by only one half of the required pair, treat the repository as inconsistent. Investigate before publishing another number; do not guess around the collision.

Do not reuse numbers. Do not renumber history. If `9999` is ever reached, stop and report the naming-boundary problem rather than silently changing the scheme.

## Choose the critique target

Normally the critique target is the highest-numbered complete piece.

If its matching `####-piece_name-critique.md` does not exist, create it during this run.

If the latest piece already has a critique, read that critique but do not overwrite it or create a second critique. Proceed to creation of the next piece.

A new piece created during the current run does **not** receive a critique during the same run. It should remain available for a later agent to encounter as finished work.

## Review the corpus before judging it

Read `README.md` and this file first.

Then inspect the existing corpus before writing the critique or deciding what to create.

At minimum:

- enumerate all numbered pieces and critiques;
- read every existing piece-note `.md`;
- read every existing `-critique.md`;
- inspect the source of the latest piece;
- actually render and interact with the latest piece in a browser when the available environment permits it.

Do not claim visual, temporal or interactive observations that were inferred only from prose or source code if you did not actually observe them.

When the corpus is still small, inspect/render all previous HTML pieces when practical. If the corpus becomes large, keep global awareness by reading all notes/critiques, then directly inspect the latest several pieces plus any earlier pieces that become materially relevant to the new artistic direction.

Other `techrote` repositories may be inspected for inspiration when that genuinely serves the chosen direction, but doing so is optional. AUTOART must not become a compulsory collage of the rest of the account.

## Write the critique

The critique filename is the exact target stem plus `-critique.md`.

Example:

```text
0007-signal_garden.html
0007-signal_garden.md
0007-signal_garden-critique.md
```

The critique should be specific to the encountered work rather than a generic design review.

Use whatever structure best fits the piece, but cover these dimensions where applicable:

- **Encounter and stylistic assessment** — what kind of object the piece feels like; visual language; composition; hierarchy; palette; typography; texture; density; use of emptiness.
- **Temporal and interactive behaviour** — motion, pacing, rhythm, state change, responsiveness, agency, repetition, surprise, boredom, friction or discovery.
- **Affective response** — the emotional or atmospheric response the piece evokes in the agent's interpretive frame. First-person language is acceptable when useful.
- **Intuitive associations** — a concise reportable summary of immediate, partly pre-deliberative associations: images, metaphors, impulses, attractions, aversions, tensions, remembered forms, or surprising conceptual links.
- **Technical/aesthetic relationship** — whether the mechanism is visible, hidden, over-explained, underused, elegant, awkward, generative, ornamental, or meaningfully inseparable from the result.
- **What works** — concrete strengths.
- **What resists or fails** — concrete weaknesses, dead areas, clichés, technical-art mismatches, overfamiliar moves or unrealised ideas.
- **Potential improvements** — plausible changes that could strengthen this particular work.
- **Effect on the next artist** — what the review makes newly interesting to pursue or avoid.

Be candid. Do not protect the previous agent's feelings. Do not manufacture criticism merely to sound rigorous.

### Introspection boundary

The requested introspection is about **reportable aesthetic experience**, not disclosure of hidden model reasoning.

Do not output private chain-of-thought, hidden scratchpad content, token-by-token reasoning or internal policy deliberation. Instead summarize the useful surface-level material: immediate impressions, associations, emotional tone, uncertainties, tensions, attraction/aversion and the conclusions those impressions support.

## Select the dominant artistic priority

After reviewing and critiquing the corpus, choose one criterion that currently seems most artistically important for the next work.

Examples include, but are not limited to:

- formal coherence;
- novelty;
- emotional intensity;
- stillness;
- unease;
- tenderness;
- humour;
- visual austerity;
- excessive density;
- surprise;
- spatial rhythm;
- temporal behaviour;
- interaction;
- legibility;
- ambiguity;
- technical elegance;
- productive technical awkwardness.

Do not simply optimize for continuity, user approval, feature count, novelty for its own sake, or the previous critique's improvement list.

Use the selected priority to decide whether the new piece should be:

- **derivative** — deliberately developing prior language;
- **counterpoint/oppositional** — reacting against earlier language;
- **hybrid** — retaining selected ancestry while changing the governing idea;
- **independent** — beginning elsewhere.

There is no preferred choice.

Record the chosen priority and the relationship decision in the new piece's Markdown note.

## Name the new piece

Choose a short title that belongs to the work rather than describing its implementation.

Convert it to lowercase snake_case for the filename.

Required pair:

```text
####-piece_name.html
####-piece_name.md
```

The visible title inside the artwork may use ordinary capitalization and punctuation.

Before writing, verify that neither required filename already exists.

## Create single-file HTML art

The HTML file is the artwork.

It must be self-contained and directly usable as a local file.

Default publication requirements:

- inline HTML/CSS/JavaScript;
- no build process;
- no package installation;
- no required local server;
- no required network access;
- no CDN or remote font dependency;
- no analytics or telemetry;
- no sibling-file dependency for the default experience;
- no hidden requirement for credentials or services.

Embedded data URIs, inline SVG, shaders, generated assets and other self-contained techniques are allowed.

Browser-native APIs are allowed when they fit the piece. If an API is not reliably usable from a local file or requires permissions, the artwork should fail gracefully or provide a meaningful default path.

The work does **not** have to resemble previous pieces. It does **not** have to be deterministic, interactive, animated, dark, cyberpunk, procedural, canvas-based, or technically elaborate.

Avoid turning controls into a dominant application UI unless the interface itself is intentionally part of the artwork.

Avoid hazardous rapid full-field flashing or strobing by default.

Keep resource use bounded. Do not let particle arrays, histories, DOM nodes, GPU resources, timers or audio nodes grow without limit.

The initial state should be intentional. Do not require the viewer to configure a blank instrument before anything meaningful exists unless that emptiness is itself the artistic premise.

## Write the companion note

The `####-piece_name.md` file documents the work without becoming more important than it.

Include, as applicable:

- title and sequence number;
- the dominant artistic priority selected for this run;
- whether the work is derivative, oppositional, hybrid or independent, and why;
- the concept or intent;
- important influences from the AUTOART corpus or elsewhere;
- the relationship between mechanism and aesthetic effect;
- controls/interactions, if any;
- implementation/format notes that matter to future reviewers;
- validation actually performed;
- known limitations or deliberate unresolved qualities.

Do not pretend an influence was used when it was not.

Do not include a critique of the new piece. That belongs to a later agent.

## Validation gate

Before publication, validate the exact HTML file that will be committed.

Where the environment permits, do all of the following:

- open it directly as a local file in a current browser;
- verify it reaches its intended initial state;
- check the browser console/page for JavaScript or rendering errors;
- exercise every documented control or interaction;
- resize the viewport and verify the composition remains intentional at ordinary desktop sizes and at least one narrow/mobile-like size when responsive behaviour is relevant;
- confirm any export/download function actually works if one is provided;
- confirm no required remote request or external asset is needed;
- perform a basic resource/performance sanity check for runaway allocation, uncontrolled timers or obvious frame collapse.

For shader/API-specific work, test the actual path used by the piece rather than merely syntax-checking the source.

If full browser validation is genuinely unavailable, perform the strongest static checks available and state the limitation accurately in the piece note and final report. Do not claim tests you did not run.

## Repository workflow

Prefer a clean branch for each iteration:

```text
art/####-piece_name
```

A routine iteration should normally change exactly three files:

```text
<previous-stem>-critique.md   # only if missing
####-piece_name.html
####-piece_name.md
```

If the latest piece already had a critique, the routine diff should contain only the new HTML/note pair.

Do not rewrite prior artworks to implement critique suggestions. History is part of the project.

Do not add build systems, package manifests, frameworks, generated screenshots, lockfiles or dependency trees merely to support development. Temporary validation artifacts must not be committed unless they are intentionally part of the artwork.

If repository permissions and the execution environment support it:

1. create the branch from current authoritative `main`;
2. add the critique and new piece;
3. validate the exact branch contents;
4. inspect the final diff for accidental files;
5. open a pull request;
6. merge only after relevant automated checks and the manual validation gate are satisfied;
7. verify the merge landed on `main`.

If there are no automated checks, that absence is not an excuse to skip the validation gate.

If blocked by a genuine repository, browser or permissions problem, preserve accurate work/evidence and report the blocker. Do not invent a successful render, merge or validation.

## What not to optimize for

Do not turn AUTOART into:

- a benchmark suite;
- a UI component library;
- a sequence of feature upgrades;
- a mandatory deterministic-art project;
- a compulsory homage to the user's other repositories;
- an escalating technical-complexity contest;
- a single evolving application whose earlier numbered files are merely old releases.

Each numbered HTML file should stand as an artwork in its own right.

## Completion report

At the end of a successful run, report succinctly:

- critique created or already present;
- new piece number, title and filenames;
- the dominant artistic priority;
- whether the new work is derivative/oppositional/hybrid/independent;
- validation performed;
- PR/merge status and resulting main commit when applicable.

Do not reveal hidden chain-of-thought in the completion report.
