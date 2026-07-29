# Location Assets — Adel's Bedroom + Sunny Beach

## Recommendation up front

- **Adel's bedroom → generate a reference asset.** Roughly half your scenes happen here, so every clip needs to show the *same* room: same bed placement, same window, same desk, same clutter. Without a locked reference image, each video generation will invent a different bedroom and the edit will feel broken. Generate it, approve it, and reuse it as the environment reference for every bedroom shot.
- **Sunny beach → skip the asset (or treat it as optional).** It appears in one quick shot, it's generic by your own description, and nothing in it needs to match anything else. A text description inside the video prompt itself will do the job with zero extra production cost. I've still included a beach prompt below in case your pipeline requires a reference image for every location, or you later add a second beach shot.

One assumption to resolve before generating: I don't know your project's visual style (3D animation, 2D illustration, live-action photoreal). The prompts below are written with a **swappable style line** at the top — replace it with your project's actual style so the location matches your characters. Keep that style line identical across all assets in the project.

---

## Asset 1: Adel's Bedroom (generate this)

### Primary prompt — wide establishing view

```
[STYLE LINE — replace with your project style, e.g. "Warm 3D animated style,
soft global illumination, Pixar-like rendering" or "photorealistic, natural
light, shot on 35mm"]

Wide establishing shot of a child's messy bedroom, eye-level camera from the
doorway, empty of people. A single bed with rumpled colorful bedding sits
directly under the room's one large window; soft warm daylight streams
through the window onto the bed. Against the adjacent wall, a small wooden
desk is completely covered in children's drawings — loose crayon and marker
sketches layered on top of each other, a cup of colored pencils, a few
drawings taped to the wall above the desk. Toys are scattered everywhere
across the floor: building blocks, a few plush animals, a toy car, an open
toy chest overflowing in the corner. Clothes draped over a chair. The mess
is cheerful and lived-in, not dirty or gloomy — a creative, well-loved kid's
room. Walls in a soft warm color, wooden floor with a small rug. Clear view
of the full room layout: window and bed on the back wall, desk on the side
wall, open floor space in the middle. No people, no text, no watermarks.
16:9 aspect ratio.
```

### Optional companion angles (generate only if your shot list needs them)

Since half the film happens here, you'll likely shoot from more than one direction. If your video model supports multiple reference images per location, generate 1–2 reverse/side angles **after** approving the primary image, using it as an image reference to keep everything consistent:

```
Same bedroom as the reference image, identical layout, furniture, bedding,
and lighting. Camera now positioned at the window looking back into the room
toward the doorway: the desk covered in drawings visible on the left, the
open door and toy-strewn floor ahead. Same warm daylight, same color
palette. Empty of people, no text. 16:9.
```

```
Same bedroom as the reference image, identical layout and lighting.
Medium-close angle on the desk area: the desk surface piled with crayon
drawings, cup of colored pencils, drawings taped to the wall above, corner
of the bed and window visible at frame edge. Empty of people, no text. 16:9.
```

### QA checklist before approving the bedroom asset

- [ ] Bed is clearly **under the window** (this is your stated layout — video prompts will rely on it)
- [ ] Desk reads as "covered in drawings," not just cluttered with generic junk
- [ ] Toys on the floor are distinct, nameable objects (blocks, plush, car) — vague blobs will drift between generations
- [ ] Mess reads as cheerful, not neglected/depressing (matters for tone)
- [ ] Room is empty — no accidental children or figures baked into the reference
- [ ] Lighting direction is consistent and matches your story's time of day; if scenes happen at different times of day, consider generating a second lighting variant (e.g., "same room at night, bedside lamp on, cool moonlight through the window")
- [ ] No text, letters, or watermarks anywhere (AI-generated posters/drawings often contain garbled text — check the taped-up drawings closely)
- [ ] Style matches your character assets

---

## Asset 2: Sunny Beach (recommend: skip — describe in the video prompt instead)

For a single quick shot of a generic location, just fold the description into the video prompt directly, e.g.:

> "...on a bright generic sandy beach, sunny blue sky with a few small clouds, gentle turquoise waves, empty stretch of golden sand, midday sunlight..."

If your pipeline requires a reference image anyway, use this:

```
[SAME STYLE LINE as the bedroom asset]

Wide shot of a bright, generic sunny beach, empty of people. Golden sand in
the foreground, gentle turquoise waves rolling in, clear blue sky with a few
small white clouds, strong cheerful midday sunlight. Clean and simple
composition with open sand space in the mid-foreground where action could be
placed. No umbrellas, no buildings, no boats, no landmarks — deliberately
generic and timeless. No people, no text, no watermarks. 16:9 aspect ratio.
```

Quick QA if you do generate it: matches the project style line, horizon is level, no stray people/objects, lighting says "sunny and happy."

---

## Production notes

1. **Generate the bedroom first and lock it** before writing any bedroom video prompts — then reference the approved image in every bedroom shot rather than re-describing the room from scratch each time.
2. **Keep the style line identical** across the bedroom, the beach (if generated), and all character assets, or the beach shot will feel like it belongs to a different film.
3. **Name and save the approved bedroom image** (e.g., `loc_adel_bedroom_day_v1.png`) so prompts can reference it unambiguously; if you later need a night version, derive it from the approved day version, not from scratch.
