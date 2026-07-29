---
name: asset-planner
description: >
  Break a script, story, or video concept down into the asset production list — which characters, locations, and props need generated reference sheets before any video prompting starts. Use whenever the user has a script, storyboard, episode idea, or scene list and asks "what assets do I need", "plan the assets", "break this down", "what do we need to generate first", or starts a new AI video project. Use this BEFORE generating individual assets — it decides what to build, the asset skills decide how. Output is a prioritized asset shopping list with per-asset production notes.
---

# Asset Planner

Read a script like a line producer: extract every character, location, and prop the video needs, decide which of them earn a generated asset, and emit the production list that drives the **asset-character**, **asset-location**, and **asset-prop** skills. Planning first prevents the two classic failures: discovering a missing asset mid-shoot, and wasting generations on assets the video model never needed.

**Output: the asset production list in the exact format below.**

---

## HOW TO BREAK DOWN A SCRIPT

Go scene by scene and collect four things:

1. **Characters** — everyone who appears on screen, including background groups.
2. **Locations** — every distinct setting, noting which scenes reuse them.
3. **Props** — objects that are *held, used, or interacted with*, or that carry story weight. Set dressing that just sits in the background belongs to the location, not the prop list.
4. **Interactions** — moments where a character does something *specific* to a prop (presses THE button, pulls THE lever). These flag arrow-annotation work.

Then apply the filters:

- **Reuse is the strongest signal.** Anything appearing in 2+ scenes needs an asset — continuity across generations is what assets are for.
- **Locations get the skip test** (from asset-location): simple, generic, single-use environments can be described directly in the video prompt. Mark them SKIP with a one-line justification instead of deleting them — the decision should be visible and reversible.
- **Groups get flagged** (from asset-character): any character type appearing as multiples needs a variation sheet, or the video renders an army of clones.
- **One-shot incidental props** (a coffee cup someone sips once) usually don't need sheets — fold them into the scene description. A prop earns a sheet when it recurs, is invented/specific, or has an interaction moment.

---

## THE SCALE PASS

If more than one character shares the screen and their **comparative size carries story or comedic weight** (a giant vs a boy, a tall king above his soldiers, an adult beside a child), run the **asset-scale** skill *now* — before any sheet is generated. Each sheet fills its own frame, so relative size can't be added later; it has to be decided up front.

The scale pass produces the project **Scale Bible**: a base unit (×1.00 = the ordinary human), every character as a ratio + head-count, and a **landmark chain** ("the boy's crown reaches the giant's navel") that later gets copied into every two-shot. It also flags when a **single-pass cast-lineup** asset is needed to lock the proportions at the reference stage. Note it in the production list and put the lineup early in the production order — it's a dependency for consistent two-shots.

---

## OUTPUT FORMAT

Always use this structure:

```markdown
# Asset Production List — [Project]

## Characters
| # | Element | Scenes | Sheet type | Notes |
|---|---------|--------|-----------|-------|
| 1 | Mom | 1,2,4 | three-view | face + full body; green apron is signature |
| 2 | Elf soldiers | 3,4 | 4-variation group sheet | crowd — needs distinct builds/heights |

## Locations
| # | Element | Scenes | Decision | Notes |
|---|---------|--------|----------|-------|
| 1 | Adel's room | 1,4 | GENERATE — 3/4 angle | recurs; cluttered kid's room, layout matters |
| 2 | Beach at sunset | 5 | SKIP — describe in video prompt | generic, single scene, no layout dependency |

## Props
| # | Element | Scenes | Sheet type | Interaction notes |
|---|---------|--------|-----------|-------------------|
| 1 | TV remote | 2 | four-view + red arrow | Mom presses the green power button — arrow on it |

## Production order
1. [assets blocking the most scenes first]
2. ...

## Open questions
- [ambiguities in the script the user must resolve before generation]
```

**Production order:** sort by how many scenes an asset blocks — the recurring lead character before the scene-5 gadget. Note dependencies (the annotated remote variant depends on the clean remote sheet being accepted first).

**Open questions:** scripts underspecify. If the script says "the device" and three shots depend on what it looks like, don't invent it silently — list it as a question. The planner's job is to surface these gaps *before* generation, when they're cheap.

---

## HANDOFF

Each GENERATE row routes to its skill: **asset-character**, **asset-location**, or **asset-prop**. When the scale pass applies, **asset-scale** runs first and its Scale Bible feeds all of them. As assets get accepted, they're registered by the **asset-librarian** — the Element names chosen here should already be tag-friendly (short, unique), because they become the manifest's element names and `@tags`.
