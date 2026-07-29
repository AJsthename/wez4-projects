# The Goliath Complex — Prop Assets: Descriptions & Generation Prompts

**Project:** "The Goliath Complex" (Gulayat) — ANN / David & Goliath, 1 Samuel 17
**Style:** Realism/Hyperrealism (not 3D animation)
**Sheet standard:** Solid mid-gray studio background · four-view product-style layout (front, back, side, 3/4) · soft studio lighting, grounding shadow, subtle reflections (physical *volume* is the acceptance bar) · scale stated as a **body landmark**, never in centimetres · no text labels, no hands, no scenery.
**Scale source:** [crs_table_Goliath_Complex.md](crs_table_Goliath_Complex.md) (the Scale Bible). Built with the **asset-prop** skill.

---

## What earns a prop sheet (triage)

Rule (from asset-prop / asset-planner): a prop earns a sheet when it is **held/used/interacted with**, **recurs**, or is **invented/specific**. Set dressing that just sits in a room belongs to the *location* plate. **Worn armor is costume** — it lives on the character sheet, not here — *unless* it is handled or worn by someone else on screen.

| # | Prop | Tag | Sheet? | Why | Scale anchor |
|---|------|-----|--------|-----|--------------|
| 1 | Goliath's spear | `@goliath_spear` | GENERATE | carried, hero weapon, scale gag | shaft **taller than Saul** |
| 2 | Goliath's tower shield | `@goliath_shield` | GENERATE | carried by shield-bearer "before him" | covers a grown man shin-to-shoulder |
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

**Description:** The large body-shield carried *before* Goliath by his shield-bearer. Tall enough to cover a grown man from shin to shoulder; bronze-faced over wood and hide, with a central boss. Not strapped to Goliath — the bearer holds it (Clips 3, 83, 88).

### Image-Generation Prompt
```
Product-style reference sheet of a large ancient tower shield on a solid mid-gray studio background,
even soft studio lighting, soft grounding shadow, subtle reflections on the bronze.
Four views of the same object: [1] front, [2] back, [3] side profile, [4] three-quarter view.
Object: a tall rectangular-oval body shield, tall enough to cover a grown man from shin to shoulder,
hammered bronze facing over a wooden and layered-hide core, a domed central bronze boss, riveted rim,
leather forearm strap and hand-grip visible on the back view. Battle-scarred, dented, weathered patina.
Clean sheet layout, no text labels, no hands, no scenery.
```
### QA Checklist
- [ ] Front shows the bronze face + boss; **back view shows the strap and grip** (how the bearer holds it)
- [ ] Reads **tall/heavy** — a body shield, not a small round buckler
- [ ] Curvature/thickness visible in the side view (volume, not a flat plate)
- [ ] Consistent dents/wear across views
- [ ] Background solid mid-gray

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

**Description:** Saul's personal battle gear — bronze/chain breastplate, royal helmet, and sword — that Saul puts on David (Clips 79–80). It is **sized for a broad 185 cm king**, so on 158 cm David it visibly *swallows* him: helmet slips over his eyes, the hem hangs past his shins, the sword is nearly his own height. This is a distinct handled prop, separate from Saul's worn costume on his character sheet.

### Image-Generation Prompt
```
Product-style reference sheet of a king's ancient royal armor set on a solid mid-gray studio background,
even soft studio lighting, soft grounding shadows, subtle metallic reflections.
Four views of the set, consistent across views: [1] the chain-and-scale breastplate front, [2] the
breastplate back, [3] the royal helmet three-quarter, [4] the royal sword in its scabbard.
Objects: a large ornate Israelite king's armor — a heavy bronze scale-and-chain breastplate with engraved
royal motifs and leather straps, a domed bronze helmet with a nasal guard and a modest crest, and a fine
straight sword with a gilded crossguard in a tooled leather scabbard. Regal, polished, clearly sized for
a very tall broad-shouldered man. Well-kept, high-status metalwork.
Clean sheet layout, no text labels, no hands, no scenery.
```
### QA Checklist
- [ ] Reads **large and regal** — a tall king's gear, so it will visibly swallow a slight youth
- [ ] Breastplate front/back consistent; helmet and sword match the set's metal and style
- [ ] Metal scale/chain texture, engraving, and volume all present (not flat)
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
- **Assumptions flagged (change if wrong):** (1) the provisions cart is a hand/push cart, not ox-drawn; (2) `@jesse_provisions` and `@ann_artifact` are light/optional — drop to inline if they don't earn screen time.
- **Next:** promote clips to Seedance prompts once character, location, and prop sheets are finalised and registered (see the [Scene & Clip Breakdown](script_&_scenes/Goliath_Complex_Scene_&_Clip_Breakdown.md)).

_Built to the same sheet standard as the Acts 23 prop assets._
