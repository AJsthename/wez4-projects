---
name: asset-location
description: >
  Write image-generation prompts for location assets used in AI video production. Use whenever the user wants to create or prompt an environment for their video — a location, set, room, interior, exterior, backdrop, or scene setting that AI-generated video will take place in. Trigger on phrases like "create a location", "I need the bedroom / spaceship bridge / forest clearing", "location asset", "environment reference", "generate the set". Also use when deciding whether a location even needs a generated asset or can just be described in the video prompt directly, and when writing or fixing a **reverse / back-view plate** of a location already generated ("the back view just mirrors the front", "reverse shot plate", "180° opposite angle"). Output is either an image-generation prompt plus a QA checklist, or a recommendation to skip the asset.
---

# Location Assets

Produce image-generation prompts for location plates that AI video models can build scenes inside. The final video inherits this image's geometry, lighting logic, and physical coherence — the location asset is the stage everything else performs on.

**Output: one image-generation prompt in a code block plus the QA checklist — or, when the skip rule applies, a short recommendation to describe the setting directly in the video prompt instead.**

---

## FIRST DECISION: DOES THIS LOCATION NEED AN ASSET AT ALL?

Not every location earns a generated asset. Modern video models handle **simple, generic environments** well from text alone — a plain beach at sunset, an empty highway, a generic office. Generate a location asset when any of these hold:

- The location **recurs across multiple shots** and must stay identical (continuity).
- The layout is **specific** — the video depends on where the door, window, or desk is.
- The space is **cluttered or detailed** — a kid's bedroom, a workshop, a market stall.
- The location is **invented** — a fantasy interior, a spaceship bridge, anything the model can't default to.

If none apply, say so: recommend describing the setting directly in the video prompt and skip the asset. An unnecessary asset is an unnecessary continuity constraint.

---

## THE TWO NON-NEGOTIABLES

### 1. 3/4 camera angle for interiors

For indoor or enclosed locations, always prompt a **3/4 angle** — the camera positioned diagonally into the room, seeing two walls and the depth between them. A flat frontal view gives the video model one plane and no depth cues; the 3/4 angle shows how the room actually occupies space, which is what keeps the geometry from breaking when the video camera moves. State it explicitly: "camera at a three-quarter angle into the room, showing two walls and the depth of the space."

For exteriors, choose the angle that shows the spatial relationships the video needs (where the path leads, how buildings face each other) — the same principle, applied outdoors.

### 2. Physical logic is the acceptance bar

The video quality rests on this base image being **completely coherent**. Every object must obey physics and make sense: things sit *on* surfaces, hang *from* attachments, connect *to* what powers them. A location with sloppy details — levitating sneakers, headphones attached to nothing, a shelf with no bracket, a lamp with no cord near no outlet — gets **discarded**, not fixed. Generate a new batch.

---

## REVERSE / BACK-VIEW PLATES — THE SOLID-ANCHOR RULE

When a location needs a **reverse plate** for shot/reverse-shot cutting, how you write it depends entirely on what the camera is looking at. Getting this wrong is the single most common way a back view comes back as a mirrored copy of the front.

**Enclosing anchors** — a room, a tent, a lab, a valley basin, an open plain: spaces the camera stands *inside*. Turning 180° genuinely swaps left and right, because you are seeing the *same* surfaces from the other end. Mirror language works here: "the map table now on the left, mirrored from the front view."

**Solid anchors** — a house, a statue, a vehicle, a wall: objects the camera stands *outside* and looks *at*. Crossing to the other side mirrors nothing. It reveals **a surface the front view never showed**, and no reference image contains it. The model has nothing to copy, so if the prompt says "the 180° reverse" or "mirrored", it flips the façade it *can* see and returns a juxtaposition — the same front wall, handed back left-right swapped.

Write solid-anchor reverses like this:

1. **Place the camera in world terms, not relative terms.** "Camera on the higher ground behind the house, up-slope side, looking down past the building" — not "the 180° reverse of the front view." Relative phrasing invites a transform of the reference image; absolute phrasing describes a place to stand.
2. **Describe the hidden face from scratch.** It is new content, so it needs real detail — what is actually on that wall: window openings, a roof stair, stored jars, a lean-to, weathering. A prompt that never says what the back looks like is asking the model to invent or copy, and it will copy.
3. **State positively where the front-side features went.** "The arched doorway and the provisions table are on the far side, hidden behind the building" places them out of frame. Phrase it as location, never as prohibition — the model needs somewhere to put them.
4. **Restrict the reference to identity, and say so in the prompt.** "@tag sets the building's construction, materials, proportions and the hillside it stands on; this plate shows the opposite face of that same building." The `@tag` locks *what it is*; your text locks *which side you see*.

**QA the reverse specifically:** if the plate returns the same façade with left and right swapped, that is a mirror, not a reverse — discard it. The correct plate shows different features on a wall that shares the front view's materials, proportions, and roofline.

### Stacking references — and what they cost

Once a location has two or more accepted plates, a further view (an overhead map, a detail angle) is usually worth referencing **all** of them: between them they hold the site's full inventory, and objects that appear in only one plate would otherwise go missing. That is a real gain, and the reason to do it.

The cost is directional pull. **Every reference you attach is more evidence for the vantage those references were shot from** — two eye-level plates argue twice as hard that this location is seen at eye level, and a request for a true top-down comes back as a tilted high-angle. The rule generalizes from solid anchors: references carry identity, text carries geometry, and adding references means the geometry language has to get *stronger*, not stay the same. Pay for extra references by stating the vantage in absolute terms ("the roof reads as a flat shape seen face-on, walls showing only as thickness at the roof edge"), fixing a frame orientation ("the hillside rising toward the top of frame"), and describing whatever surface the new vantage exposes from scratch — an overhead of a building needs its roof written out, because no eye-level plate contains it.

---

## PROMPT TEMPLATE

Adapt to the space — this is the interior form; simplify for exteriors:

```
[Location type], empty of people, camera at a three-quarter angle into the room
showing two walls and the depth of the space, eye-level.
Layout: [what is on the left wall], [what is on the right/far wall],
[what sits in the middle], [floor and what's on it], [window/door positions].
[Time of day] light from [source and direction], [practical lights on/off].
[Style/mood in concrete terms: materials, colors, condition, tidiness level].
Every object physically grounded and logically placed.
```

**Describe the layout spatially**, not as an inventory. "Bed against the left wall under the window, desk in the far right corner, clothes piled on the chair beside it" gives the model geometry; "a bedroom with a bed, desk and clothes" gives it a shopping list to scatter.

**No people, no story.** The location is an empty stage. Characters come from character sheets; putting them in the location plate creates conflicts later.

---

## QA — ACCEPT OR REJECT THE GENERATED PLATE

Audit like a physics inspector, corner to corner:

- **Everything supported?** No floating objects, no furniture legs sinking into the floor, no shelves without mounts.
- **Everything attached and connected?** Cords, hinges, brackets, straps — objects that need them have them.
- **Geometry sane?** Walls meet at sensible angles, perspective consistent, doors/windows plausibly sized.
- **Lighting consistent?** Shadows agree with the stated light source.
- **Depth visible?** For interiors: can you feel the 3/4 angle — two walls and real depth? A flat wall-facing shot → reject.

One levitating sneaker means the model was sloppy everywhere — **discard and regenerate a new batch** rather than hoping the video model ignores it. It won't.

---

## HANDOFF

When a plate is accepted, register it as a named element — use the **asset-librarian** skill. The element name (e.g. "adels_room", "dragon_cave") becomes the `@tag` your video prompts reference. If planning assets for a whole script, the **asset-planner** skill applies the skip rule across all locations at once.
