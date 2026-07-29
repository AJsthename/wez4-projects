---
name: asset-character
description: >
  Write image-generation prompts for character sheet assets used in AI video production. Use whenever the user wants to create, design, or prompt a character for their video — a character sheet, character reference, character asset, cast member, creature, or any person/being that will appear in AI-generated video. Trigger on phrases like "create a character", "character sheet for", "I need a character asset", "design the mom / hero / monster", or when a video project needs a new character reference image. Also use when the user needs a group of similar characters (army, crowd, squad). Output is an image-generation prompt plus a QA checklist for the generated sheet.
---

# Character Asset Sheets

Produce image-generation prompts for character sheets that AI video models can reliably reference. A character sheet exists for one reason: the video model should never have to guess what the character looks like. Every rule below serves that.

**Output: one image-generation prompt in a code block, followed by the QA checklist for the generated result.**

---

## THE THREE NON-NEGOTIABLES

### 1. Gray background — always

Every character sheet is generated on a **solid mid-gray background**. Extensive testing showed gray sheets perform significantly better as video references than white or black ones: gray is neutral against both light and dark scenes, doesn't blow out edge detail, and doesn't tint the character. Write it explicitly into every prompt — "solid mid-gray studio background" — never leave the background to chance.

### 2. Multiple distinct views

Request a **three-view character sheet** as the default layout. At absolute minimum the sheet must contain:

- **One clear face view** — front-facing close-up, the identity anchor.
- **One full-body view** — showing the complete outfit head to toe.

The standard three-view layout adds a third angle (3/4 or back view) so the video model knows the character from more than one side. If the character has a defining back-side feature (cape, backpack, tail, hair length), the third view must show it.

### 3. Variations for groups

If the character will appear as a **group** in the video (an army of elves, a crowd of monsters, a squad of guards), the sheet must show **3–4 distinct variations** of that character type — different heights, builds, hair, gear wear, scars. A single character used for a group produces a visually repetitive "army of clones" in the video. Vary what reads at a distance (silhouette, height, color accents), keep what defines the type (species, uniform, faction markers).

---

## RELATIVE SCALE (when size matters)

A character sheet fills its own frame, so it **cannot encode how big this character is next to another** — a boy's sheet and a giant's sheet are the same pixel height. If the project's **asset-scale** Scale Bible exists, read it and:

- **Write the head-count into the full-body view** ("proportioned ~8.5 heads tall, with a proportionally larger head" for a giant; "slight, ~7.5 heads" for a youth) so build stays consistent across generations.
- For any cast where relative size carries story weight, generate the **single-pass cast lineup** (all principals on one shared ground line, correct proportions) — that image, not the individual sheets, is what locks relative size. Individual sheets carry *identity*; the lineup carries *scale*.
- Remember height is not the only lever — **state mass/shoulder width** too, or a tall character reads as a stretched normal one.

**Recurring-cameo signature.** A minor or comic character who may reappear across projects gets one or two **locked, distinctive features** — a very long neck and a slipping helmet, a huge mustache and a dented helmet — so the audience re-identifies them ("oh, it's that guy!") every time. Bake those into the sheet and register them as critical details.

---

## PROMPT TEMPLATE

Adapt, don't fill blindly — drop what the character doesn't need:

```
Character reference sheet on a solid mid-gray studio background, even soft lighting.
Three views of the same character, consistent across all views:
[1] front-facing close-up portrait of the face,
[2] full-body front view showing the complete outfit,
[3] full-body three-quarter back view.
Character: [age] [build/species] [role], [skin/fur/surface], [hair], [eyes],
[distinctive features — scars, markings, glasses],
wearing [outfit: materials, colors, condition],
[carried items only if permanently part of the character].
Neutral standing pose, arms relaxed. Clean sheet layout, no text labels, no props, no scenery.
```

For groups, replace the three-views block with:

```
Four distinct variations of [character type] standing side by side, same species/faction,
each differing in [height, build, hair, gear wear, battle damage], sharing [the uniform /
armor style / defining trait]. Full-body front views.
```

**Writing the character description:** concrete and visible only. "Mid-40s woman, soft round face, shoulder-length auburn hair, laugh lines" beats "warm friendly mom type." The sheet locks *appearance*; personality lives in the video prompt's action.

---

## QA — ACCEPT OR REJECT THE GENERATED SHEET

The sheet is the foundation of every shot the character appears in; a flawed sheet poisons every downstream generation. Check:

- **Same person in every view?** Face, hair, and outfit must match across views. Drifting details (different buttons, changed hair part) → reject.
- **Face view clear and large?** If the face is small, soft, or shadowed → reject.
- **Outfit fully visible?** Shoes to collar, nothing cropped or occluded.
- **Background actually gray?** Gradients, scenery, or props sneaking in → reject.
- **Groups: genuinely distinct?** If two variations could be twins, regenerate with stronger stated differences.

Reject fast, regenerate in batches. Iterating on a mediocre sheet costs more than rerolling.

---

## HANDOFF

When a sheet is accepted, register it as a named element — use the **asset-librarian** skill. The element name (e.g. "Mom", "elf_soldier") becomes the `@tag` your video prompts reference, so keep it short, unique, and memorable. If planning assets for a whole script, the **asset-planner** skill decides which characters need sheets at all. For multi-character casts where size matters, the **asset-scale** skill supplies the head-counts and the cast lineup — run it before these sheets.
