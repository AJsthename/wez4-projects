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
| Giant     | 297 cm        | 1.86  | ~8.5 + ~2× shoulder width | colossal mass, heavy brow |

Landmark chain (copy into prompts):
- Boy's crown ≈ Giant's navel/waist
- King's crown ≈ Giant's mid-chest
- King stands ~a head above the average soldier
- Giant ~2× the shoulder width of any man
```

Head-count ≈ design height ÷ ~21.5 cm (adult head); give giants a proportionally larger head so they aren't stretched men. Anchor **props to a body**, never to cm: "staff ≈ the boy's own height," "the king's armor sized to swallow the boy — helmet over the eyes, hem past the shins."

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

Reject fast, reroll in batches — a wrong yardstick corrupts every downstream shot.

---

## HANDOFF

- **asset-planner** — emits the Scale Bible table during cast breakdown, before any sheet exists.
- **asset-character** — reads the Bible for head-count/build; generates the single-pass lineup for casts where relative size matters.
- **asset-librarian** — stores each element's scale line in the manifest and registers lineups as *scale reference* elements.
- **seedance-clean** — copies the landmark line for every on-screen pair into the shot, uploads the relevant lineup, and keeps compared figures at similar camera distance on a longer lens.
