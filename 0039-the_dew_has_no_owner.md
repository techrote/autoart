# AUTOART 0039 — The Dew Has No Owner

**Dominant artistic priority:** ephemeral resilience. A fragile structure should answer a brief disturbance across its whole surface, then recover without turning the disturbance into an inventory of scars.

**Relationship:** oppositional to the sole complete numeric frontier, `0038-the_moth_has_two_maps`, encountered on `main` `53a41d0a2a6ced6dd3e1724aed1ebd137f80cd86` on 11 November 2026. The unrelated `editions/0025-...` second-edition Draft is not a numbered frontier, serial blockage, or critique obligation.

## The work

A loosely drawn spiderweb spans a large portion of a warm paper-coloured sheet. Forty-eight amber-and-milk dew drops cling at irregular positions. Most of the picture is slender blue ink line; some radial cords end early or break, and three outer anchor lines run off the edge of the page. No spider appears. A still field is not necessarily empty of tension.

The viewer drags across the woven field to introduce a gust, or presses **Send a Breeze**. The whole web bends through a short, damped elastic disturbance. The dew travels with its threads rather than falling or becoming a countable harvest. **Let It Settle** restores the initial arrangement. The gesture neither accumulates prints nor creates scores. The work does not attempt a physical spiderweb solver: its radial links and motion are a calibrated drawing, deliberately stronger in silhouette than in scientific realism.

Where 0038 uses saturated paired wings and retained outline impressions, 0039 uses a single wide asymmetric net, mostly near-white negative space, one restrained warm accent and a response that naturally dissipates. The counterpart to the moth's heavy map is not another creature; it is the almost invisible support that could have existed before the moth arrived. This is a relationship of scale and attention, not a narrative sequel. The larger anthology's many studies of withheld contact and released objects were consulted to avoid another falling inventory or another solemn near-miss.

## Encounter and controls

The initial image is complete without input. Drag pointer or touch horizontally through the image to pull the threads into a gust; release to watch the field settle. **B** or the **Send a Breeze** button supplies a bounded impulse without needing a pointing device. **R** or **Let It Settle** restores the undisturbed authored state. The status text reports stillness or motion. Both buttons are ordinary keyboard-focusable controls. A viewer who prefers reduced motion sees a stable deformation immediately instead of a spring animation.

## Construction

A self-contained HTML document uses one pixel-ratio-capped Canvas 2D surface, 29 indexed imperfect spokes, 15 stitched rings, 48 droplets, three anchor cords and an authored initial layout. The droplet seeds are fixed arithmetic indices, not generated at publication time. A one-frame-request-at-a-time loop only runs while the spring is moving. Its energy is damped and bounded, and the animation terminates when motion is negligible. No external images, libraries, fonts, telemetry, network, audio, storage or build are needed. The mobile layout gives the title its own high-key band and crops the web rather than collapsing its fine lines into a tiny diagram.

## Qualification and limitations

On 11 November 2026, the exact proposed HTML was syntax-checked in Node 22 and rendered as document content in system Chromium at 1440×900 and 390×844, including a visible breeze and restoration. An additional qualification checked keyboard, pointer, reduced motion, no external requests, no page errors and the mobile overflow gate. Direct local `file://` navigation is blocked by the managed Chromium environment; physical Firefox, OS-local-file opening and subjective owner aesthetic acceptance have not been claimed. The geometry is a stylised drawing rather than a tension solver, and the visible mobile crop is intentional. No 0039 critique is created in this run.
