# Pancake Run — Asset Breakdown (60s Animated Short)

The rule of thumb for AI video work: anything that appears in **more than one shot**, or that the audience will track continuously, needs a generated reference asset before you prompt a single video shot. One-off background elements can be described inline in the video prompt.

Here's the breakdown by scene coverage:

| Element | Appears in | Asset needed? |
|---|---|---|
| Mom | Scenes 1, 5 | Yes — character sheet |
| The dog | Scenes 3, 5 | Yes — character sheet |
| The pancake | Scenes 1, 2, 3, 4, 5 | Yes — hero prop sheet |
| Kitchen | Scenes 1, 2 (window), 5 | Yes — location reference |
| Suburban street + bakery | Scenes 2, 3, 4 | Yes — location reference |
| Street performer | Scene 4 only | Borderline — light reference recommended |
| Performer's hat | Scene 4 only | Fold into performer's sheet |
| Pigeons | Scene 4 only | No — describe in prompt |
| Frying pan / spatula | Scenes 1, 5 | Optional — fold into kitchen or Mom's sheet |

## Priority 0 — Style frame (do this first)

Before any character or location, generate **one style frame** that locks your visual language: animation style (e.g., Pixar-ish 3D, 2D cel, stop-motion look), color palette, lighting mood, lens/rendering feel. Every other asset gets generated *in this style* so the whole short feels like one film. Without this, your kitchen and your street will look like they came from two different movies.

## Priority 1 — Characters (multi-scene, identity-critical)

**1. Mom** (Scenes 1 & 5)
- Character sheet: front, 3/4, and side views; neutral background.
- Lock: hairstyle, apron/outfit, age, build, facial features.
- Include an expression pass if you can (cheerful flipping face + the Scene 5 shrug).
- She bookends the film — if she drifts between Scene 1 and Scene 5, the payoff dies.

**2. The Dog** (Scenes 3 & 5)
- Character sheet: front, side (critical — he's mostly seen running in profile), and 3/4.
- Lock: breed/silhouette, coat color and markings, collar color, ear and tail shape.
- He's your action star; the chase is the centerpiece of the short. Side-profile fidelity matters most.
- Bonus: one reference pose of him balancing something on his nose for Scene 5.

**3. Street Performer** (Scene 4 only)
- Lighter-weight sheet — one solid 3/4 reference is enough since he's in one scene.
- Include the hat **on his head and worn as he'd hold it out / have it on the ground**, since the hat is the pancake's landing zone.
- If your Scene 4 is a single shot, you could skip him and describe inline — but a punchline scene with a specific physical gag (pancake lands in hat) benefits from a locked design.

## Priority 2 — Hero prop

**4. The Pancake**
- This is your protagonist's MacGuffin — it appears in **all five scenes** and travels across every location. It's the most continuity-sensitive object in the film.
- Prop sheet: top view, side view (shows thickness), and a slight 3/4 angle.
- Lock: size relative to a hand/plate, golden-brown tone, char pattern, edge shape. Decide now whether it has butter/syrup on it (it shouldn't, if it's flying — keep it dry and clean for continuity).
- Also useful: one in-flight reference (spinning, slight motion suggestion) since it's airborne in Scenes 2–4.

## Priority 3 — Locations

**5. Cozy Kitchen** (Scenes 1, 5, and the window in Scene 2)
- Wide establishing reference showing: the stove area, the open window (must exist and be visibly open in Scene 1 so the Scene 2 gag reads), and the door the dog exits/enters through.
- Lock: color palette, cabinet style, window position relative to the stove, morning light direction.
- The window and door placement are *story geography* — plan them so Scene 1's flip, Scene 2's exit, and Scene 5's return all make spatial sense.

**6. Suburban Street with Bakery** (Scenes 2–4)
- Wide reference of the street: houses, sidewalk, the little bakery storefront.
- Consider a second angle or a bakery close-up if the dog runs *past* it in a tracking shot (the bakery is a nice visual joke — pancake escaping past a bakery — so it deserves to read clearly).
- The performer's corner (Scene 4) can be a spot on this same street — generate it as part of this environment or as one extra angle, not a separate location. Keeping it one continuous street helps the chase feel geographically coherent.

## Skip — describe inline in the video prompts

- **Pigeons** — generic flock behavior, single scene, models handle "a flock of pigeons swarms in" well without a reference.
- **Frying pan / spatula / plates** — standard kitchen objects; include them in the kitchen location reference or just describe them. Only make a pan prop sheet if you want a distinctive design (e.g., a signature red pan) featured in close-up.
- **Sky/exterior of the house for Scene 2** — the pancake-sailing shot can be prompted from the street location reference.

## Suggested generation order

1. Style frame (locks the look)
2. Mom → Dog → Pancake (characters and hero prop, in style)
3. Kitchen → Street/bakery (locations, in style)
4. Street performer + hat (lighter pass)
5. Optional: composite test frame — Mom in the kitchen holding the pan — to verify character + location assets combine cleanly before you start video prompting.

**Total: 6 core assets + 1 style frame.** That's a manageable pre-production batch, and with the pancake, Mom, dog, and both locations locked, every one of your five scenes can reference consistent imagery instead of re-rolling descriptions and praying for continuity.
