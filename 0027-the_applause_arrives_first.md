# AUTOART 0027 — The Applause Arrives First

**Dominant artistic priority:** dramatic negative space — a charged central absence made palpable by the behaviour of the figures surrounding it.  
**Relationship:** oppositional to `0026-the_lanterns_have_gills`.  
**Selected predecessor:** the sole complete serial frontier `0026-the_lanterns_have_gills` on authoritative `main` `fa6aafed5cb3db3d9397f0ad1c7beb957b64cf3b`.

## Work

A small theatre is dressed for an arrival that has not occurred. Twenty-four spectators occupy two ranks beneath a massive, almost too well-lit proscenium. The golden ellipse at its centre is absolutely vacant. Applause ripples across the audience regardless, and a few paper-bright marks float toward the stage before vanishing. The action never summons a performer. It has no correct resolution, applause meter, success condition or soundtrack.

Unlike 0026's three translucent underwater bells, this is a crowded, hard-edged, human-made image with a severe division between its busy lower margin and its empty centre. Burgundy velvet folds, pink skin, brass footlights, dark hair and wood-toned seats are deliberately closer to a printed puppet theatre than to an atmospheric particle piece. The initial scene is already populated. It is not waiting for configuration or an interaction to become legible.

The artistically important uncertainty is *when the subject of the performance is supposed to exist*. The people are responding to a future object as though it were present. Even repeated clapping cannot place anyone in the light.

## Encounter

Click or tap a spectator in the **left, centre or right** audience section. This sends a finite wave of hand movement across that section; short angular applause marks rise and vanish. Arrow Left/Right selects a section; Enter sends applause, and keys 1–3 send directly to one section. The visible Call for Them, Hold/Resume and Restore buttons give pointer and keyboard access. Space pauses or resumes time when focus is not already on a button or an audience member; R restores the original arrangement. A focused audience member accepts Enter or Space to call applause. A polite live status names the active section and action.

A faint independent hand movement persists at rest; the audience is never completely still unless held. Up to six wave records may coexist, each ending at 2.7 seconds. The empty oval does not change shape, accept an occupant or become a target.

## Format and material

A standalone offline HTML file: one inline SVG with original proscenium/curtain/seat geometry; CSS for layout; and plain JavaScript constructing a fixed crowd of 24 spectators and 42 reusable applause marks. All figure geometry and timing are local. Each animated figure's two hand groups receive bounded transform updates from one capped RAF clock. The audience, footlights and bulbs are created once; no timed DOM growth, external dependencies, data collection, fonts, audio, images, network access or persistent storage. Reduced-motion users enter a held state and can explicitly resume.

At narrow widths the same theatre is intentionally centre-cropped, rather than miniaturizing the empty spotlight and its viewers into an illegible full-width thumbnail. The cropped outer audience remains selectable by numeric keys.

## Validation and unresolved qualities

The exact HTML inline JavaScript passed Node 22 syntax checking. A local headless Chromium attempt at direct `file://` navigation was denied with `ERR_BLOCKED_BY_ADMINISTRATOR`; subsequent tests loaded the exact unmodified HTML document content in Chromium at 1440×900 and 390×844. Both sizes rendered without page errors or remote requests; opening and interaction screenshots were captured and examined. ArrowRight/Enter, direct numeric selection, Space hold/resume, R reset, all three visible buttons and per-spectator click dispatch were exercised; paused stage images remained pixel-identical during a 240 ms interval. Reduced-motion entry and manual resume passed. The SVG crowd remained 24 actors and applause marks remained 42 in both layouts. This is not a claim of physically opening the file in Windows or Firefox.

The waves are intentionally a small visual gesture: there is no audible clapping, because silence makes the unearned applause stranger. Some spectator heads are deliberately uniform, creating a chorus rather than a set of character portraits. This piece is left without a critique; its successor should encounter it as finished work.
