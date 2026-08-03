# The Goliath Complex — Prop Assets: Descriptions & Generation Prompts

**Project:** "The Goliath Complex" (Gulayat) — ANN / David & Goliath, 1 Samuel 17
**Style:** Realism/Hyperrealism (not 3D animation)
**Sheet standard:** Solid mid-gray studio background · four-view product-style layout (front, back, side, 3/4) · soft studio lighting, grounding shadow, subtle reflections (physical *volume* is the acceptance bar) · scale stated as a **body landmark**, never in centimetres · no text labels, no hands, no scenery.

> **No people in a referenceable sheet — ever.** Not a figure, not a silhouette, not a mannequin, not a hand. A person baked into a prop sheet is attached to every video prompt that references that prop, and the video model may render them into the shot. It also wastes view slots. Size is carried by **internal proportion cues** (a grip sized to a normal forearm and spanning a stated fraction of the object) and by the **body-landmark text in the video prompt** — never by a figure in the sheet. If a ratio needs visual proof, generate a **separate QA-only comparison image**, check it once, and never register or upload it.
>
> **State empty hardware positively.** The trailing "no hands" exclusion is not reliable — it produced a leather glove and a gripping hand inside `@goliath_shield` v2's strap. For anything with a strap, grip, handle, hilt or opening, write it as a property of the object: *"the forearm strap and hand-grip are empty and unoccupied — bare leather and bare wood, the inner face plainly visible."* This matters most for the still-unbuilt `@saul_armor`, where a mannequin or body form is the obvious failure mode.
**Scale source:** [crs_table_Goliath_Complex.md](crs_table_Goliath_Complex.md) (the Scale Bible). Built with the **asset-prop** skill.

---

## What earns a prop sheet (triage)

Rule (from asset-prop / asset-planner): a prop earns a sheet when it is **held/used/interacted with**, **recurs**, or is **invented/specific**. Set dressing that just sits in a room belongs to the *location* plate. **Worn armor is costume** — it lives on the character sheet, not here — *unless* it is handled or worn by someone else on screen.

| # | Prop | Tag | Sheet? | Why | Scale anchor |
|---|------|-----|--------|-----|--------------|
| 1 | Goliath's spear | `@goliath_spear` | GENERATE | carried, hero weapon, scale gag | shaft **taller than Saul** |
| 2 | Goliath's tower shield | `@goliath_shield` | GENERATE (**v2 pending**) | carried by shield-bearer "before him" | **taller than the bearer** — top rim above his crest, lower rim at his ankles (≈1.5× the v1 sheet) |
| 3 | Goliath's sword | `@goliath_sword` | GENERATE | David draws it to behead Goliath (interaction) | so large David needs **both hands**, nearly his own height |
| 4 | David's shepherd's staff | `@david_staff` | GENERATE | carried, then thrown aside; "a stick" gag | ≈ **David's own height** when planted |
| 5 | David's sling, pouch & 5 stones | `@david_sling_kit` | GENERATE | the hero weapon; slow-mo stone (Clip 89) | sling hand-length; stones **fist-sized** |
| 6 | King Saul's royal armor set | `@saul_armor` | GENERATE | worn by David — the "swallows him" gag (Clip 80) | sized for a **185 cm king**; swallows 158 cm David |
| 7 | Jesse's provisions (grain basket, 10 loaves, 10 cheeses) | `@jesse_provisions` | GENERATE (light) | handed over + shown to Eliab (Clips 25–26, 59) | loaves/cheeses **hand-sized**; basket two-handed |
| 8 | Provisions handcart | `@provisions_cart` | GENERATE | David loads & rides off / unloads (Clips 27, 43) | waist-high, loads the provisions |
| 9 | ANN camera rig (video camera + zoom mic) | `@ann_camera` | GENERATE | Tec films throughout; recurs | shoulder-held; mic a forearm long |
| 10 | ANN drones (pair) | `@ann_drones` | GENERATE | aerial shots; invented modern | two-hand carry each |
| 11 | ANN tablet | `@ann_tablet` | GENERATE | Clarissa/Chris track the timeline; recurs | hand-held, two-hand |
| 12 | Chris's ANN smartwatch (the "two-hour clock") | `@ann_watch` | GENERATE + red arrow | plot ticking-clock; flashes (Clips 28, 94) | wrist-sized |
| 13 | ANN incursion artifact | `@ann_artifact` | GENERATE (optional) | invented lore object; flashback (Clips 16–17) | two-hand held |

**On the sheet as COSTUME, not a prop (do not generate here):** Goliath's worn bronze helmet, coat of mail, greaves → part of **Goliath's character sheet**. The helmet that *flies off* in Clip 89 is that same worn helmet — describe it in the shot, no separate sheet. ANN headcam and backpacks → part of the **ANN character sheets** (worn kit).

**Inline-only (describe directly in the Seedance prompt, no sheet):** the swirling portal VFX, the Jericho-walls and Red-Sea montage effects, the flying stone's motion trail, generic tents/food not handled.

**Not props — see the separate file:** the **ANN logo system** and **crew wardrobe (jacket)** are brand/wardrobe assets, in [Goliath Complex - Brand & Wardrobe Assets](Goliath%20Complex%20-%20Brand%20&%20Wardrobe%20Assets_%20Descriptions%20&%20Prompts.md).

> **ANN modern-gear note:** generate every ANN prop as the **real modern object** (that is what the viewer sees). The in-world "incursion field makes it look like an everyday object to the ancients" is a **per-shot effect**, not the asset — don't bake it into the sheet.

---

## 1. Goliath's Spear — `@goliath_spear`

**Description:** The champion's oversized thrusting spear. Shaft "like a weaver's beam" (1 Sam 17:7) — thick, dark, hardwood — with a massive iron leaf-shaped head. Proportioned to a 297 cm giant: the whole spear is **taller than King Saul** stood beside it. Heavy, brutal, battle-worn.

### Image-Generation Prompt
```
Product-style reference sheet of an ancient oversized war spear on a solid mid-gray studio background,
even soft studio lighting, soft shadow grounding it, subtle studio reflections on the metal.
Four views of the same object, consistent across all views:
[1] front, [2] back, [3] side profile, [4] three-quarter view.
Object: a giant's thrusting spear, taller than a tall man — an exceptionally thick dark hardwood shaft
"like a weaver's beam", bound with worn leather grips, tipped with a massive leaf-shaped iron head with
a raised central spine and a bronze collar, plus an iron butt-spike at the base. Weathered, nicked,
oiled dark iron. Oversized and heavy, clearly built for a colossal warrior.
Clean sheet layout, no text labels, no hands, no scenery.
```
### QA Checklist
- [ ] Same spear in all four views — head shape, shaft thickness, grip wraps consistent
- [ ] Reads **oversized / heavy** — a giant's weapon, not a normal soldier's
- [ ] Iron head has real volume (shadow, reflection) — not a flat cutout
- [ ] Wood grain + leather wrap textures visible
- [ ] Background solid mid-gray, no scenery
> **Scale in the shot:** state "the shaft is taller than King Saul" / "longer than a man is tall" — never centimetres.

---

## 2. Goliath's Tower Shield — `@goliath_shield`

**Description:** The body-shield carried *before* Goliath by his shield-bearer. It is sized to Goliath's frame rather than fitted to the 165 cm man who lugs it — **about one and a third the bearer's own height (target 1.35×, ceiling 1.5×), and roughly two and a half times as tall as it is wide.** Standing it on the ground beside the bearer, its lower rim sits at his ankles and its top rim about two and a half head-heights above his crown, so **his crown reaches only about seven-tenths of the way up the shield** and his shoulders sit a little above its midpoint. Wide enough to cover Goliath's chest — about twice an ordinary man's shoulder span — so the bearer can crouch entirely behind it. On Goliath the shield covers shin to upper chest. Bronze-faced over wood and hide, with a domed central boss. Not strapped to Goliath — the bearer holds it, and it takes both his arms and his shoulder to move (Clips 3, 83, 88).

**The accepted design is v3's** — vertical wood planks under a bronze cross-band and rim, domed boss, dark patina. v4 changes **size only**, plus two hygiene fixes. Keep the look.

> ### ⚠️ Generation log — v1 too small, v2 4–5× too large, v3 too small again, v4 = design locked + size fixed
> - **v1** — specced *"covers a grown man shin-to-shoulder"*, generated at exactly that: a well-fitted shield for the bearer, not a champion's.
> - **v2** — over-corrected to ~**4–5×** the man's height (a gate) on *"enormous"*, *"built for a giant warrior"*, *"with room to spare"*, and a *"**small** grey silhouette"* yardstick the model duly shrank.
> - **v3** — bounded ratios were correct and internally consistent, and the model **ignored them and came back at ~0.85× the man** (shield to his shoulder — a v1 repeat). **Cause: the size-class analogue was in the wrong class.** *"The same size class as a Roman scutum or a Norman kite shield"* names two **man-fitted** shields, and it was the most concrete statement in the prompt, so it beat every ratio line. *"A shield he could hold"* and *"a heavy burden for one man"* pulled the same way. **A size-class analogue is the strongest lever in a prop prompt — which makes a wrongly-chosen one the most destructive.** Verify the analogue is actually in the target class before naming it; here, a door leaf is, a scutum is not.
> - **v3's second, worse problem — the yardstick figure was baked into the referenceable sheet.** A human figure inside a prop sheet is a **bleed risk**: every video prompt that attaches this sheet is attaching a picture of a man, and Seedance may render him. It also ate two of the four view slots, so the sheet only delivered three object views. **A referenceable sheet must contain the object and nothing else.** The scale proof belongs in a separate, QA-only image that is never uploaded to a video prompt.
> - **v4 (below)** — two prompts: the **hero sheet** (object only, no figure, empty strap) which becomes `@goliath_shield_v4.png`, and an optional **scale-check image** used once to verify proportion and then set aside. Tag unchanged (`@goliath_shield`).
>
> See the [scale cage](crs_table_Goliath_Complex.md#the-scale-cage-bounding-a-giant).

### Image-Generation Prompt (v4 — the hero sheet, this is the referenceable asset)

No human figure of any kind. Absolute size is carried by the **internal proportion cues** (strap width, boss size, aspect ratio) — these read as "built for someone much larger" without putting a person in the frame:

```
Product-style reference sheet of a large ancient tower shield on a solid mid-gray studio background,
even soft studio lighting, soft grounding shadow, subtle reflections on the bronze.
Four views of the same object, consistent across all views:
[1] front, [2] back, [3] side profile, [4] three-quarter view.
Object: a tall rectangular-oval body shield with rounded ends, roughly two and a half times as tall as
it is wide. Vertical wooden planks across the face under a bronze vertical spine and horizontal
cross-band, a domed central bronze boss, riveted bronze rim, dark weathered bronze and aged wood,
battle-scarred and dented.
Proportions that set its size — hold these exactly: the domed central boss is about a quarter of the
shield's width, the size of an adult man's head. On the back, a single broad leather forearm strap
and a wooden hand-grip, both sized for an ordinary adult man's arm, together spanning only about a
third of the shield's width and sitting well inside the rim, so the shield is clearly far larger than
the man who would carry it. About seven vertical planks across the face. In height it is a little
taller than a full-height interior door leaf.
The forearm strap and hand-grip are empty and unoccupied — bare leather and bare wood, the shield's
inner face plainly visible through and around them.
The shield stands alone in every view. Clean sheet layout, no text labels, no scenery.
```

### QA Checklist — hero sheet
- [ ] **The object stands alone — no human figure, silhouette, mannequin or partial body in any view.** Any figure at all → reject and reroll; it will bleed into video generations
- [ ] **Strap and grip are empty** — no glove, no gauntlet, no hand, no forearm, no arm inside them
- [ ] **Strap + grip span ≈ ⅓ of the shield's width; boss ≈ ¼ of the width.** If the strap looks like a comfortable fit across the back, the shield is reading man-sized → reject
- [ ] Aspect ratio ≈ **2.5 : 1** (tall, not a door-shaped slab or a narrow plank)
- [ ] Four **object** views present — front, back, side profile, three-quarter (no view spent on anything else)
- [ ] Design matches the accepted v3 look — vertical planks, bronze spine + cross-band, domed boss, dark patina
- [ ] Curvature/thickness visible in the side view (volume, not a flat plate)
- [ ] Consistent dents/wear across views; background solid mid-gray

### Image-Generation Prompt (v4-scale — QA ONLY, never upload to a video prompt)

Run this **once** to confirm the size reads right, check it, then set it aside. Do **not** register it as a referenceable element and do **not** attach it to a Seedance prompt — it contains a human figure by design, which is exactly what must not reach a video generation.

```
Scale comparison diagram on a plain mid-gray background, flat even lighting, orthographic side-by-side
layout, no perspective.
On the left, a plain flat grey silhouette of an average-height adult man, standing upright, facing
forward, arms at his sides.
On the right, standing on the same ground line, a tall rectangular-oval bronze-and-wood tower shield
with a domed central boss, resting upright on the ground.
Their relative size, drawn exactly: the shield is about one and a third times the man's height. Its
lower rim is level with his ankles and its top rim rises about two and a half head-heights above the
top of his head, so THE MAN'S CROWN REACHES ONLY ABOUT SEVEN-TENTHS OF THE WAY UP THE SHIELD and his
shoulders sit a little above the shield's midpoint. The shield is about twice as wide as his
shoulders are broad.
Two separate objects side by side, not touching. No text, no labels, no arrows, no scenery.
```

### QA Checklist — scale check
- [ ] **Measure it: the man's crown lands at ~0.7 of the shield's height** (shoulders a little above the midpoint). Crown at or above ~0.85 → too small, a v1/v3 repeat. Crown below ~0.4 → too large, a v2 repeat
- [ ] Shield height reads **between 1.2× and 1.5× the man** — a little taller than a doorway, never a gate or a wall
- [ ] Shield width ≈ twice the man's shoulder span
- [ ] Both objects on one ground line, no perspective foreshortening
- [ ] **This image is filed as QA evidence only** — not registered, not uploaded to any Seedance prompt
> **Scale in the shot:** state "its lower rim at the shield-bearer's ankles, its top rim about two and a half head-heights above his crown — his crown reaching only about seven-tenths of the way up the shield" — never centimetres, and never a bare "taller than a man" (a floor with no ceiling is what produced v2). The shield then works as a **second yardstick** capping Goliath's size in frame, which only holds if the shield itself is capped.

---

## 3. Goliath's Sword — `@goliath_sword`

**Description:** The giant's sword — the weapon David ultimately uses to behead Goliath (Clip 91, "David needs both hands"). A massive bronze/iron blade, Philistine style, far too large for an ordinary man to wield one-handed.

### Image-Generation Prompt
```
Product-style reference sheet of a giant's ancient sword on a solid mid-gray studio background,
even soft studio lighting, soft grounding shadow, subtle metallic reflections.
Four views of the same object: [1] front (full blade), [2] back, [3] side edge profile, [4] three-quarter.
Object: an oversized ancient Philistine sword, so large a normal man would need both hands — a broad
straight double-edged blade of dark oiled iron with a bronze crossguard, a leather-wrapped grip long
enough for two hands, and a heavy bronze pommel. Nicked, battle-worn, faint bloodline down the fuller.
Clean sheet layout, no text labels, no hands, no scenery.
```
### QA Checklist
- [ ] Reads **oversized** — proportioned so a slight youth would need both hands and it is nearly his own height
- [ ] Same blade/guard/pommel across all four views
- [ ] Edge profile view shows real blade thickness (volume)
- [ ] Metal + leather textures, grounding shadow present
- [ ] Background solid mid-gray
> **Interaction note:** in Clip 91 David draws THIS sword from Goliath's scabbard — restate "the sword is nearly as tall as David and he lifts it with both hands."

---

## 4. David's Shepherd's Staff — `@david_staff`

**Description:** A plain worn wooden shepherd's staff, "his staff in his hand" (1 Sam 17:40). Goliath mocks it as "a stick." Roughly **David's own height** when stood on end. Thrown aside before the sling shot (Clip 88).

### Image-Generation Prompt
```
Product-style reference sheet of a shepherd's wooden staff on a solid mid-gray studio background,
even soft studio lighting, soft grounding shadow, subtle reflections.
Four views of the same object: [1] front, [2] back, [3] side, [4] three-quarter.
Object: a simple worn wooden shepherd's staff about as tall as a slim teenager, a natural slightly
crooked hardwood shaft with a gently hooked or knobbed top, smoothed and darkened by years of handling,
small nicks and cracks, a worn patch where a hand grips it. Plain, humble, undecorated.
Clean sheet layout, no text labels, no hands, no scenery.
```
### QA Checklist
- [ ] Reads **humble and worn** — not a wizard's staff or a polished stave
- [ ] Length reads as ≈ a slim youth's height (state "as tall as David" in the shot)
- [ ] Grain, hand-worn patch, nicks visible; grounding shadow
- [ ] Consistent shape across views
- [ ] Background solid mid-gray

---

## 5. David's Sling, Pouch & Five Stones — `@david_sling_kit`

**Description:** David's actual weapon and its kit, grouped because they're always used together: a simple leather shepherd's sling, a small leather stone pouch on his belt, and **five smooth river stones** (1 Sam 17:40). One stone is the slow-motion hero object in Clip 89.

### Image-Generation Prompt
```
Product-style reference sheet of a shepherd's sling with its pouch and five stones on a solid mid-gray
studio background, even soft studio lighting, soft grounding shadows, subtle reflections.
Four views of the same items, consistent across views: [1] the sling laid out flat showing the two cords
and the leather cradle, [2] the sling coiled ready, [3] the small leather drawstring stone pouch,
[4] three-quarter of the five smooth grey-brown river stones grouped together.
Objects: a simple two-cord leather shepherd's sling with a widened leather cradle in the middle, worn and
supple; a small brown leather drawstring pouch; five smooth rounded river stones, each roughly fist-sized,
grey and tan, water-worn. Humble, handmade, well-used.
Clean sheet layout, no text labels, no hands, no scenery.
```
### QA Checklist
- [ ] Sling reads as a real two-cord shepherd's sling (not a slingshot / catapult)
- [ ] Five **fist-sized** rounded stones, clearly smooth and river-worn
- [ ] Pouch and sling look hand-made leather, worn — match David's humble kit
- [ ] Each item has volume (shadow, reflection); stones not flat discs
- [ ] Background solid mid-gray
> **Hero-stone note:** for the slow-mo (Clip 89), the single flying stone is described in the shot from this sheet — a fist-sized smooth grey river stone.

---

## 6. King Saul's Royal Armor Set — `@saul_armor`

**Description:** Saul's personal battle gear — a blackened dark-steel plate breastplate, close helm, and sword — that Saul puts on David (Clips 79–80). It is **sized for a broad 185 cm king**, so on 158 cm David it visibly *swallows* him: helmet slips over his eyes, the hem hangs past his shins, the sword is nearly his own height. This is a distinct handled prop, separate from Saul's worn costume on his character sheet.

### Image-Generation Prompt
```
Product-style reference sheet of a king's royal battle armor set on a solid mid-gray studio background,
even soft studio lighting, soft grounding shadows, subtle metallic reflections.
Four views of the same set, consistent across views: [1] the full suit front, [2] the breastplate from the
back, [3] the close helm three-quarter, [4] the royal sword in its scabbard.
Objects: an ornate king's battle armor — a full suit of blackened dark-steel plate with an aged patina: a
rounded close helm with a horizontal visor slit and breathing slits and a polished gold band running down the
centre of the face; a rounded breastplate bearing a large ornate embossed gold roundel at its centre; layered
articulated pauldrons and arm plates; a fauld of dark-steel lames over a mail skirt reaching mid-thigh; and a
straight sword with a gold cruciform hilt in a dark scabbard. Regal, high-status metalwork, clearly sized for
a very tall broad-shouldered man.
Clean sheet layout, no text labels, no hands, no scenery.
```
### QA Checklist
- [ ] Reads **large and regal** — a tall king's gear, so it will visibly swallow a slight youth
- [ ] **Blackened dark-steel plate** with an aged patina; helm, breastplate and sword share the same metal and style
- [ ] Key **gold accents** present: the helm's face-band, the large embossed breastplate roundel, the sword's cruciform hilt
- [ ] Close helm (visor + breathing slits), layered pauldrons, and a fauld over a **mail skirt** all present (not flat)
- [ ] Higher-status than ordinary soldier armor (this is the comic contrast)
- [ ] Background solid mid-gray
> **Scale gag (Clip 80):** in the shot state "the armor is sized for King Saul (a tall broad man) and swallows David — helmet slips over his eyes, hem past his shins, sword nearly his own height."

---

## 7. Jesse's Provisions — `@jesse_provisions`

**Description:** The food David carries to his brothers (1 Sam 17:17–18): a basket/ephah of roasted grain, ten loaves of ancient bread, and ten cheeses for the unit commander. Shown at home and again to Eliab. Grouped as one sheet — they travel together.

### Image-Generation Prompt
```
Product-style reference sheet of ancient Hebrew provisions on a solid mid-gray studio background,
even soft studio lighting, soft grounding shadows, subtle reflections.
Four views/groupings, consistent across views: [1] a woven basket of roasted grain, [2] a stack of ten
round flat rustic bread loaves, [3] ten pale round cheeses stacked, [4] three-quarter of all grouped
together as a bundle.
Objects: a two-handled woven reed basket filled with roasted golden grain; ten round rustic flatbread
loaves, hand-sized, floury and slightly charred; ten pale wheel-shaped cheeses, hand-sized, rind visible.
Simple, rustic, period-accurate ancient Near-Eastern food. Everyday, humble.
Clean sheet layout, no text labels, no hands, no scenery.
```
### QA Checklist
- [ ] Loaves and cheeses read **hand-sized**; basket a two-handed carry
- [ ] Period-accurate rustic food (no modern packaging or modern bread shapes)
- [ ] Volume/texture on bread crust, cheese rind, woven basket
- [ ] Consistent look across the groupings
- [ ] Background solid mid-gray
> Light asset — if generation struggles, these can be described inline instead; they're not scale- or plot-critical.

---

## 8. Provisions Handcart — `@provisions_cart`

**Description:** The cart David loads the provisions into and rides/pushes away from home (Clip 27), then unloads at the camp (Clip 43). A simple period two-wheel wooden handcart. *(Assumption: a hand/push cart, not ox-drawn — the script only says "cart." Flag if you want it animal-drawn.)*

### Image-Generation Prompt
```
Product-style reference sheet of a simple ancient wooden handcart on a solid mid-gray studio background,
even soft studio lighting, soft grounding shadow, subtle reflections.
Four views of the same object: [1] side profile, [2] front, [3] rear, [4] three-quarter view.
Object: a small rustic two-wheeled wooden handcart with a plank bed and low side rails, two spoked wooden
wheels with iron rims, a pair of long pull handles at the front, rope lashing points. Weathered timber,
grey-brown, worn joints, a little dusty. Humble farm cart, big enough to carry a basket and food bundles.
Clean sheet layout, no text labels, no hands, no scenery.
```
### QA Checklist
- [ ] Reads as a **small humble handcart**, period-accurate (no modern wheels/metal frame)
- [ ] Wheels, bed, handles consistent across views; wheels actually round and load-bearing
- [ ] Wood grain + iron rim textures, grounding shadow (volume)
- [ ] Bed is plausibly sized for the provisions bundle
- [ ] Background solid mid-gray

---

## 9. ANN Camera Rig — `@ann_camera`

**Description:** Mr Tec Nical's modern video camera and zoom microphone — the ANN team's core filming kit, on screen throughout the incursion. Contemporary broadcast/prosumer look. (Headcam is worn kit on Tec's character sheet.)

### Image-Generation Prompt
```
Product-style reference sheet of a modern video camera and zoom microphone on a solid mid-gray studio
background, even soft studio lighting, soft grounding shadows, subtle reflections.
Four views, consistent across views: [1] the shoulder-mount video camera front, [2] its side profile,
[3] three-quarter with the flip-out screen, [4] the shotgun zoom microphone with its foam windscreen.
Objects: a matte-black modern shoulder-held broadcast video camera with a large lens, top handle, flip-out
side monitor, and small status buttons; a long shotgun zoom microphone with a grey foam windshield and a
short cable. Clean contemporary electronics, subtle brand-neutral (no readable logos or text).
Clean sheet layout, no text labels, no hands, no scenery.
```
### QA Checklist
- [ ] Reads as a **modern** camera + mic (deliberate anachronism against the ancient setting)
- [ ] **No readable brand text/logos** (keep it brand-neutral)
- [ ] Same unit across views; lens, screen, buttons consistent
- [ ] Matte + glass textures, reflections, grounding shadow (volume)
- [ ] Background solid mid-gray

---

## 10. ANN Drones (Pair) — `@ann_drones`

**Description:** The two drones Tec brings for aerial/close-action shots (Clip 33). Modern quadcopters, brand-neutral.

### Image-Generation Prompt
```
Product-style reference sheet of a modern camera drone on a solid mid-gray studio background,
even soft studio lighting, soft grounding shadows, subtle reflections.
Four views of the same drone: [1] top-down, [2] front, [3] side, [4] three-quarter in a landed pose.
Object: a compact matte-dark-grey quadcopter camera drone, four arms with propellers, a small gimbal
camera under the nose, landing feet, subtle status LEDs. Sleek modern consumer electronics, brand-neutral,
no readable text. Show one drone in detail (a matched pair is implied).
Clean sheet layout, no text labels, no hands, no scenery.
```
### QA Checklist
- [ ] Reads as a **modern quadcopter** (anachronism intact); brand-neutral, no text
- [ ] Four arms/props, gimbal camera, feet all consistent across views
- [ ] Plastic/matte + lens-glass textures, grounding shadow (volume)
- [ ] Top and three-quarter views make the geometry readable
- [ ] Background solid mid-gray

---

## 11. ANN Tablet — `@ann_tablet`

**Description:** The team's timeline-tracking tablet (Clarissa checks it in Clips 44, 57). Modern slate tablet, brand-neutral; on-screen UI kept abstract so no readable text is baked in.

### Image-Generation Prompt
```
Product-style reference sheet of a modern tablet computer on a solid mid-gray studio background,
even soft studio lighting, soft grounding shadow, subtle screen and body reflections.
Four views of the same object: [1] front with the screen on, [2] back, [3] side edge profile, [4] three-quarter.
Object: a slim modern glass-and-aluminium tablet, thin bezels, a front camera dot, a matte metal back with a
small camera bump; the screen shows an abstract glowing blue timeline/map interface with NO readable text.
Brand-neutral, no logos. Clean contemporary electronics.
Clean sheet layout, no text labels, no hands, no scenery.
```
### QA Checklist
- [ ] Reads as a **modern tablet**; brand-neutral, **no readable text** on screen or body
- [ ] Screen glow + glass reflection present (volume, not a flat rectangle)
- [ ] Front/back/edge consistent; thickness reads in the profile view
- [ ] Abstract blue UI only
- [ ] Background solid mid-gray

---

## 12. Chris's ANN Smartwatch — `@ann_watch` (with red arrow)

**Description:** Chris's smartwatch — the **two-hour incursion clock**, the story's ticking-clock device. It flashes when the portal is about to close (Clips 28, 94). Needs a **red arrow** on the flashing face so the video model knows the interaction point.

### Image-Generation Prompt
```
Product-style reference sheet of a modern smartwatch on a solid mid-gray studio background,
even soft studio lighting, soft grounding shadow, subtle glass reflections.
Four views of the same object: [1] face-on front with the screen lit, [2] side profile, [3] back with the
sensor, [4] three-quarter view with a bold red arrow pointing directly at the round watch face.
Object: a modern smartwatch with a rounded rectangular glass face on a dark silicone strap; the face shows
an abstract glowing blue countdown ring with NO readable text; matte dark body, small side crown button.
Brand-neutral, no logos.
Clean sheet layout, no text labels except the red arrow, no hands, no scenery.
```
### QA Checklist
- [ ] Reads as a **modern smartwatch**; brand-neutral, no readable text
- [ ] The **red arrow points unambiguously at the face** (the flashing countdown)
- [ ] Countdown ring reads as abstract/glowing, not literal numbers/text
- [ ] Face/strap/back consistent; glass reflection + volume present
- [ ] Background solid mid-gray

---

## 13. ANN Incursion Artifact — `@ann_artifact` (optional)

**Description:** The ancient artifact the research team unearthed that powers the incursions (Clips 16–17). Invented lore object — an ancient-looking device with a subtle sci-fi glow. Optional: generate if it gets meaningful screen time; otherwise describe inline.

### Image-Generation Prompt
```
Product-style reference sheet of a mysterious ancient artifact device on a solid mid-gray studio background,
even soft studio lighting, soft grounding shadow, subtle reflections and a faint internal glow.
Four views of the same object: [1] front, [2] back, [3] side, [4] three-quarter.
Object: a two-hand-sized ancient artifact — carved dark stone and tarnished bronze in an unfamiliar
geometric form, inset with seams of faintly glowing pale-blue light and worn unreadable glyphs. Looks
genuinely ancient yet subtly technological. Weathered, heavy, enigmatic.
Clean sheet layout, no text labels, no hands, no scenery.
```
### QA Checklist
- [ ] Reads as **ancient + subtly technological** (not obviously modern, not purely mystical)
- [ ] Faint blue glow comes from within seams — subtle, not a lamp
- [ ] Consistent form/glyphs across views; real volume (shadow, reflection)
- [ ] Glyphs unreadable (no real text)
- [ ] Background solid mid-gray

---

## Handoff & open questions

- **Register** each accepted sheet via the **asset-librarian** skill (create `assets/MANIFEST.md` for this project on first registration). Copy the **scale anchor** into the manifest's Scale field and any critical detail (brand-neutral, no-text, red-arrow) into Critical details.
- **Scale-critical props** — spear, tower shield, Goliath's sword, David's staff, Saul's armor — enforce the body-landmark phrasing in every Seedance prompt; never write centimetres.
- **A giant's prop is specced oversized for whoever handles it, not fitted to them.** Anchoring it to "a grown man" produces a prop that looks correct on the ordinary man and wrong on the giant — the `@goliath_shield` v1 mistake. Anchor to the giant's frame, then state how far past the handler's body it overhangs. The over-scaled prop then works as a **second yardstick** capping the giant's size on screen. Same logic applies in reverse to `@saul_armor` (built for the king, swallows David) — which is why that gag reads correctly.
- **Assumptions flagged (change if wrong):** (1) the provisions cart is a hand/push cart, not ox-drawn; (2) `@jesse_provisions` and `@ann_artifact` are light/optional — drop to inline if they don't earn screen time.
- **Next:** promote clips to Seedance prompts once character, location, and prop sheets are finalised and registered (see the [Scene & Clip Breakdown](script_&_scenes/Goliath_Complex_Scene_&_Clip_Breakdown.md)).

_Built to the same sheet standard as the Acts 23 prop assets._
