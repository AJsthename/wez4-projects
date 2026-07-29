# The Goliath Complex — Location Assets: Descriptions & Generation Prompts

**Project:** "The Goliath Complex" (Gulayat) — ANN / David & Goliath, 1 Samuel 17
**Style:** Realism/Hyperrealism (not 3D animation)
**Plate standard:** Empty of people · **3/4 camera angle** for interiors (two walls + depth) · spatial *layout*, not an inventory · light source stated · every object physically grounded (a single floating object = discard the batch).
**Built with the asset-location skill.** Scale/continuity source: [Scene & Clip Breakdown](script_&_scenes/Goliath_Complex_Scene_&_Clip_Breakdown.md).

**Three views per location, one anchor.** Every location is oriented around a single fixed **Anchor** — an unmistakable landmark (a throne, a stream, a doorway, a drop-off) that tells you which way you're facing. Each generated plate ships up to three views, all built around that anchor:
- **A. Three-Quarter — Front View** — eye-level, diagonal, facing the anchor from the front (the original primary reference; two walls/slopes + depth).
- **B. Three-Quarter — Back View** — the **180° reverse of A** (the shot/reverse-shot plate). Same location, same anchor, camera on the opposite side. **Left/right of every fixed object swaps, and the light source keeps its world position — so a sun that is high-left in A reads high-right in B.** Not every location has a meaningful reverse (the master panorama does not — see §1).
- **C. CCTV Top-Down View** — an overhead **top-down view**: the camera looks straight/steeply *down* on the space from directly above, so you see the tops of everything (the crowns of heads, if anyone were there) and the *full* floor/ground layout reads as a map. **"CCTV" here names a camera *position*, not a prop** — it must **never** put a surveillance camera, mast, pole, ceiling mount, or lens *in the frame*; there is no camera visible in the shot, only the view from above. Clean photorealistic plate — no timestamp, no grain/monochrome, no on-screen text.

The anchor is restated in every view, carried into the Seedance shot prompts (rulebook §6 / tip #14, anchor objects), and recorded in the manifest's Critical details so reverse cuts never flip the geometry. All views of a location share the **same geography, layout, and world light** (only the *screen-direction* of that light flips between front and back, as noted).

**Shared QA for the B / C plates (applies to every Back-View and CCTV plate below):**
- [ ] **Back View** — same anchor and same objects as the Front View; camera clearly 180° opposite; left/right of fixed objects swapped; light source in its correct world position (screen-side flipped vs A); depth still reads (two walls/slopes)
- [ ] **CCTV (top-down)** — a true overhead top-down view (tops of objects visible, layout reads as a map); **no camera, mast, pole, mount or lens rendered anywhere in frame**; same geography and world light as A; clean plate (no timestamp/text/grain); empty of people; everything grounded/cabled/supported

---

## First decision: which locations earn a plate (skip test)

Generate a plate when the location **recurs**, has a **layout the action depends on**, is **cluttered/detailed**, or is **invented**. Otherwise describe it directly in the Seedance prompt.

| # | Location | Tag | Decision | Why |
|---|----------|-----|----------|-----|
| 1 | Valley of Elah — master panorama | `@valley_elah` | GENERATE | signature environment; two mountains + valley layout; recurs across the whole film |
| 2 | The valley floor / the plain (battlefield) | `@elah_plain` | GENERATE | the confrontation + battle happen here; ground continuity (Clips 3–6, 83–91) |
| 3 | Israel army camp — front & slope | `@israel_camp` | GENERATE | recurs heavily (ranks, front line, Eliab, funny soldiers); layout matters |
| 4 | King Saul's command tent (interior) | `@saul_tent` | GENERATE | recurs most of the film; interior layout; the throne/map staging |
| 5 | ANN observation peak | `@ann_peak` | GENERATE (light) | ANN watch-point; must show the valley below for continuity (Clips 11–14, 44) |
| 6 | Jesse's homestead (hillside + yard) | `@jesse_house` | GENERATE | specific yard layout (provisions table), sheep pasture; Clips 22–27 |
| 7 | ANN lab + circular portal stage | `@ann_lab` | GENERATE | invented sci-fi interior; the portal stage is a key recurring set piece |

**SKIP — describe directly in the Seedance prompt (no plate):**

| Location | Where | Why skip |
|----------|-------|----------|
| ANN HQ corridor | Clip 28 | single shot, generic modern corridor |
| Antarctic dig site / buried structure | Clip 15 | single flashback beat, generic |
| Tomb interior (door + cascading sand) | Clip 16 | single flashback beat |
| Stream / brook (5 stones) | Clip 82 | brief; a shallow rocky brook at the valley edge — fold into `@elah_plain`/`@valley_elah` |
| Jericho walls falling | Clip 17 | VFX montage moment |
| Red Sea splitting | Clip 20 | VFX montage moment |
| Road from Jesse's house | Clip 27 | brief transition; generic |

> **Note on the portal:** the swirling portal itself is a **VFX**, not a location. The **circular stage + four laser devices** it opens above is a fixed feature of the ANN lab, so it lives inside `@ann_lab` (below), not as a separate asset.

---

## 1. Valley of Elah — Master Panorama — `@valley_elah`

**Description:** The establishing environment (1 Sam 17:2–3): two facing mountains with a valley between. Israel's army encamped on one slope (tents on a lower peak); the Philistine army covering the opposite mountain and spilling onto the plain. Some mountains barren, some grassy, some treed (the script even jokes about it). Wide exterior; the camera soars over it in Clip 1 and returns throughout.

**Anchor:** the two-mountain axis — Israel's **green, treed slope with the tent camp on the LEFT** and the **Philistine barren rocky slope on the RIGHT**, the thin stream running the valley floor between them. This left = Israel / right = Philistine convention is the master orientation every other location's plates obey.

### Image-Generation Prompt — A. Three-Quarter — Front View
```
Sweeping aerial establishing plate of an ancient Near-Eastern valley, empty of people, bright midday
haze, photorealistic.
Layout: two large facing mountains running left and right with a broad dry valley floor between them;
the left mountain green and partly treed with an army encampment of tents clustered on a lower peak;
the right mountain barren and rocky, its slope and the plain below it able to hold a second great army;
a thin rocky stream winds along the valley floor. Distant mountain ranges fade into heat haze on the horizon.
Warm midday sun from high left, hard shadows in the ravines, dust haze at 20% in the far distance.
Arid earth tones — ochre, dust-green scrub, pale rock. Every landform geologically plausible and grounded.
```
### Image-Generation Prompt — B. Three-Quarter — Back View — N/A
> **No back view for the master panorama.** This is an omniscient aerial that already sees the whole basin; a 180° reverse would only flip Israel and Philistine to the wrong sides and break the left/right convention every other location inherits. Keep one canonical orientation — overhead coverage is the top-down (CCTV) plate below.

### Image-Generation Prompt — C. CCTV Top-Down View
```
High overhead top-down view of an ancient Near-Eastern valley, empty of people, bright midday haze,
photorealistic clean plate, no on-screen text.
Vantage: looking straight down on the whole basin from directly above, so the entire two-mountain layout
reads like a map — ridgelines, tent tops and terrain all seen from overhead. No camera, mast, or equipment
anywhere in frame.
Layout: two large facing mountains running left and right with a broad dry valley floor between them; the
left mountain green and partly treed with an army encampment of tents clustered on a lower peak; the right
mountain barren and rocky, its slope and the plain below able to hold a second great army; a thin rocky
stream winding along the valley floor; distant mountain ranges fading into heat haze at the frame edges.
Warm midday sun from high left, hard shadows in the ravines, dust haze at 20% in the far distance.
Arid earth tones — ochre, dust-green scrub, pale rock. Every landform geologically plausible and grounded.
```
### QA Checklist
- [ ] **Two facing mountains + a valley floor between** clearly readable (the core geography)
- [ ] One slope greener/treed with a tent camp; the opposite barren and rocky (the two-army setup)
- [ ] A stream/brook visible on the valley floor (for the stone-gathering beat)
- [ ] Depth: foreground ridge → valley → far mountain → hazy horizon
- [ ] No people, no armies rendered as figures (they're added per shot); no floating rocks/impossible geology
- [ ] Consistent single sun direction

---

## 2. The Valley Floor / The Plain — `@elah_plain`

**Description:** Ground-level plate of the battlefield floor where Goliath issues his challenge and the duel happens (Clips 3–6, 83–91). Dusty open plain between the two slopes, shimmering heat, the stream bank at one edge. This is the stage for the scale-critical two-shots — keep it open and uncluttered so David and Goliath read clearly.

**Anchor:** the shallow **rocky stream with its pebbled bank** at one edge, read against the **tented Israelite slope** on one side and the **barren Philistine slope** on the other — the two slopes label which way you face.

### Image-Generation Prompt — A. Three-Quarter — Front View
```
Ground-level plate of a dry open valley battlefield floor, empty of people, shimmering midday heat,
photorealistic.
Layout: a wide flat expanse of cracked dusty earth and scattered stones between two rising rocky slopes
that frame it left and right; a shallow rocky stream with a pebbled bank along the near-left edge; the
Israelite tented slope rising in the background on one side, the barren Philistine slope on the other.
Open central ground with nothing in the middle — room for figures to face off.
Harsh midday sun from high, hard short shadows, heat-shimmer haze at 30% low to the ground, fine dust.
Arid ochre and grey palette. Ground physically consistent, stones grounded, no floating debris.
```
### Image-Generation Prompt — B. Three-Quarter — Back View
```
Ground-level plate of a dry open valley battlefield floor, empty of people, shimmering midday heat,
photorealistic — the 180° reverse of the front view, camera on the opposite side of the open ground looking
back across it, three-quarter angle.
Layout: the same wide flat expanse of cracked dusty earth and scattered stones, open and clear in the centre
with nothing in the middle; the shallow rocky stream with its pebbled bank now running along the far-right
edge (mirrored from the front view); the barren Philistine slope now rising on the left and the tented
Israelite slope on the right, swapped to the reverse side; the opposite framing slope closing the background.
Harsh midday sun still near-vertical from high, hard short shadows, heat-shimmer haze at 30% low to the
ground, fine dust. Arid ochre and grey palette. Ground physically consistent, stones grounded, no floating debris.
```
### Image-Generation Prompt — C. CCTV Top-Down View
```
High overhead top-down view of a dry open valley battlefield floor, empty of people, shimmering midday heat,
photorealistic clean plate, no on-screen text.
Vantage: looking straight down on the open ground from directly above, the whole clearing readable like a
map — cracked earth, scattered stones and the stream all seen from overhead. No camera, pole, or equipment
anywhere in frame.
Layout: a wide flat expanse of cracked dusty earth and scattered stones between two rising rocky slopes that
frame it left and right; a shallow rocky stream with a pebbled bank along one edge; the Israelite tented
slope rising on one side, the barren Philistine slope on the other; open central ground with nothing in the
middle — room for figures to face off.
Harsh midday sun from high, hard short shadows, heat-shimmer haze at 30% low to the ground, fine dust.
Arid ochre and grey palette. Ground physically consistent, stones grounded, no floating debris.
```
### QA Checklist
- [ ] **Open, uncluttered central ground** (so a two-shot of David vs Goliath stays clear)
- [ ] Both framing slopes visible in the background (spatial link to `@valley_elah`)
- [ ] Pebbled stream bank present at one edge (Clip 82 stone-gathering)
- [ ] Heat-shimmer + dust sell the midday desert; single sun direction
- [ ] No people; ground and stones grounded, nothing floating

---

## 3. Israel Army Camp — Front & Slope — `@israel_camp`

**Description:** The Israelite encampment on its mountain slope — rows of tents, the ranked soldiers' front line looking down into the valley, and the rear ranks where the funny soldiers skulk. Recurs across many clips (fear reactions, David questioning soldiers, Eliab's confrontation, the ANN interview). Layout matters: a front edge overlooking the valley, tents behind, room for crowds.

**Anchor:** the **cleared front edge / battle-line lip** where the slope drops toward the valley — the valley lies on the down-slope side, the tents and the crowning ridge rise on the up-slope side.

### Image-Generation Prompt — A. Three-Quarter — Front View
```
Exterior plate of an ancient Israelite army encampment on a mountain slope, empty of people, midday,
photorealistic, camera at a three-quarter angle showing the slope's depth down toward the valley.
Layout: rows of earth-tone goat-hair military tents pitched on terraced ground in the mid and background;
a cleared front edge in the foreground where a battle line would form, overlooking the dry valley below;
banners on simple poles, stacked spears and shields on wooden racks beside the tents, cook-fire rings,
a rocky path winding up between the tents. The opposite barren Philistine mountain visible far across the valley.
Warm midday sun from the left, soft dust haze, hard shadows under the tents. Arid ochre/brown palette.
Every tent staked and grounded, racks and poles physically supported.
```
### Image-Generation Prompt — B. Three-Quarter — Back View
```
Exterior plate of an ancient Israelite army encampment on a mountain slope, empty of people, midday,
photorealistic — the 180° reverse of the front view, camera down at the cleared front edge looking back up
the slope into the camp, three-quarter angle keeping the slope's depth.
Layout: the cleared front edge / battle line in the foreground with the dry valley dropping away behind the
camera; rows of earth-tone goat-hair military tents rising up the terraced slope ahead; banners on simple
poles, stacked spears and shields on wooden racks beside the tents, cook-fire rings, a rocky path winding up
between the tents toward the crowning ridge at the top of the slope.
Warm midday sun now from the right (camera turned 180° from the front view), soft dust haze, hard shadows
under the tents. Arid ochre/brown palette. Every tent staked and grounded, racks and poles physically supported.
```
### Image-Generation Prompt — C. CCTV Top-Down View
```
High overhead top-down view of an ancient Israelite army encampment on a mountain slope, empty of people,
midday, photorealistic clean plate, no on-screen text.
Vantage: looking straight down on the camp from directly above, so the rows of tents and the cleared front
edge read like a map — tent tops, weapon racks and paths all seen from overhead. No camera, pole, or
equipment anywhere in frame.
Layout: rows of earth-tone goat-hair military tents pitched on terraced ground; a cleared front edge
overlooking the dry valley below where a battle line would form; banners on simple poles, stacked spears and
shields on wooden racks beside the tents, cook-fire rings, a rocky path winding up between the tents; the
opposite barren Philistine mountain across the valley at the frame edge.
Warm midday sun from the left, soft dust haze, hard shadows under the tents. Arid ochre/brown palette.
Every tent staked and grounded, racks and poles physically supported.
```
### QA Checklist
- [ ] **Front edge overlooking the valley** + tents behind (the front-line vs rear-ranks geography)
- [ ] 3/4 angle gives real slope depth — not a flat wall of tents
- [ ] Weapon racks, banners, fire rings grounded and plausibly placed (no floating gear)
- [ ] Opposite mountain / valley visible for continuity with `@valley_elah`
- [ ] No people; consistent single sun direction

---

## 4. King Saul's Command Tent (interior) — `@saul_tent`

**Description:** The large royal command tent where Saul holds court with his counsellors and generals, and where David meets him (Clips 7–9, 37–49, 64, 74–81). Interior — needs the 3/4 angle. A raised seat/throne area, a map or battle table, an armor stand (Saul's armor hangs here before it's brought to David), an open flap looking down toward the valley.

**Anchor:** the **raised carpeted dais with the carved wooden throne-seat** (against the far-left wall in the front view) — the fixed focal point; the **entrance flap in the far wall** is the fixed daylight source that the light logic keys off.

### Image-Generation Prompt — A. Three-Quarter — Front View
```
Interior plate of a large ancient royal military command tent, empty of people, camera at a three-quarter
angle into the tent showing two canvas walls and the peaked canvas roof over wooden ridge beams, eye-level,
photorealistic.
Layout: against the far-left wall a raised stepped dais carpeted with layered rugs holding a carved dark-wood
throne with a deep-red seat, backed by a deep-red gold-embroidered wall hanging and tied-back red curtains; in
the centre of the far wall a partly open entrance flap with tied-back canvas curtains, letting in bright
daylight and a glimpse of green valley hills beyond; right of centre near the entrance a wooden armor stand
displaying the king's armor — a dark steel breastplate with a large round embossed gold medallion, a closed
helmet topped with a golden royal crown, a tall spear held upright at its side and a sheathed sword at the hip;
against the right side a sturdy wooden map/campaign table with a spread hide map and coloured cone markers; at
the centre of the tent a large patterned carpet spread over the packed earth — a deep-red royal rug matching
the dais rugs — covering the middle of the floor; further woven rugs layered over a packed-earth and pale-stone
flagstone floor around the edges; tall wrought-iron cage lantern stands at the left and mid-floor and a warm
brass lantern on a stand at the right.
Bright daylight from the open entrance flap (far wall) plus warm lamp glow from the lanterns; goat-hair canvas
walls and roof, colour balanced 60-30-10 — 60% dominant sandy goat-hair canvas neutral, 30% deep-red royal
textiles (dais rugs, wall hanging and curtains), 10% brass-and-gold accent (the lantern flames, the armor's
round medallion and the king's crown). Every object grounded — throne on the dais, table legs and armor stand
on the floor, lanterns on their stands, the central carpet lying flat on the floor.
```
### Image-Generation Prompt — B. Three-Quarter — Back View
```
Interior plate of a large ancient royal military command tent, empty of people, three-quarter angle,
eye-level, photorealistic — the 180° reverse of the front view, camera near the entrance (far) wall looking
back across the tent toward its rear, showing two canvas walls and the peaked canvas roof over wooden ridge beams.
Layout: the raised stepped dais with its carved dark-wood throne, deep-red gold-embroidered wall hanging and
tied-back red curtains now in the near foreground on the right (mirrored from the front view); the king's armor
stand — a dark steel breastplate with a large round embossed gold medallion, a closed helmet topped with a
golden royal crown, a tall spear upright at its side and a sheathed sword at the hip — now standing left of
centre; the sturdy wooden map/campaign table with its spread hide map and coloured cone markers now against the
left side; at the centre of the tent a large patterned carpet spread over the packed earth — a deep-red royal
rug matching the dais rugs — covering the middle of the floor; further woven rugs layered over a packed-earth
and pale-stone flagstone floor around the edges; the rear canvas wall closing the space ahead;
tall wrought-iron cage lantern stands and a warm brass lantern on a stand around the space.
Daylight spills from the open entrance flap behind the camera as soft backlight, warm lamp glow filling the
rear of the tent; goat-hair canvas walls and roof, colour balanced 60-30-10 — 60% dominant sandy goat-hair
canvas neutral, 30% deep-red royal textiles (dais rugs, the central carpet, wall hanging and curtains), 10% brass-and-gold accent
(the lantern flames, the armor's round medallion and the king's crown). Every object grounded — throne on the
dais, table legs and armor stand on the floor, lanterns on their stands, the central carpet lying flat on the floor.
```
### Image-Generation Prompt — C. CCTV Top-Down View
```
Interior high overhead top-down view of a large ancient royal military command tent, empty of people,
photorealistic clean plate, no on-screen text.
Vantage: looking straight down into the tent from directly above, the canvas roof omitted so the full floor
layout reads like a map — the throne, dais, table, armor stand and the large central carpet all seen from
overhead. No camera or equipment anywhere in frame.
Layout: against the far-left wall a raised stepped dais carpeted with layered rugs holding a carved dark-wood
throne backed by a deep-red gold-embroidered wall hanging; in the centre of the far wall a partly open entrance
flap; right of centre near the entrance a wooden armor stand displaying the king's armor — a dark steel
breastplate with a round embossed gold medallion, a helmet topped with a golden royal crown, an upright spear
and a sheathed sword; against the right side a sturdy wooden map/campaign table with a spread hide map and
coloured cone markers; at the centre of the tent a large patterned carpet spread over the packed earth — a
deep-red royal rug matching the dais rugs — covering the middle of the floor; further woven rugs layered over a
packed-earth and pale-stone flagstone floor around the edges; tall wrought-iron cage lantern stands and a warm
brass lantern on a stand.
Warm daylight from the open flap plus soft warm lamp glow; goat-hair canvas walls, colour balanced 60-30-10 —
60% dominant sandy goat-hair canvas neutral, 30% deep-red royal textiles (dais rugs, the central carpet, wall hanging and curtains),
10% brass-and-gold accent (the lantern flames, the armor's round medallion and the king's crown). Every object
grounded — table legs and armor stand on the floor, lamps on stands, the central carpet lying flat on the floor.
```
### QA Checklist
- [ ] **3/4 angle** — two canvas walls + real depth (not a flat tent wall)
- [ ] **Table to the right side**, **armor stand right of centre near the entrance** — furniture kept off the middle of the floor
- [ ] **A large deep-red patterned carpet covers the centre of the floor** (matching the dais rugs) — the bare earth in the middle is covered, not left empty
- [ ] The **armor stand shows the king's crowned armor** — dark steel breastplate with a **large round gold medallion**, closed helmet topped with a **golden crown**, upright spear, sheathed sword (sets up the Clip 79–80 gag)
- [ ] Scenery matches the loved take: **packed-earth/pale-stone flagstone floor** under layered rugs, **tall wrought-iron cage lanterns** + a **warm brass lantern** at the right, deep-red gold-embroidered dais hanging (not a plank floor)
- [ ] Open flap shows a sliver of daylight/valley (spatial logic to the outside)
- [ ] Lighting: daylight from the flap + lamp glow agree in direction
- [ ] No people; nothing floating; canvas sagging/poles physically plausible

---

## 5. ANN Observation Peak — `@ann_peak`

**Description:** The small rocky peak on a nearby mountain where the ANN team stands to watch and film the confrontation (Clips 11–14, 44). Must show the **valley below** in the background for continuity — the whole point is they overlook the battlefield. Light plate; a rocky outcrop vantage.

**Anchor:** the **drop-off edge** — the direction the valley falls away. The outcrop sits on the mountain side; the wide Valley of Elah opens on the down-slope side. Which side the drop is on is what orients every shot here.

### Image-Generation Prompt — A. Three-Quarter — Front View
```
Exterior plate of a small rocky mountain peak vantage point, empty of people, midday, photorealistic,
camera at a three-quarter angle so the outcrop foreground and the valley far below both read.
Layout: a flat rocky outcrop with scattered boulders and dry scrub in the foreground (a natural place to
stand and film), the ground dropping away steeply behind it into the wide Valley of Elah far below, with the
two opposing army mountains visible across the valley in the hazy distance.
Bright midday sun from high left, hard shadows on the rocks, dust haze at 25% over the distant valley.
Arid ochre and grey stone, sparse dry brush. Rocks and scrub physically grounded, geology plausible.
```
### Image-Generation Prompt — B. Three-Quarter — Back View
```
Exterior plate of a small rocky mountain peak vantage point, empty of people, midday, photorealistic — the
180° reverse of the front view, camera out on the valley-facing side looking back at the outcrop, three-quarter
angle keeping foreground rock and background slope.
Layout: the flat rocky outcrop with its scattered boulders and dry scrub now in the mid-ground, the mountain
slope rising steeply behind it to fill the background, and the wide Valley of Elah now falling away behind
the camera (out of frame); scattered boulders and dry brush in the foreground.
Bright midday sun now from high right (camera turned 180° from the front view), hard shadows on the rocks,
dust haze at 25% in the air. Arid ochre and grey stone, sparse dry brush. Rocks and scrub physically grounded,
geology plausible.
```
### Image-Generation Prompt — C. CCTV Top-Down View
```
High overhead top-down view of a small rocky mountain peak vantage point, empty of people, midday,
photorealistic clean plate, no on-screen text.
Vantage: looking straight down on the outcrop from directly above, so the flat standing area and the edge
where the ground drops into the valley both read from overhead — boulder tops and scrub all seen from above.
No camera, pole, or equipment anywhere in frame.
Layout: a flat rocky outcrop with scattered boulders and dry scrub (a natural place to stand and film), the
ground dropping away steeply on one side into the wide Valley of Elah far below, with the two opposing army
mountains across the valley at the hazy frame edge.
Bright midday sun from high left, hard shadows on the rocks, dust haze at 25% over the distant valley.
Arid ochre and grey stone, sparse dry brush. Rocks and scrub physically grounded, geology plausible.
```
### QA Checklist
- [ ] Foreground **standing outcrop** + the **valley visible far below** (the watch-point logic)
- [ ] Reads as higher than, and looking onto, the `@valley_elah` geography (continuity)
- [ ] Depth: boulders foreground → drop-off → hazy valley
- [ ] No people; boulders grounded, no floating rocks
- [ ] Single consistent sun direction

---

## 6. Jesse's Homestead — Hillside & Yard — `@jesse_house`

**Description:** David's family home near Bethlehem (Clips 22–27): a large house on a gentle green hillside, sheep pastures on the slope, and a yard with the table where Jesse has packed the provisions. Layout matters — David climbs the slope to Jesse waiting by the laden table outside.

**Anchor:** the **house** — its flat roof and **arched doorway** with the sturdy **wooden provisions table against the yard-side wall**. The house sits up-slope; the pasture and distant hills fall away down-slope.

### Image-Generation Prompt — A. Three-Quarter — Front View
```
Exterior plate of an ancient Near-Eastern hillside homestead, empty of people, warm morning light,
photorealistic, camera at a three-quarter angle showing the house, the yard, and the slope's depth.
Layout: a large sand-coloured stone-and-mud-brick house with a flat roof and an arched doorway set on a
gentle green hillside; an open packed-earth yard in front with a sturdy wooden table against the house wall;
low stone walls and a animal pen to one side; a grassy pasture slope in the foreground and mid-ground dotted
with sparse olive trees, descending toward distant hills.
Soft warm early-morning sun from low right, long gentle shadows, clear sky. Colour balanced 60-30-10 — 60% dominant green pasture and warm sand-stone, 30% ochre packed-earth and roof/wall tones, 10% terracotta accent (a jar or a folded textile at the table).
Every structure grounded, walls and table physically supported, roof beams sensible.
```
### Image-Generation Prompt — B. Three-Quarter — Back View
```
Exterior plate of an ancient Near-Eastern hillside homestead, empty of people, warm morning light,
photorealistic — the 180° reverse of the front view, camera up-slope beside the house looking back down the
hillside, three-quarter angle showing the house and the slope falling away.
Layout: the sand-coloured stone-and-mud-brick house with its flat roof and arched doorway now in the near
foreground (seen from its yard side, the sturdy wooden table still against the wall); the open packed-earth
yard with low stone walls and an animal pen beside it; the grassy pasture slope with sparse olive trees now
descending away from the house into the distance, toward far hills and the valley beyond.
Soft warm early-morning sun now from low left (camera turned 180° from the front view), long gentle shadows,
clear sky. Colour balanced 60-30-10 — 60% dominant green pasture and warm sand-stone, 30% ochre packed-earth and roof/wall tones, 10% terracotta accent (a jar or a folded textile at the table). Every structure grounded, walls and table physically supported,
roof beams sensible.
```
### Image-Generation Prompt — C. CCTV Top-Down View
```
High overhead top-down view of an ancient Near-Eastern hillside homestead, empty of people, warm morning
light, photorealistic clean plate, no on-screen text.
Vantage: looking straight down on the house, yard and slope from directly above, so the whole layout reads
like a map — the flat roof, the yard and the table all seen from overhead. No camera, pole, or equipment
anywhere in frame.
Layout: a large sand-coloured stone-and-mud-brick house with a flat roof and an arched doorway on a gentle
green hillside; an open packed-earth yard in front with a sturdy wooden table against the house wall; low
stone walls and an animal pen to one side; a grassy pasture slope dotted with sparse olive trees, descending
toward distant hills.
Soft warm early-morning sun from low right, long gentle shadows, clear sky. Colour balanced 60-30-10 — 60% dominant green pasture and warm sand-stone, 30% ochre packed-earth and roof/wall tones, 10% terracotta accent (a jar or a folded textile at the table).
Every structure grounded, walls and table physically supported, roof beams sensible.
```
### QA Checklist
- [ ] House + **yard with a table against the wall** + a **pasture slope** below (the Clip 22–26 staging)
- [ ] 3/4 angle gives the hillside real depth (David climbs *up* to the house)
- [ ] Period-accurate stone/mud-brick build, flat roof, arched door — no modern materials
- [ ] Morning light direction consistent; pastoral green vs the arid valley elsewhere
- [ ] No people, no sheep-as-characters (sheep added per shot); nothing floating

---

## 7. ANN Lab + Circular Portal Stage — `@ann_lab`

**Description:** The invented modern ANN laboratory (Clips 17 flashback, 29–35): a large high-tech equipment-filled space with, at its centre, a **circular stage ringed by four laser-like emitter devices** — the rig that opens the incursion portal. Deliberate modern/sci-fi contrast with the ancient world. Interior — 3/4 angle.

**Anchor:** the **central circular raised stage ringed by the four inward-aimed laser-emitter devices** (the portal rig) — the fixed focal set piece the whole room is built around; the **reinforced doorway** in the far wall fixes the room's front/back.

### Image-Generation Prompt — A. Three-Quarter — Front View
```
Interior plate of a large modern high-tech research laboratory, empty of people, camera at a three-quarter
angle showing two walls and the depth of the room, eye-level, photorealistic.
Layout: at the centre, a low circular raised metal stage/platform ringed by four tall angular laser-emitter
devices aimed inward toward the stage's centre; banks of computer workstations and glowing monitor screens
along the left wall; scientific scanning instruments, cabling runs, and equipment racks along the right wall;
a polished concrete floor with inset cable channels; a reinforced doorway in the far wall.
Cool blue-white ceiling and screen lighting, subtle glow from the emitter devices, soft reflections on the
floor. Clean industrial sci-fi, colour balanced 60-30-10 — 60% dominant brushed-metal and matte-grey panels, 30%
cool blue screen-and-emitter glow, 10% warm amber accent (status lights and warning strips); brand-neutral
screens with abstract UI (no
readable text). Every device cabled and grounded, monitors on mounts, nothing floating or unpowered.
```
### Image-Generation Prompt — B. Three-Quarter — Back View
```
Interior plate of a large modern high-tech research laboratory, empty of people, three-quarter angle,
eye-level, photorealistic — the 180° reverse of the front view, camera from the far (doorway) side looking
back across the room, showing two walls and the depth.
Layout: the low circular raised metal stage ringed by four tall angular laser-emitter devices aimed inward
still at the centre; the banks of computer workstations and glowing monitor screens now along the right wall
(mirrored from the front view); the scientific scanning instruments, cabling runs and equipment racks now
along the left wall; a polished concrete floor with inset cable channels; the reinforced doorway now behind
the camera, the opposite wall closing the space ahead.
Cool blue-white ceiling and screen lighting, subtle glow from the emitter devices, soft reflections on the
floor. Clean industrial sci-fi, colour balanced 60-30-10 — 60% dominant brushed-metal and matte-grey panels, 30%
cool blue screen-and-emitter glow, 10% warm amber accent (status lights and warning strips); brand-neutral
screens with abstract UI and no
readable text. Every device cabled and grounded, monitors on mounts, nothing floating or unpowered.
```
### Image-Generation Prompt — C. CCTV Top-Down View
```
Interior high overhead top-down view of a large modern high-tech research laboratory, empty of people,
photorealistic clean plate, no on-screen text.
Vantage: looking straight down on the room from directly above, the ceiling omitted so the full floor layout
reads like a map — the tops of the circular stage, the four emitters and the workstations all seen from
overhead. No camera or equipment mount anywhere in frame.
Layout: at the centre, a low circular raised metal stage/platform ringed by four tall angular laser-emitter
devices aimed inward toward the stage's centre; banks of computer workstations and glowing monitor screens
along the left wall; scientific scanning instruments, cabling runs, and equipment racks along the right wall;
a polished concrete floor with inset cable channels; a reinforced doorway in the far wall.
Cool blue-white overhead and screen lighting, subtle glow from the emitter devices, soft reflections on the
floor. Clean industrial sci-fi, colour balanced 60-30-10 — 60% dominant brushed-metal and matte-grey panels, 30%
cool blue screen-and-emitter glow, 10% warm amber accent (status lights and warning strips); brand-neutral
screens with abstract UI and no
readable text. Every device cabled and grounded, monitors on mounts, nothing floating or unpowered.
```
### QA Checklist
- [ ] **Central circular stage + four inward-aimed emitter devices** clearly the focal set piece
- [ ] 3/4 angle — two walls + depth; workstations one wall, instruments the other
- [ ] Reads as **modern/sci-fi** (the anachronism); brand-neutral, **no readable text** on screens
- [ ] Everything cabled/mounted/grounded — no floating monitors, no device without a base or cable
- [ ] Cool consistent lighting; reflections agree with sources
- [ ] No people

---

## Handoff & open questions

- **Register** each accepted plate via the **asset-librarian** skill (create `assets/MANIFEST.md` on first registration). Note continuity-critical layout facts in Critical details (e.g. "armor stand on the right wall" for `@saul_tent`, "valley visible below" for `@ann_peak`).
- **Continuity anchors:** `@valley_elah`, `@elah_plain`, `@israel_camp`, and `@ann_peak` must all agree on the same two-mountain geography and sun direction — generate the master `@valley_elah` first and match the others to it.
- **Assumptions flagged (change if wrong):** (1) `@ann_peak` is a light plate — could be folded into a per-shot description if you'd rather not lock it; (2) the dig site is treated as SKIP despite the script/production note conflict (script says "desert"/sand, production list says "Antarctica") — **flag which you want** if that flashback grows beyond one shot; (3) the stream is folded into the valley plates rather than its own asset.
- **Next:** promote clips to Seedance prompts once character, location, and prop sheets are finalised and registered (see the [Scene & Clip Breakdown](script_&_scenes/Goliath_Complex_Scene_&_Clip_Breakdown.md)).

_Built to the same plate standard as the Acts 23 location assets._
