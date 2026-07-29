# Location Assets — Adel's Bedroom + Beach

## Decision per location

**1) Adel's messy bedroom — GENERATE an asset.**
It hits three of the four criteria: it recurs across roughly half the scenes (continuity), the layout is specific (bed under the window, desk with drawings — the video depends on where things are), and it's a cluttered kid's space with lots of detail the model would re-invent differently every shot.

**2) Generic sunny beach — SKIP the asset.**
A plain sunny beach is exactly what modern video models handle well from text alone: one quick shot, no recurrence, no specific layout, nothing invented. Generating a plate would just add an unnecessary continuity constraint. Describe it directly in the video prompt, e.g.: "a wide sunny beach, golden sand, gentle turquoise waves, clear blue sky, bright midday light."

---

## Image prompt — Adel's bedroom

```
Child's messy bedroom, empty of people, camera at a three-quarter angle into
the room showing two walls and the depth of the space, eye-level.
Layout: single bed against the far wall directly under the window, rumpled
blanket half sliding off it; wooden desk against the right wall covered in
crayon drawings, loose paper sheets, and cups of colored pencils, a small
chair pulled out from it; open toy chest near the left wall with toys
spilling out; floor scattered with building blocks, a plush dinosaur, action
figures, and a few picture books; door in the left wall standing ajar;
crayon drawings taped to the wall above the desk.
Warm afternoon daylight coming through the window above the bed, casting
soft shadows into the room, ceiling light off.
Cozy lived-in kid's room: warm wooden furniture, pale blue walls, colorful
rug slightly bunched up, cheerful clutter everywhere but nothing broken.
Every object physically grounded and logically placed.
```

---

## QA checklist — accept or reject the generated plate

Audit corner to corner like a physics inspector. One levitating toy means the model was sloppy everywhere — **discard the whole image and regenerate a new batch**, don't try to fix it.

- **Everything supported?** No floating toys or books; furniture legs rest on the floor, nothing sinking into the rug; taped drawings actually touch the wall.
- **Everything attached and connected?** Blanket drapes off the bed naturally; drawings on the wall have visible tape/attachment; if a lamp appears, it has a cord near a plausible outlet; toy chest lid has hinges.
- **Geometry sane?** The two walls meet at a sensible angle; window sits plausibly above the bed; door and window sized correctly for a room; perspective consistent across the clutter.
- **Lighting consistent?** All shadows agree with the window as the light source; no second phantom light direction.
- **Depth visible?** You can feel the 3/4 angle — two walls and real depth between them. A flat, wall-facing shot → reject.
- **No people, no story** — the room is an empty stage.

## Handoff

Once a plate passes QA, register it via the **asset-librarian** skill (suggested element name: `adels_room`) so video prompts can reference it as `@adels_room` instead of re-describing it. The beach needs no registration — it lives as a text description inside the one video prompt that uses it.
