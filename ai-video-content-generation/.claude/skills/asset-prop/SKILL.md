---
name: asset-prop
description: >
  Write image-generation prompts for prop sheet assets used in AI video production. Use whenever the user wants to create or prompt an object that will appear in AI-generated video — a prop, item, device, weapon, vehicle, product, artifact, or any physical object a character will hold, use, or interact with. Trigger on phrases like "create a prop", "prop sheet", "I need an asset for the remote / sword / potion bottle", "reference image for the object", or when a video project needs an object reference. Also use when a video requires a precise interaction with a prop (pressing a specific button, pulling a specific lever). Output is an image-generation prompt plus a QA checklist for the generated sheet.
---

# Prop Asset Sheets

Produce image-generation prompts for prop sheets that AI video models can hold onto. Props follow the exact same sheet discipline as characters — a neutral studio document of the object from several sides — because the video model treats them the same way: a visual identity it must not reinvent mid-shot.

**Output: one image-generation prompt in a code block, followed by the QA checklist for the generated result.**

---

## THE THREE NON-NEGOTIABLES

### 1. Character-sheet format: gray background, multiple views

Every prop sheet uses a **solid mid-gray studio background** and **multiple views** — a **four-view sheet** is the default (front, back, side, three-quarter). Same reasoning as character sheets: gray is neutral against any scene, and multiple angles give the video model several references to hold onto instead of one angle it must hallucinate around. For flat-ish objects (a card, a phone) three views may suffice; for complex objects (a vehicle, a machine) add a top or detail view.

### 2. Physical volume is the acceptance bar

A prop that looks flat or 2D is useless — the video model will move it through 3D space, and a flat reference produces cardboard-cutout artifacts. Prompt for, and later verify, the evidence of volume:

- realistic shapes and proportions
- visible surface textures (brushed metal, worn leather, matte plastic)
- cast shadows grounding the object
- **soft studio reflections** on the surface

These aren't aesthetics — they're proof the object has physical volume the video model can rotate and light.

### 3. Red arrow for critical interactions

If the video requires a **specific interaction point** — pressing one particular button on a remote, gripping a specific handle, inserting a key into a specific slot — edit the sheet to include **a literal red arrow pointing at the exact spot**. This is the field-tested hack that tells the video model exactly where the character's hand goes. Either prompt the arrow into the sheet directly ("a bold red arrow pointing at the round green button") or add it in an edit pass after the sheet is accepted. One arrow per interaction; more than two arrows on one sheet gets noisy — make a second annotated copy instead.

### 4. Scale-critical props need a ratio, a ceiling, and internal proportion cues — never a figure in the sheet

A prop whose *size* is the point — a giant's shield, a king's armor on a boy, an oversized weapon — fails in **both** directions, and the two failures look nothing alike:

- **Anchored to the handler → too small.** "A shield covering a grown man shin-to-shoulder" generates a shield that fits that man perfectly. On screen it reads as *his* shield, not the giant's, and the whole point is lost.
- **Anchored to superlatives → far too large.** The re-spec "an enormous body shield built for a giant warrior, taller than a man, wide enough to crouch behind with room to spare" came back at roughly **4–5× the man's height** — a gate, not a shield. "Taller than a man" is a floor with no maximum, and every superlative reads as "more."

So spec three things together:

1. **A ratio to a body** — "≈1.35× the bearer's height."
2. **A ceiling** — "never past 1.5× his height."
3. **A landmark measurable off the finished image** — "lower rim at his ankles, top rim about two and a half head-heights above his crown, so **his crown reaches only about seven-tenths of the way up the shield**." Then make that measurement a line in the QA checklist.

4. **A real-world size-class analogue** where one exists — "a little taller than a full-height door leaf." This is an absolute the adjectives can't argue with, which makes it **the strongest single lever in a prop prompt — and therefore the most destructive one to get wrong.** A correct set of ratios was overridden wholesale by naming *"the same size class as a Roman scutum or a Norman kite shield"*: both are **man-fitted** shields, so the generation came back at 0.85× the man despite every ratio line above it. **Verify the analogue actually sits in the target size class before naming it**, and drop function phrases that imply a comfortable fit ("a shield he could hold") — keep only ones that imply strain ("it takes both his arms and his shoulder to move").

**Carry size through internal proportion cues, and keep people out of the sheet.** Do **not** put a yardstick figure in a referenceable sheet:

- It is a **bleed risk.** Every video prompt that attaches that sheet is attaching a picture of a person, and the video model may render them into the shot.
- It **eats view slots** — a silhouette in every view cost two of four views, so the sheet delivered only three angles of the actual object.

Instead, make the object's own geometry report its size: **grip and strap sized to a normal adult forearm and spanning only a fraction of the object's width** (the single most effective cue — a strap that looks like a comfortable fit reads as a man-sized prop), a **boss/handle/control as a stated fraction of the whole**, and an explicit **aspect ratio**. These read as "built for someone far larger" with no person in frame.

When the ratio still needs proving, generate a **separate QA-only comparison image** — silhouette and object side by side on one ground line at correct relative scale — check the landmark off it once, and **never register or upload it**. Never describe that figure as a *"small* silhouette": the model will shrink the yardstick to satisfy "small" rather than hold the object's size, which is how a 4× oversized shield happened.

**State empty hardware positively.** "No hands" in the trailing exclusion list produced a leather glove and a gripping hand inside the strap. Write it as a property of the object: *"the forearm strap and hand-grip are empty and unoccupied — bare leather and bare wood, the inner face plainly visible through and around them."*

---

## PROMPT TEMPLATE

Adapt to the object — drop views or details it doesn't need:

```
Product-style reference sheet of [object] on a solid mid-gray studio background,
even soft studio lighting, soft shadows grounding the object, subtle studio reflections.
Four views of the same object, consistent across all views:
[1] front view, [2] back view, [3] side profile, [4] three-quarter view.
Object: [size relative to a hand/human if scale matters — for scale-critical props give internal
proportion cues: grip/strap sized to a normal hand or forearm and spanning only a stated fraction of
the object's width, a stated aspect ratio, and a size-class analogue verified to be in the right
class. Keep every human figure out of the sheet], [materials and surface finish],
[colors], [condition — new, worn, scratched], [critical details: buttons, labels, markings
described exactly — position, color, shape].
Clean sheet layout, no text labels, no hands, no scenery.
```

With an interaction arrow:

```
..., [4] three-quarter view with a bold red arrow pointing directly at [the exact
feature — "the large round green button on the upper left"].
```

**Critical details in words.** If a button, logo, or marking matters in the video, describe it exactly (position, color, shape) — small details are the first thing generation drops, and the sheet is where they get locked.

---

## QA — ACCEPT OR REJECT THE GENERATED SHEET

- **Volume test first:** does it look like a physical object photographed in a studio, or a sticker? Flat shading, missing shadows, no reflections → **reject**.
- **Same object in every view?** Button count, proportions, wear marks must match across views. If the back view invents new geometry → reject.
- **Critical details present and correct?** The button/label/marking the video depends on must be clearly visible in at least one view.
- **Background actually gray?** Scenery, surfaces with visible texture, or gradient backdrops → reject.
- **Arrow (if used) unambiguous?** It must point at exactly one spot, clearly, in red.
- **No people in the sheet.** Any human figure, silhouette, mannequin, hand, arm or glove in any view → **reject**. It will bleed into video generations. Straps, grips and handles must read as empty.
- **Scale-critical prop: measure the internal cues.** Grip/strap/handle sized to a normal human hand or forearm and occupying the stated fraction of the object — a strap that looks like a comfortable fit means the prop is reading man-sized → reject. Aspect ratio as specified. Verify the ratio itself on the **separate QA-only comparison image**, checking **both** bounds: undershooting the ratio and overshooting the ceiling are equally wrong, and the ceiling is the one that gets forgotten. That comparison image is never registered and never uploaded to a video prompt.

Reject fast, regenerate in batches — a prop sheet is cheap, broken prop continuity across a whole video is not.

---

## HANDOFF

When a sheet is accepted, register it as a named element — use the **asset-librarian** skill. The element name (e.g. "tv_remote", "fantasy_dragon_egg") becomes the `@tag` your video prompts reference. If planning assets for a whole script, the **asset-planner** skill decides which props need sheets and which interactions need arrows.
