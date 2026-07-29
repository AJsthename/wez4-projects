# Asset Production List — Pancake Run (60s animated short)

Scene-by-scene read: S1 kitchen (Mom, pan, pancake flip) → S2 pancake exits window → S3 dog chase down suburban street past bakery → S4 pancake lands on street performer's hat, pigeon swarm → S5 kitchen again (Mom shrugs, dog returns with pancake on nose).

## Characters
| # | Element | Scenes | Sheet type | Notes |
|---|---------|--------|-----------|-------|
| 1 | Mom | 1, 5 | three-view | face + full body; recurs and bookends the film. Give her one signature wardrobe item (e.g. apron) so S1 and S5 match across generations |
| 2 | Dog | 3, 5 | three-view | the co-lead — appears running (S3) and trotting with pancake on nose (S5). Breed, size, coat color and collar must be locked or every shot renders a different dog |
| 3 | Street performer | 4 | three-view | single scene, but S4 likely cuts to 2+ shots (pancake landing, pigeon swarm) so he needs continuity. The hat is his signature item — design it ON the sheet, since the pancake must land on *that* hat |
| 4 | Pigeons | 4 | SKIP — describe in video prompt | generic real-world birds; video models render pigeon flocks natively. A swarm doesn't need individual continuity. (If one "hero pigeon" gets a close-up gag, promote it to a sheet) |

## Locations
| # | Element | Scenes | Decision | Notes |
|---|---------|--------|----------|-------|
| 1 | Kitchen | 1, 2, 5 | GENERATE — 3/4 angle | the anchor set: recurs in three scenes and bookends the story. Layout matters — the open window (S2 exit) and the door (S5 dog entrance) must both exist in the reference and stay in consistent positions |
| 2 | Suburban street w/ bakery | 3, 4 | GENERATE — 3/4 angle | recurs across the chase and the performer beat; the little bakery is a specific landmark the dog runs past. One street reference keeps S3 and S4 in the same neighborhood (same architecture, curb, light) |
| 3 | House exterior | 2, 3 | SKIP — describe in video prompt | seen only briefly (pancake exiting window, dog bolting out the door). Generic suburban house; describe it to match the street's architecture. Reversible: generate later if the window-exit shot needs precise geography |

## Props
| # | Element | Scenes | Sheet type | Interaction notes |
|---|---------|--------|-----------|-------------------|
| 1 | Pancake | 1, 2, 3, 4, 5 | four-view | THE hero prop — appears in every scene and is flipped, flies, lands on a hat, and balances on a nose. Lock size, thickness, golden-brown tone, and edge shape. Decide topping state (plain vs. butter/syrup) — a syrupy pancake can't fly clean |
| 2 | Frying pan | 1 | SKIP — fold into scene/kitchen | one scene, generic object; the flip interaction reads fine from description. Include it in the kitchen location dressing |
| 3 | Performer's hat | 4 | (covered by character sheet) | landing target for the pancake — design it on the street performer's sheet rather than as a separate prop, since it's worn, not handled separately |

## Production order
1. **Pancake** — blocks all 5 scenes; every other asset shares frames with it, so it must be locked first.
2. **Mom** — blocks the opening and closing scenes; sets the character art style the dog and performer must match.
3. **Dog** — blocks S3 and S5, the two biggest action beats.
4. **Kitchen** — blocks S1, S2, S5; window and door placement gate the flip-exit and return shots.
5. **Suburban street w/ bakery** — blocks S3 and S4.
6. **Street performer (incl. hat)** — blocks only S4; depends on the character style established by Mom's accepted sheet.

Dependency notes: generate Mom first among characters so Dog and Performer sheets can match her style; the pancake sheet should exist before the kitchen scene prompts so S1 shows the same pancake that lands in S4.

## Open questions
- **Animation style?** "Animated short" underspecifies — 3D Pixar-style, 2D flat, stop-motion look? This decision comes *before* any sheet, since all six assets must share it.
- **Dog design:** breed/size? A corgi chase reads very differently from a golden retriever chase, and S5 requires a nose that can plausibly balance a pancake.
- **Pancake state:** plain, or with butter/syrup? Affects flight shots (S2–S4) and the nose-balance gag (S5).
- **Kitchen geography:** are the open window and the door on camera-compatible walls? S2 (window exit) and S5 (door entrance) both depend on the kitchen layout — confirm before generating the location sheet.
- **Same street for S3 and S4?** Assumed yes (one street asset). If the performer's spot is a separate plaza/corner, it needs its own location decision.
- **Street performer type:** musician, mime, juggler? Determines pose, gear, and what kind of hat the pancake lands on (upturned tip hat on the ground vs. hat on his head — these are different shots).
