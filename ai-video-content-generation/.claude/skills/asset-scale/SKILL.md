---
name: asset-scale
description: >
  Lock the relative size of every character and prop in an AI video project so proportions stay identical from reference sheet to clip to final compile. Use whenever a project has more than one character and their comparative size carries story or comedic weight — a giant vs a boy, a tall king above his soldiers, an adult beside a child, a monster looming over the party. Trigger on "how tall is X vs Y", "keep the sizes consistent", "make the giant actually dwarf him", "relative height", "scale chart", "size reference", "they look different sizes in every shot", or at the start of any multi-character project before sheets are generated. Output is a project Scale Bible (ratio table + landmark chain) and the single-pass cast-lineup prompt that enforces it.
---

# Asset Scale

Lock relative size across the whole pipeline. The problem this solves: **each character sheet is generated on its own canvas and fills the frame**, so a boy's sheet and a giant's sheet are the same pixel height — the sheets physically cannot encode "the giant dwarfs the boy." Size has to be *imposed*, consistently, at every stage. This skill is where the numbers are decided once so nothing drifts later.

**Output: a project Scale Bible (ratio table + landmark chain + prop anchors) and the single-pass cast-lineup image prompt.**

This runs **before** character/prop sheets are generated. `asset-planner` calls it during breakdown; `asset-character`, `asset-librarian`, and `seedance-clean` consume its output.

---

## THE THREE NON-NEGOTIABLES

### 1. One base unit, everything relative to it

Pick the project's most common ordinary human — the average man/soldier/adult — and call them **×1.00**. Express every other element as a multiple of that base. Design heights in centimetres are fine as *internal bookkeeping* to derive the ratios, but **centimetres never go into an image or video prompt** — models ignore "205 cm." Ratios, head-counts, and landmarks are what the model can actually act on.

Mixed-era or mixed-species casts still share **one** base unit, so a modern 176 cm reporter and a 297 cm giant stay consistent in any crossover shot.

### 2. Landmarks, not ratios, in the prompt text

A ratio ("1.3× taller") gets destroyed by perspective — the nearer figure just looks bigger. A **landmark contact** — "the boy's crown reaches the giant's navel," "the king's head clears the soldier by a full head" — states where two *bodies meet*, which survives camera distance and angle. The ratio table is for you; the **landmark chain** is what gets copied into prompts. Derive one landmark line for every pair whose size matters.

Giants still use human-multiple phrasing for their absolute impression ("as tall as two men standing on each other's shoulders"), and **mass matters as much as height** — state shoulder width too ("~twice the shoulder width of any man"), or a tall figure just reads as a stretched normal person.

Anchor every multiple to a figure **actually in the frame**, by tag: "twice `@shield_bearer`'s shoulder width," not "twice a man's shoulder width." The second phrasing has no on-screen referent, so there is nothing to measure against. When the large character is alone in the shot, use whatever *is* present as the yardstick — nearby crowd figures, or their own (capped) oversized prop. A solo shot with no yardstick has nothing holding the size at all.

### 2b. One landmark is a floor — write the ceiling too (the scale cage)

**A single landmark line does not hold.** It tells the model where the *minimum* gap is and says nothing about the maximum, so over a video generation the large figure drifts upward. Field-tested failure: with only "the bearer's crown reaches just above the giant's waist," three different video models held the ratio for ~2 seconds and then inflated the giant into a ~15 m titan whose calves the bearer no longer reached. The Bible must therefore carry a **cage**, not a line — four parts, all required:

1. **Several contacts, not one.** Two or three places where the bodies *meet*: crown-to-belt, **kneecap-to-hip**, hanging-elbow-to-helmet. One contact can be satisfied by an inflating figure; three mutually-contradicting ones cannot. Pick at least one contact that directly forbids the failure you have actually seen (knee-to-hip is what rules out "the man is below the giant's calf").
2. **An explicit ceiling, in body terms.** "A little under twice his height." "Two men of his height standing one on the other's shoulders would overtop him." "Both figures fit whole in one frame on one visible ground line." "The same size in the last frame as in the first."
3. **Banned vocabulary.** *colossal, enormous, monumental, gigantic, towering, earth-shaking, ground tremor* do not name a size — they name "more", and the model keeps supplying more, frame after frame. Describe **build** instead ("heavyweight-wrestler mass, human proportions") and make weight **relative** ("his steps land heavier and slower than the other man's; the ground stays firm"). Seismic physics and audio cues are read as *evidence the figure must be bigger*, and it gets resized to justify them.
4. **A real-world size class, where one exists.** "A little taller than a full-height door leaf," "the build of a heavyweight wrestler." An absolute the superlatives can't argue with — but **verify the analogue is genuinely in the target class**, because it outranks every ratio line in the prompt. Naming "a Roman scutum" for a giant's shield (a *man-fitted* shield) silently overrode a correct ratio spec and produced a man-sized prop.

Record the cage in the Bible as its own block so prompt-writers copy the whole thing, and note that it gets restated **three times per shot** — in blocking, in the action beat that reveals it, and compressed in the locks.

**Camera rule that comes with it:** no god's-eye overheads in a scale shot. An overhead throws away the shared ground line the entire comparison rests on, and the model re-guesses both figures' sizes on the new angle. Use a high three-quarter that keeps both pairs of feet in frame — it delivers the same "look how small he is" gag with the evidence still in shot.

### 3. A single-pass cast lineup locks the reference stage

The only reliable prompt-only way to fix cross-character proportion is one image containing **all the principals** on a shared ground line, correctly proportioned — in a single generation the model sets their relative sizes internally. Individual sheets still carry **identity/appearance**; the lineup carries **scale**. In a two-shot you upload both. Add pairwise mini-lineups for the money shots.

**Characters that must match cannot be generated independently and reconciled later** — a boy's solo sheet and a giant's solo sheet are the same pixel height, and text alone can't turn them into the same two people at the right relative size. Tie them together at generation time, one of two ways depending on your image tool:

- **Referenced-forward (multi-image tools):** generate each detailed identity sheet first, then build the lineup by **feeding those sheets in as references** + landmark text. Identity from the images, size from the words. Preferred — keeps full sheet detail.
- **Born-together (single-reference or text-only tools):** generate the lineup **first**, in one pass, then derive each individual sheet from its crop. Identity and scale are consistent by construction, at the cost of lower per-character detail.

Either way, **never re-describe a character's identity in the lineup text** when a sheet exists for them — the text carries layout + landmarks only.

---

## THE SCALE BIBLE (per-project artifact)

Create one file per project (e.g. `<Project> - Scale Bible.md`). Keep this shape:

```markdown
Base unit: [ordinary human] (~[N] cm) = ×1.00. Design height is internal only — never prompt cm.

| Character | Design height | ×base | Head-count | Build note |
|-----------|---------------|-------|------------|------------|
| Boy       | 158 cm        | 0.99  | ~7.5       | slight, wiry — youth reads via build/face, not height |
| Giant     | 297 cm        | 1.86  | ~8.5 + ~2× shoulder width | heavyweight mass, heavy brow — a huge *man*, capped (see cage) |

Landmark chain (copy into prompts):
- Boy's crown ≈ Giant's navel/waist
- King's crown ≈ Giant's mid-chest
- King stands ~a head above the average soldier
- Giant ~2× the shoulder width of any man

Scale cage — Giant (copy the WHOLE block into every shot he shares):
- Contacts: Boy's crown ≈ Giant's belt line · Giant's kneecap ≈ Boy's hip · Giant's hanging elbow ≈ just above Boy's crown
- Mass: Giant's shoulders ≈ 2× Boy's shoulder width
- Ceiling: a little under 2× Boy's height; two men of Boy's height one on the other's shoulders would overtop the Giant; both fit whole in one frame on one ground line; same size in the last frame as the first
- Build words only, never scale superlatives: "heavyweight-wrestler mass, human proportions" — never colossal/monumental/towering/earth-shaking
- Weight is relative: steps heavier and slower than Boy's; the ground stays firm
- Camera: no god's-eye overhead; high three-quarter keeping both pairs of feet in frame
```

Head-count ≈ design height ÷ ~21.5 cm (adult head); give giants a proportionally larger head so they aren't stretched men.

**Props: anchor to a body, never to cm — and give the prop its own ceiling.** "Staff ≈ the boy's own height." "The king's armor sized to swallow the boy — helmet over the eyes, hem past the shins." A large character's prop is **oversized for whoever handles it, by a stated amount**, because a prop anchored to the handler ("a shield covering a grown man shin-to-shoulder") comes out fitted to the ordinary man and wrong for the giant. But an *uncapped* oversize fails just as hard in the other direction: "enormous, built for a giant, taller than a man" produced a shield **4–5× the man's height** — a gate, not a shield. Spec a ratio + a ceiling + a landmark measurable off the image: *"≈1.35× the bearer's height, never past 1.5×; lower rim at his ankles, top rim ~2.5 head-heights above his crown, so his crown reaches only about seven-tenths of the way up the shield."* A capped prop becomes a second yardstick for the giant; an uncapped one is a second thing to go wrong. Expect to iterate: this prop took four passes (too small → 4× too large → too small again on a bad size-class analogue → correct).

**Recurring-cameo signatures.** Minor/comic characters that may reappear across projects get one or two **locked, memorable features** ("oh, it's that guy!") recorded here and in the manifest, so they stay re-identifiable everywhere.

---

## THE CAST-LINEUP PROMPT (reference-driven)

Upload the finalized identity sheets as references; the text carries layout + landmarks only, never identity:

```
UPLOAD (references, identity — do not restyle): @charA, @charB, @charC, ...

Character scale lineup, solid mid-gray studio background, even soft lighting, photorealistic.
Recreate the referenced characters exactly as in their reference images — same face, hair, skin,
build, and outfit — changing only pose and their size relative to each other.
All standing on ONE shared ground line, feet aligned, facing camera, full figure head to toe,
evenly spaced. Long lens from a distance at mid-height — no perspective foreshortening, every
figure at true comparative scale.
Left to right and their locked proportions:
[1] [charA] — the reference height.
[2] [charB] — [landmark vs charA, e.g. "same height; youth in build, not height"].
[3] [charC] — [landmark, e.g. "a full head taller; crown clears theirs by one head"].
[4] [charD] — [landmark + mass, e.g. "~2× shoulder width; B's crown reaches only its navel"].
Neutral standing poses, arms relaxed. No props, no scenery, no text labels.
```

If the tool binds references by upload order, drop the `@` tags and rely on left-to-right slot order. Register the result via **asset-librarian** as a *scale reference* element (e.g. `@cast_scale`), plus pairwise lineups (`@boy_giant_scale`) for key two-shots.

---

## QA — ACCEPT OR REJECT THE LINEUP

The lineup becomes the yardstick everything else is measured against, so it must be right first:

- **Measure pixel head-heights** of each figure in the generated lineup; confirm the ratios match the table (within a small tolerance). Off → reroll, don't accept.
- **Feet actually on one ground line?** A figure standing "closer" or floating breaks the comparison → reject.
- **Mass present, not just height?** A giant that's only tall reads wrong → reject, restate shoulder width.
- **Landmarks hold?** Eyeball the contact points against the chain (boy's crown at the giant's navel, etc.).
- **Ceiling respected?** A figure that overshoots the cap is as wrong as one that undershoots the landmark → reject. Check the *upper* bound explicitly; it is the one everyone forgets.
- **Scale-carrying prop sheets:** verify the ratio on a **separate QA-only comparison image** (silhouette + object, one ground line, correct relative scale) and put that measurement in the QA checklist as its own line. **Keep the figure out of the referenceable sheet** — a person baked into a prop sheet bleeds into every video generation that attaches it, and it eats view slots; the sheet carries size through internal proportion cues (grip sized to a normal forearm at a stated fraction of the object's width, stated aspect ratio) instead. In the comparison prompt, describe the figure as **"at correct relative scale"**, never as a "small silhouette", which invites the model to shrink the reference instead of holding the object.
- **Check the size-class analogue is in the right class.** A concrete real-world comparison ("a door leaf", "a Roman scutum") outranks every ratio line in the prompt, so a wrongly-chosen one silently overrides the whole spec — a giant's shield compared to a scutum came back man-sized despite correct ratios above it.

Reject fast, reroll in batches — a wrong yardstick corrupts every downstream shot.

---

## HANDOFF

- **asset-planner** — emits the Scale Bible table during cast breakdown, before any sheet exists.
- **asset-character** — reads the Bible for head-count/build; generates the single-pass lineup for casts where relative size matters.
- **asset-librarian** — stores each element's scale line in the manifest and registers lineups as *scale reference* elements.
- **asset-prop** — reads the prop ceiling (ratio + cap + measurable landmark) for anything a large character handles.
- **seedance-clean** — copies the **whole cage** (contacts + mass + ceiling) for every on-screen pair into the shot, restates it three times, uploads the relevant lineup, keeps compared figures at similar camera distance on a longer lens, and avoids overheads in scale shots.
