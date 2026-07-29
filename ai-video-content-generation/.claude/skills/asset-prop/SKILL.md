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

---

## PROMPT TEMPLATE

Adapt to the object — drop views or details it doesn't need:

```
Product-style reference sheet of [object] on a solid mid-gray studio background,
even soft studio lighting, soft shadows grounding the object, subtle studio reflections.
Four views of the same object, consistent across all views:
[1] front view, [2] back view, [3] side profile, [4] three-quarter view.
Object: [size relative to a hand/human if scale matters], [materials and surface finish],
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

Reject fast, regenerate in batches — a prop sheet is cheap, broken prop continuity across a whole video is not.

---

## HANDOFF

When a sheet is accepted, register it as a named element — use the **asset-librarian** skill. The element name (e.g. "tv_remote", "fantasy_dragon_egg") becomes the `@tag` your video prompts reference. If planning assets for a whole script, the **asset-planner** skill decides which props need sheets and which interactions need arrows.
