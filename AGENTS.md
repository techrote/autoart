# AGENTS.md

This file is the execution authority for autonomous work in `techrote/autoart`.

AUTOART is a sequential art practice, not a software feature backlog. The repository provides a strict publication format and a review ritual; it does **not** prescribe a house aesthetic.


## Core invariant

AUTOART is an accumulating anthology organised into numbered **publication slots**. Most slots contain one piece. A slot may contain multiple sibling variants when independent agents began from the same published frontier and produced distinct valid work.

One normal creative run creates at most:

- critique(s) required for the selected predecessor piece(s), when missing;
- one new artwork `.html` file;
- one matching artwork `.md` note.

A collision-recovery run may instead preserve an already-created concurrent critique or artwork under the documented variant naming rules. Valid generated art and valid independent reviews must not be discarded merely because another agent published first.

Routine runs should not otherwise modify older artwork, older notes, existing critiques, `README.md`, or this file.


## Determine the current sequence

Establish the current authoritative `main` state before making creative changes. Do not infer the current corpus solely from the branch or worktree that happens to be checked out.

A **publication slot** is the four-digit numeric prefix:

```text
####
```

A **piece id** is that slot plus an optional lowercase variant suffix:

```text
####
####a
####b
...
```

If more than 26 variants are ever needed, continue with `aa`, `ab`, and so on rather than changing the slot number.

A **complete piece** is a matching pair:

```text
####-piece_name.html
####-piece_name.md
```

or, for a sibling variant:

```text
####a-piece_name.html
####a-piece_name.md
```

Ignore critique files when determining slots and piece ids.

The **highest slot** is the largest four-digit numeric prefix represented by a complete piece, ignoring variant suffixes.

The **frontier set** is every complete piece in the highest slot, including the unsuffixed piece and any suffixed sibling variants.

The next ordinary slot is highest slot + 1, zero-padded to four digits. The first publication in that slot uses the unsuffixed id.

If independent work intended for that same slot is published later because another agent won the publication race, preserve the later work in the **same slot** using the next available variant suffix. Do not discard it and do not silently move it to the next numeric slot, because doing so would falsify its historical starting point.

If a piece id is represented by only one half of the required HTML/Markdown pair, treat the repository as inconsistent. Investigate before publishing another piece; do not guess around the collision.

Do not renumber published history. If numeric slot `9999` is ever reached, stop and report the naming-boundary problem rather than silently changing the scheme.


## Choose the critique target

Normally, when the frontier set contains one piece, that piece is the critique target and artistic predecessor.

When the frontier set contains multiple sibling pieces, inspect all of them and their existing critiques before choosing the lineage for the next work. The agent may choose:

- one frontier piece as its predecessor; or
- two or more frontier pieces as joint predecessors.

Record that choice explicitly in the new piece's companion note.

For each selected predecessor that has no critique, create a critique during this run when practical.

A normal run does not create a second critique merely because it disagrees with an existing one. However, if a distinct critique was already produced independently in a concurrent run before the agent could observe the first publication, preserve it rather than discard it:

```text
####-piece_name-critique.md
####-piece_name-critique-a.md
####-piece_name-critique-b.md
```

The first published critique keeps the unsuffixed `-critique.md` filename. Later concurrent reviews use the next available suffix.

A new piece created during the current run does **not** receive a critique during the same run. It should remain available for a later agent to encounter as finished work.

## Review the corpus before judging it

Read `README.md` and this file first.

Then inspect the existing corpus before writing the critique or deciding what to create.

At minimum:

- enumerate all numbered pieces and critiques;
- read every existing piece-note `.md`;
- read every existing `-critique.md`;
- inspect the source of the selected frontier predecessor piece(s);
- actually render and interact with the relevant frontier piece(s) in a browser when the available environment permits it.

Do not claim visual, temporal or interactive observations that were inferred only from prose or source code if you did not actually observe them.

When the corpus is still small, inspect/render all previous HTML pieces when practical. If the corpus becomes large, keep global awareness by reading all notes/critiques, then directly inspect the latest several pieces plus any earlier pieces that become materially relevant to the new artistic direction.

Other `techrote` repositories may be inspected for inspiration when that genuinely serves the chosen direction, but doing so is optional. AUTOART must not become a compulsory collage of the rest of the account.

## Write the critique

The ordinary critique filename is the exact target stem plus `-critique.md`. A preserved concurrent duplicate review adds the next available suffix after `critique`.

Example:

```text
0007-signal_garden.html
0007-signal_garden.md
0007-signal_garden-critique.md
0007-signal_garden-critique-a.md
```

Critique suffixes are collision-preservation metadata, not invitations to generate redundant reviews during ordinary runs.

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

Ordinary required pair:

```text
####-piece_name.html
####-piece_name.md
```

Preserved concurrent sibling:

```text
####a-piece_name.html
####a-piece_name.md
```

The visible title inside the artwork may use ordinary capitalization and punctuation, but its displayed AUTOART id should match the published piece id.

Before writing, verify that neither required filename already exists. Immediately before publication, re-check authoritative `main`; if the intended ordinary slot was claimed by genuinely concurrent work, convert this run to the next available sibling variant in the same slot and preserve its original artistic provenance.

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
- its selected predecessor lineage; when the frontier had sibling variants, state whether the work responds to one named sibling or to several;
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

### Publication continuity gate

Start every invocation by checking:

- current authoritative `main`;
- open AUTOART pull requests;
- relevant `art/*` branches;
- whether a previous completed iteration exists outside `main` because publication was blocked.

A previously completed but unpublished iteration is **not** permission to continue making an arbitrarily long unpublished sequence.

If completed AUTOART work exists outside `main` because PR creation, merge, repository permissions, connector safety policy, or another publication mechanism blocked it:

1. preserve the completed branch and exact commit;
2. attempt to reconcile or publish that existing work before creating new art;
3. do **not** create another ordinary sequential artwork merely by continuing from the unpublished branch;
4. if publication remains blocked, report the exact blocker and stop the run without advancing the artistic sequence.

This gate does not invalidate genuine concurrency. If multiple agents independently began from the same published frontier before any could observe the others, preserve every valid result using the sibling-variant and duplicate-critique rules.

### Normal creative publication

Prefer a clean branch for each iteration:

```text
art/####-piece_name
```

If a publication collision is discovered later, the branch may be renamed/recreated for the corresponding variant, but preserving the committed artwork is more important than branch-name aesthetics.

A routine iteration normally changes:

```text
<selected-predecessor-stem>-critique.md   # only if missing
####-piece_name.html
####-piece_name.md
```

A run selecting multiple frontier predecessors may create more than one missing critique. A collision-recovery run may add suffixed critique or piece files instead.

Do not rewrite prior artworks to implement critique suggestions. History is part of the project.

Do not add build systems, package manifests, frameworks, generated screenshots, lockfiles or dependency trees merely to support development. Temporary validation artifacts must not be committed unless they are intentionally part of the artwork.

Publication procedure:

1. establish current authoritative `main` and pass the publication continuity gate;
2. create the branch from that published frontier;
3. review the frontier and create the required critique(s), new piece and note;
4. validate the exact branch contents;
5. re-check authoritative `main` immediately before publication;
6. if the intended ordinary slot is still free, publish normally;
7. if genuinely concurrent work has claimed that slot, preserve this run under the next available variant suffix in the **same slot**, preserve any concurrently-created duplicate critique under the next available critique suffix, and revalidate the exact final files;
8. inspect the final diff for accidental files;
9. open a pull request;
10. merge only after relevant automated checks and the manual validation gate are satisfied;
11. verify the intended files and resulting commit actually landed on `main`.

If there are no automated checks, that absence is not an excuse to skip the validation gate.

If publication is blocked by a genuine repository/tool/permissions problem, preserve accurate work/evidence and report the blocker. Do not invent a successful PR, render, merge or validation. A later recurring invocation must attempt publication recovery before creating further art.

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

At the end of a run, report succinctly:

- publication state found at the beginning;
- any pending work recovered or published;
- selected predecessor piece(s);
- critique(s) created, preserved as concurrent variants, or already present;
- new piece id/variant, title and filenames, if a new creative iteration was permitted;
- the dominant artistic priority;
- whether the new work is derivative/oppositional/hybrid/independent;
- validation performed;
- exact branch/commit;
- PR/merge status and resulting main commit, or the exact publication blocker.

Do not reveal hidden chain-of-thought in the completion report.
