# The Goliath Complex — Seedance 2.0 Prompts (per clip)

**Source script:** [script_&_scenes/Goliath_Complex_Script.md](script_&_scenes/Goliath_Complex_Script.md)
**Clip plan:** [script_&_scenes/Goliath_Complex_Scene_&_Clip_Breakdown.md](script_&_scenes/Goliath_Complex_Scene_&_Clip_Breakdown.md) — 95 clips total.
**Asset registry:** [assets/MANIFEST.md](assets/MANIFEST.md) · Locations: [Goliath Complex - Location Assets_ Descriptions & Prompts.md](Goliath%20Complex%20-%20Location%20Assets_%20Descriptions%20&%20Prompts.md)

Built with the **seedance-clean** skill. This file grows one scene-block at a time. **Currently written: Scenes 1–3 (Clips 1–10).**

## Generation Settings & Credit Policy

- **Resolution lives in the platform UI, never in the prompt.** These prompts are resolution-agnostic (no OUTPUT SETTINGS block) so one prompt serves every quality tier unchanged.
- **Test pass 720p → final pass re-render the accepted prompt at 1080p/4K.** Same prompt, same uploads, same order — only the resolution setting changes.
- **Reference by `@tag`.** Every `@tag` is a **`final`** asset in the registry. Attach the matching reference image per the UPLOAD ORDER table; the tags resolve in the generation platform. ⚠️ Most sheets are tagged-in-platform but **not yet filed in-repo** (see the manifest's archival-gap note) — export/file them before these prompts are leaned on heavily.
- **Scale is landmark-based, never centimetres** — copy the landmark lines from the manifest Scale column into each shot (shield-bearer's crown ≈ just above Goliath's waist; Goliath ≈ 2× a man's shoulder width; Saul ≈ a head above the soldiers).
- **Goliath is size-capped, and the cap is written as landmarks, not adjectives.** He is a huge *man* (a little under twice an ordinary man's height), never a mythic titan. Superlative mass vocabulary — *colossal, enormous, monumental, towering, earth-shaking, ground tremor* — is what makes the model inflate him mid-shot into a 15 m giant, so prompts state the **scale cage** instead: two or three body-meeting contacts (crown-to-belt, knee-to-hip, elbow-to-crest), the shoulder-width multiple, and the ceiling ("a little under twice his height", "both men whole in one frame on one ground line"). Restate the cage in ACTION at the reveal beat *and* in POSITIVE LOCKS, and keep his weight **relative** ("heavier and slower than the bearer's step") rather than seismic. Avoid god's-eye overheads in a scale shot — they destroy the ground line the comparison depends on; use a high three-quarter that keeps both pairs of feet in frame. See [crs_table_Goliath_Complex.md](crs_table_Goliath_Complex.md#the-scale-cage-bounding-a-giant).
- **Subtitles / name supers / score are added in the edit.** Every prompt locks *diegetic sound only, no music, no on-screen text.*

| Clip | Scene | Beat | Runtime | Status |
|---|---|---|---|---|
| 1 | 1 | Aerial establishing → Israel camp | 15s | ✅ ready |
| 2 | 1 | Cross the valley → Philistine army | 10s | ✅ ready |
| 3 | 1 | Shield-bearer + Goliath emerge (scale reveal) | 12s | ✅ ready |
| 4 | 1 | Goliath taunt #1 + laugh | 10s | ✅ ready |
| 5 | 1 | The challenge — "pick a champion" | 15s | ✅ ready |
| 6 | 1 | "If I win, you serve us" + Israel's fear | 14s | ✅ ready |
| 7 | 1 | Pan up to Saul; "what is your answer?" | 12s | ✅ ready |
| 8 | 2 | Consternation; "we need a champion" | 13s | ✅ ready |
| 9 | 2 | Generals stall; wealth decree | 15s | ✅ ready |
| 10 | 3 | Funny soldiers — "lie at his feet and beg" | 15s | ✅ ready |
| 11–95 | 4–21 | — | — | pending |

---

## Clip 1 — Scene 1: Aerial establishing → Israel camp (15s)

### UPLOAD ORDER
| Slot | `@tag` | Becomes |
|---|---|---|
| 1 | `@valley_elah_3qf` | the master valley (two mountains + floor) |
| 2 | `@israel_camp_3qf` | the Israelite tent camp on its slope |

### Prompt
```
SCENE CONTEXT
Bright midday over an ancient Near-Eastern valley. A soaring aerial crosses barren, grassy
and treed mountains toward two great facing mountains with a broad valley between them, then
banks right and descends toward an army encamped with tents on a lower peak. The armies read
as distant scenery, no one in close view.

ACTIVE REFERENCES
@valley_elah_3qf — the master valley: two facing mountains with a broad dry valley floor
between; the left mountain green and partly treed with a tent camp on a lower peak, the right
mountain barren and rocky; a thin stream on the valley floor; sun high-left. 100% matches the
reference.
@israel_camp_3qf — the Israelite camp on its slope: rows of earth-tone goat-hair tents on
terraced ground, a cleared front edge overlooking the valley, banners on poles, weapon racks,
cook-fire rings. 100% matches the reference.

LOCATION MAP
Foreground: open sky and passing ochre ridgelines. Midground: the two facing mountains resolve
ahead with the valley between them. Background: distant ranges fading into heat haze. Movement
path: a continuous forward aerial that banks right and drops toward the tent camp on the left
(green) mountain's lower peak. Light from high-left.

FIRST FRAME / BLOCKING
High aerial already in motion over a barren ochre ridge, the two facing mountains and the
valley opening in the distance ahead, framed centre with headroom to descend into.

FORMAT MODE
One continuous aerial shot, the camera does not cut on its own.

OPTICS
84° wide FOV throughout, rectilinear, deep focus, natural motion blur.

CAMERA
Smooth high drone-style aerial at 60 km/h, gently descending; banks right over the valley and
eases down toward the tent camp, slowing to 25 km/h as the tents grow. Wide tonal latitude,
gentle highlight roll-off on the sunlit rock.

ACTION
The camera soars forward over successive mountains — some barren rock, some grassed, some
treed — until the two great facing mountains rise ahead with the valley between them. It banks
right and descends the green left mountain, revealing rows of tents on a lower peak, banners
stirring, thin cook-fire smoke rising, tiny distant figures moving among the tents.

PHYSICS
Banners and cook-fire smoke drift on a light wind; heat haze shimmers over the far valley;
shadows fall consistently to the lower-right from the high-left sun.

LIGHTING
Bright midday sun from high-left, 5600K, hard shadows in the ravines, dust haze 20% in the far
distance. Arid palette — ochre earth, dust-green scrub, pale rock.

AUDIO
Wind over the ridges, a faint distant camp murmur and stirring banners as the camp nears.
Diegetic sound only, no music, no on-screen text.

STYLE
Photoreal, hyperreal natural detail, epic scale, fine grain.

POSITIVE LOCKS
Two facing mountains with a valley between stay clearly readable; the left mountain green and
treed with the tent camp, the right barren and rocky; single high-left sun throughout; the camp
reads as distant tents and tiny figures, not close characters. Diegetic sound only, no music,
no on-screen text.
```

---

## Clip 2 — Scene 1: Cross the valley → Philistine army (10s)

### UPLOAD ORDER
| Slot | `@tag` | Becomes |
|---|---|---|
| 1 | `@valley_elah_3qf` | the valley basin + far barren mountain |
| 2 | `@philistine_army` | the massed Philistine host |

### Prompt
```
SCENE CONTEXT
Continuing over the Valley of Elah, the camera reaches the valley floor and crosses toward the
far barren mountain, revealing it covered by a massed Philistine army that spills down onto the
plain.

ACTIVE REFERENCES
@valley_elah_3qf — the valley basin; the far (right) mountain barren and rocky, the near valley
floor with a thin stream; sun high-left. 100% matches the reference.
@philistine_army — a massed foreign warrior host in bronze/slate/teal/oxblood faction gear
distinct from the Israelites, 3–4 build and face variations through the crowd. 100% matches the
reference.

LOCATION MAP
Foreground: the dry cracked valley floor and the stream passing beneath. Midground: the ground
rising toward the far barren slope. Background: the slope and plain densely covered with the
army. Light high-left.

FIRST FRAME / BLOCKING
Low fast aerial skimming the valley floor, the far barren mountain ahead, its slope just
beginning to reveal massed figures.

FORMAT MODE
One continuous forward-tracking shot, the camera does not cut on its own.

OPTICS
84° wide FOV, deep focus, natural motion blur.

CAMERA
Low aerial gliding forward at 45 km/h across the valley floor, tilting up slightly as the far
slope fills with the army.

ACTION
The camera crosses the valley floor and closes on the far mountain; what looked like bare rock
resolves into a vast army — rank on rank of warriors covering the slope and spilling onto the
plain, spears and banners bristling.

PHYSICS
Dust drifts over the crossing; heat shimmer thickens toward the massed men; banners and the
lines of spears sway.

LIGHTING
Midday sun high-left, 5600K, hard shadows, dust haze building 20%→30% toward the army. Arid
ochre and grey palette, the army a wall of bronze and dark leather.

AUDIO
Rising war-camp ambience — a low massed rumble of voices, clatter of gear, distant drums.
Diegetic sound only, no music, no on-screen text.

STYLE
Photoreal, hyperreal, epic scale, fine grain.

POSITIVE LOCKS
The far barren mountain and plain covered with a massed Philistine host in bronze/slate/teal/
oxblood gear; single high-left sun; heat shimmer over the plain. Diegetic sound only, no music,
no on-screen text.
```

---

## Clip 3 — Scene 1: Shield-bearer + Goliath emerge (12s) · SCALE-CRITICAL

### UPLOAD ORDER
| Slot | `@tag` | Becomes |
|---|---|---|
| 1 | `@valley_plain_3qf` | the Philistine plain |
| 2 | `@shield_bearer` | the "false giant" |
| 3 | `@goliath` | Goliath |
| 4 | `@goliath_shield` | the tower shield |
| 5 | `@goliath_spear` | the weaver's-beam spear |
| 6 | `@cast_scale` | proportion lock (scale only) |

### Prompt
```
SCENE CONTEXT
On the Philistine plain a broad shield-bearer strides out of the heat-shimmer and plants — for
a beat he looks like the champion. Then Goliath steps up behind him and stops: everything from
Goliath's belt upward — chest, shoulders, head — rises above the bearer's crown. Goliath then
takes three heavy steps forward.

ACTIVE REFERENCES
@valley_plain_3qf — a dry open valley battlefield floor, two rocky slopes framing it left and
right, a pebbled stream bank near-left, heat shimmer low to the ground. 100% matches the
reference.
@shield_bearer — a broad thick-set Philistine strongman at ordinary height; banded bronze
corselet, bronze cap with a short feather crest, bronze/slate/teal/oxblood palette; hard
watchful face. 100% matches the reference.
@goliath — a giant of a man built on human proportions, heavyweight-wrestler mass: coppery-bronze
fish-scale lamellar cuirass, bronze pauldrons with a central boss, engraved vambraces and greaves,
domed bronze helmet, heavy brow, thick dark beard. He stands a little under twice
@shield_bearer's height and about twice @shield_bearer's shoulder width. 100% matches the
reference.
@goliath_shield — a bronze-and-wood tower shield with a domed central boss, sized to Goliath's frame
rather than fitted to the man carrying it: set on the ground its lower rim is level with
@shield_bearer's ankles and its top rim rises about two and a half head-heights above his crown, so
his crown reaches only about seven-tenths of the way up the shield, and it is about twice as wide as
his shoulders are broad. He carries it with both arms and his shoulder, with visible effort. 100%
matches the reference.
@goliath_spear — a weaver's-beam thick dark hardwood shaft with a massive leaf-shaped iron head,
taller than a man; held at Goliath's side. 100% matches the reference.
@cast_scale — the cast ground-line lineup; use for relative proportion only.

LOCATION MAP
Foreground: heat-shimmering cracked earth. Midground: the shield-bearer plants centre, Goliath
steps up behind him. Background: the barren Philistine slope massed with distant troops. Camera
low and near the ground on the shadow side, tilting up.

FIRST FRAME / BLOCKING
Low worm's-eye, camera near ground level looking up through the heat-shimmer; the shield-bearer
strides out of the haze into centre frame with the tower shield and plants, filling the frame
heroically — nothing yet revealed behind him.
Scale cage — every one of these stays true in every frame once both men share the shot:
@shield_bearer's crown reaches just above Goliath's waist, at his belt line.
Goliath's kneecap sits level with @shield_bearer's hip.
With Goliath's arm hanging at his side, his elbow rides just above @shield_bearer's feather crest.
Goliath's shoulders are about twice @shield_bearer's shoulder width.
Two men of @shield_bearer's height standing one on the other's shoulders would overtop Goliath.
Both men keep their feet on the same visible ground line and both fit whole inside the frame
together, the bearer's full body from crest to boots readable beside Goliath.

FORMAT MODE
One continuous crane shot in three moves, the camera does not cut on its own.

OPTICS
63° wide FOV, low-angle — a wide low lens that lets the nearer figure loom and the background
recede. No lens change mid-shot; natural motion blur. From the reveal onward both men sit at
similar camera distance so perspective reports their sizes honestly.

CAMERA
A single unbroken crane. Move 1: planted low and tilted up, glorifying the shield-bearer.
Move 2: the crane climbs, still angled low, to contain Goliath standing behind — the effort of
the tilt-up is the shock; keep the angle low so Goliath keeps his full height. Move 3: the crane
settles at about the height of Goliath's helmet and swings a quarter around into a high
three-quarter two-shot that looks down the length of both bodies with both pairs of boots on the
same ground line in frame.

ACTION
0.0s to 4.0s — the shield-bearer strides out of the shimmer and plants, tower shield set, his crown
reaching only about seven-tenths of the way up it, reading huge from below.
4.0s to 8.0s — Goliath steps up behind him and stops; the camera keeps climbing to hold him. The
bearer's crown sits just above Goliath's belt, Goliath's kneecap level with the bearer's hip,
Goliath's hanging elbow just above the bearer's crest, Goliath twice as broad across the
shoulders, his spear a dark column at his side.
8.0s to 12.0s — the camera swings around into the high three-quarter two-shot, the "muscle-man"
small beside Goliath and still whole in frame, the same belt-line, knee-to-hip and elbow-to-crest
contacts holding from the new angle; Goliath takes three slow heavy steps forward as the
shield-bearer steps aside.

PERFORMANCE
The shield-bearer plays it hard and proud, jaw set, scanning the far slope. Goliath moves with
the unhurried weight of a very large man — each step slower and heavier than the bearer's, chin
high, contemptuous. Pore-level skin, sweat sheen in the heat, living eyes.

PHYSICS
Each of Goliath's boots sets down with real weight — a low puff of dust lifts around the sole,
his greaves and bronze scale creaking on the step. The ground stays firm and still beneath him
and the camera holds steady through the footfalls. The tower shield hangs heavy in the bearer's
arm, his shoulder dropping under it. Heat-shimmer bends the air; sweat and fine dust cling to
skin.

LIGHTING
Harsh midday sun from high, 5600K, hard short shadows, heat-shimmer haze 30% low to the ground.
Arid ochre and grey ground, bronze armour catching the sun.

AUDIO
Wind and heat-buzz, the bearer's boots on cracked earth, then Goliath's boot-falls — deeper,
slower and heavier than the bearer's, leather and bronze creaking with each step, the ground
sound staying dry and solid. A distant massed murmur from the Philistine slope. Diegetic sound
only, no music, no on-screen text.

STYLE
Photoreal, hyperreal, grounded epic realism, true human proportions at giant size, fine grain.

POSITIVE LOCKS
Hold the scale cage in every frame and from every angle: the bearer's crown at Goliath's belt
line, Goliath's kneecap at the bearer's hip, Goliath's hanging elbow just above the bearer's
crest, Goliath about twice the bearer's shoulder width, Goliath a little under twice the bearer's
height, both men whole in frame on one ground line. Goliath stays a huge man of human
proportion at every moment of the shot, the same size at 12.0s as at 4.0s. The tower shield stays
at its own capped size — the bearer's crown reaching only about seven-tenths of the way up it, its
lower rim at his ankles — and stays in his hands; the weaver's-beam spear stays with Goliath. Goliath keeps his coppery-bronze scale cuirass
and domed helmet. Single high sun. Diegetic sound only, no music, no on-screen text.
```

---

## Clip 4 — Scene 1: Goliath taunt #1 + laugh (10s)

### UPLOAD ORDER
| Slot | `@tag` | Becomes |
|---|---|---|
| 1 | `@valley_plain_3qf` | the Philistine plain |
| 2 | `@goliath` | Goliath |
| 3 | `@goliath_spear` | his planted spear |

### Prompt
```
SCENE CONTEXT
On the Philistine plain, Goliath sweeps his gaze across the Israelite mountain and taunts them,
then laughs.

ACTIVE REFERENCES
@goliath — a giant of a man built on human proportions, heavyweight mass; coppery-bronze fish-scale
cuirass, bronze pauldrons with a central boss, domed bronze helmet, heavy brow, thick dark beard;
a little under twice an ordinary man's height and about twice an ordinary man's shoulder width.
Voice: huge, booming, deep, arrogant, echoing across the valley. 100% matches the reference.
@valley_plain_3qf — a dry open battlefield floor, two rocky slopes framing it, heat shimmer low
to the ground. 100% matches the reference.
@goliath_spear — a weaver's-beam dark hardwood shaft with a leaf-shaped iron head, taller than a
man; planted butt-down at his side, its head reaching about to his shoulder. 100% matches the
reference.

LOCATION MAP
Foreground: cracked earth and shimmer. Midground: Goliath centre, spear planted, facing the
Israelite slope (camera-left). Background: the barren Philistine slope with distant troops.
Camera low on the shadow side, looking up.

FIRST FRAME / BLOCKING
Low-angle medium on Goliath from below, spear planted at his side, chin lifting as he draws
breath; he fills the frame, the far slope small beyond his shoulder.

FORMAT MODE
One continuous shot, the camera does not cut on its own.

OPTICS
29° portrait-compression FOV from a low angle — a menacing bust that keeps his mass. Natural
motion blur.

CAMERA
Low, static easing to a slow push at 1 km/h toward his face on the taunt; his eye-line angled
down toward the distant Israelite slope.

ACTION
Goliath sweeps his gaze across the Israelite mountain and booms the taunt. A beat, then he
throws his head back and laughs, deep and rolling.

PERFORMANCE
Contempt in the eyes, a slow cruel smile before the line; on the laugh the whole chest heaves,
beard shaking, teeth bared. Muscle-level sneer, living eyes, sweat sheen on the brow.

PHYSICS
Breath and spit catch the light on the laugh; heat-shimmer bends the air behind him; the heavy
spear stays planted with weight.

LIGHTING
Harsh midday sun from high, 5600K, hard shadows carving the brow and cheekbones; heat haze 30%.

AUDIO
Goliath's booming taunt and rolling laugh carrying across the valley, wind, distant murmur.
Line: "I see you all cowering on your mountain. Soon to be your grave." Diegetic sound only, no
music, no on-screen text.

POSITIVE LOCKS
Goliath keeps his coppery-bronze scale cuirass and domed helmet, spear planted at his side with
its head at about his shoulder — that contact holds all the way through the push-in and caps his
size. He stays a huge man of human proportion, the same size in the last frame as in the first;
the low angle keeps his full height without stretching him. Single high sun. Diegetic sound only,
no music, no on-screen text.
```

---

## Clip 5 — Scene 1: The challenge — "pick a champion" (15s)

### UPLOAD ORDER
| Slot | `@tag` | Becomes |
|---|---|---|
| 1 | `@valley_plain_3qf` | the Philistine plain |
| 2 | `@goliath` | Goliath |
| 3 | `@shield_bearer` | the snickering shield-bearer |
| 4 | `@philistine_army` | the roaring host |
| 5 | `@goliath_spear` | his spear |

### Prompt
```
SCENE CONTEXT
Goliath issues the wager — pick a champion, and if he wins the Philistines will be Israel's
slaves — and the Philistine army roars with laughter while his shield-bearer snickers.

ACTIVE REFERENCES
@goliath — a giant of a man built on human proportions, heavyweight mass; coppery-bronze scale
cuirass, domed bronze helmet, heavy brow, dark beard; a little under twice @shield_bearer's height
and about twice @shield_bearer's shoulder width. Voice: huge, booming, mocking. 100% matches the
reference.
@shield_bearer — a broad Philistine strongman at ordinary height, banded bronze corselet,
feather-crested cap; his crown reaches just above Goliath's waist at the belt line, Goliath's
kneecap sits level with his hip, and Goliath's hanging elbow rides just above his feather crest.
100% matches the reference.
@philistine_army — a massed foreign host on the barren slope behind, bronze/slate/teal/oxblood
gear, varied faces and builds. 100% matches the reference.
@valley_plain_3qf — a dry open battlefield floor framed by two rocky slopes, heat shimmer. 100%
matches the reference.
@goliath_spear — a weaver's-beam shaft with a leaf-shaped iron head, in Goliath's hand. 100%
matches the reference.

LOCATION MAP
Foreground: cracked earth. Midground: Goliath centre with the shield-bearer just off his flank,
shorter (crown just above Goliath's waist). Background: the barren slope massed with the
Philistine army. Camera low-ish on the shadow side.

FIRST FRAME / BLOCKING
Low wide on Goliath centre, spear in hand, the shield-bearer at his flank, the massed army
rising behind. Scale cage, true in every frame both men share: the bearer's crown at Goliath's
belt line, Goliath's kneecap at the bearer's hip, Goliath's shoulders about twice the bearer's
width, both men whole in frame with their boots on one visible ground line.

FORMAT MODE
Sequential cuts, no timecodes. Cuts only at the specified points, the camera does not cut on its
own.

OPTICS
CUT 1: 47° neutral wide on Goliath and the slope. CUT 2: 29° on Goliath as he lifts his hands.
CUT 3: 29° on the shield-bearer snickering. No drift mid-segment.

CAMERA
Low eye-line up at Goliath; on CUT 3 a quick reframe to the shield-bearer at his flank.

ACTION
CUT 1 — Goliath booms: "This is the fortieth day that I have stood here to issue this challenge,
and I grow bored. I once again offer you this chance — pick a champion and let him fight me. If
he wins,"
CUT 2 — Goliath lifts both hands wide: "we shall be your slaves."
CUT 3 — the Philistine army roars with laughter behind him; the shield-bearer at his flank
snickers, shoulders shaking.

PERFORMANCE
Goliath theatrical and mocking; the army's laughter rolls in a wave; the shield-bearer's snicker
is mean and private, a sidelong grin. Pore-level realism, living eyes.

PHYSICS
Dust and heat-shimmer; spears and banners sway as the army laughs; Goliath's raised arms move
with real mass.

LIGHTING
Midday sun high, 5600K, hard shadows, haze 30%. Bronze armour catching the sun against arid
ochre ground.

AUDIO
Goliath's booming challenge, then a huge rolling wave of army laughter, the shield-bearer's
nearer snicker. Lines as above. Diegetic sound only, no music, no on-screen text.

POSITIVE LOCKS
The shield-bearer's crown stays just above Goliath's waist at the belt line, Goliath's kneecap
stays level with the bearer's hip, and Goliath stays a little under twice the bearer's height and
about twice his shoulder width — the same size on CUT 3 as on CUT 1, a huge man of human
proportion throughout. Goliath keeps his scale cuirass, domed helmet and spear; the host stays
Philistine-geared on the barren slope; single high sun. Diegetic sound only, no music, no
on-screen text.
```

---

## Clip 6 — Scene 1: "If I win, you serve us" + Israel's fear (14s)

### UPLOAD ORDER
| Slot | `@tag` | Becomes |
|---|---|---|
| 1 | `@valley_plain_3qf` | the Philistine plain (start) |
| 2 | `@goliath` | Goliath |
| 3 | `@philistine_army` | the roaring host |
| 4 | `@israel_camp_3qf` | the Israelite front edge (end) |
| 5 | `@israelite_army` | the fearful front line |

### Prompt
```
SCENE CONTEXT
Goliath finishes the wager — if he wins, Israel serves the Philistines — the Philistine camp
roars in approval, and the camera sweeps across the valley and pushes into the Israelite front
line to find fear on the soldiers' faces.

ACTIVE REFERENCES
@goliath — a giant of a man built on human proportions, heavyweight mass; coppery-bronze scale
cuirass, domed bronze helmet; a little under twice an ordinary soldier's height and about twice an
ordinary soldier's shoulder width. Voice: huge, booming, triumphant. 100% matches the reference.
@philistine_army — a massed foreign host on the barren slope, bronze/slate/teal/oxblood gear; the
nearest of them stand at about Goliath's waist, the on-screen yardstick for his size. 100% matches
the reference.
@israel_camp_3qf — the Israelite camp's cleared front edge overlooking the valley, rows of tents
behind. 100% matches the reference.
@israelite_army — Israelite front-line soldiers, fearful baseline, varied faces and builds, kit
distinct from the Philistines. 100% matches the reference.
@valley_plain_3qf — the dry plain framed by two slopes, heat shimmer. 100% matches the reference.

LOCATION MAP
Start on the plain — foreground cracked earth, midground Goliath, background Philistine slope.
The pan and push carries across the valley to the Israel front edge — midground a rank of
Israelite soldiers at the cleared edge, background their tents. Sun high-left throughout.

FIRST FRAME / BLOCKING
Low wide on Goliath centre, arms starting to rise, the Philistine slope massed behind him.

FORMAT MODE
One continuous shot — Goliath's line and the roar, then a sweeping pan and push across the
valley into the Israelite front line. The camera does not cut on its own.

OPTICS
Begins 47° wide on Goliath; as it pans and pushes across the valley it tightens to 29° on the
fearful Israelite faces — a smooth push, no abrupt lens jump.

CAMERA
Holds low on Goliath for the line, then pans right and cranes across the valley at speed,
pushing in on the Israelite front rank, ending on tight fearful faces.

ACTION
Goliath lifts his hands again and booms: "But if I win and kill your champion — you shall be our
slaves and serve us." The Philistine camp roars in approval behind him. The camera pans off
Goliath and sweeps across the valley, pushing into the Israelite front line: soldiers at the
cleared edge, wide-eyed, jaws tight, some stepping back, fear rippling down the rank.

PERFORMANCE
Goliath triumphant; the Philistine roar exultant. The Israelites' fear is muscle-level — throats
swallowing, eyes darting, knuckles whitening on spear shafts, a half-step back down the rank.

PHYSICS
Heat-shimmer over the crossing; banners sway; dust; the Israelite rank shifts and compresses as
men flinch.

LIGHTING
Midday sun high-left, 5600K, hard shadows on both slopes; haze 30% over the valley.

AUDIO
Goliath's booming line, a huge Philistine roar of approval, then closer on the Israel side —
uneasy muttering, shuffling feet, tense breath. Line as above. Diegetic sound only, no music, no
on-screen text.

POSITIVE LOCKS
Goliath stays a huge man of human proportion — the nearest Philistine soldiers reach about his
waist and he is about twice their shoulder width, holding that size for as long as he is in frame.
Goliath keeps his scale cuirass and domed helmet; Philistine host on the barren slope, Israelite
soldiers in distinct kit at their cleared front edge with tents behind; visible fear on the
Israelite faces; single high-left sun held across the whole pan. Diegetic sound only, no music,
no on-screen text.
```

---

## Clip 7 — Scene 1: Pan up to Saul; "what is your answer?" (12s)

### UPLOAD ORDER
| Slot | `@tag` | Becomes |
|---|---|---|
| 1 | `@israel_camp_3qf` | the camp + command tent on the peak |
| 2 | `@saul` | King Saul |
| 3 | `@israelite_army` | the soldiers before the tent |
| 4 | `@cast_scale` | Saul's relative height (scale only) |

### Prompt
```
SCENE CONTEXT
The camera pans up to a lower peak where a large command tent stands with soldiers before it;
among them King Saul stands head-and-shoulders above the rest. Goliath's voice carries up from
the valley demanding an answer.

ACTIVE REFERENCES
@israel_camp_3qf — the Israelite camp on its slope, a cleared front edge, rows of tents, and a
large command tent on the lower peak. 100% matches the reference.
@saul — King Saul: tall, broad-shouldered, careworn; short greying hair and a full salt-and-
pepper beard; a gold diadem band with a central rosette medallion; bronze fish-scale armor under
a deep-purple mantle with a crimson-red border; he stands a clear head above the soldiers. 100%
matches the reference.
@israelite_army — soldiers standing before the tent, varied faces and builds, ordinary height.
100% matches the reference.
@cast_scale — the cast ground-line lineup; use for Saul's relative height only.

LOCATION MAP
Foreground: the cleared slope and soldiers' heads. Midground: the rank of soldiers before the
large command tent, Saul among them standing a head taller. Background: the tent and the valley
falling away below. Sun high-left. Goliath is far below, offscreen — voice only.

FIRST FRAME / BLOCKING
Camera low on the slope, beginning to crane and tilt up toward the peak; soldiers' backs and the
command tent coming into view above.

FORMAT MODE
One continuous rising shot, the camera does not cut on its own.

OPTICS
47° neutral FOV craning up, settling to 29° on Saul once he is found among the men. Natural
motion blur.

CAMERA
A steady crane and tilt up the slope to the peak, discovering the command tent and the rank of
soldiers, drifting to frame Saul standing a head above the others.

ACTION
The camera rises to the lower peak: the large command tent, a knot of soldiers before it, and
among them King Saul — a head and shoulders above the men around him — jaw tight as he stares
down toward the valley. From far below, Goliath's booming voice rolls up: "What is your answer,
people of Israel?" Saul's expression hardens.

PERFORMANCE
Saul careworn, kingly, unsettled — a slow jaw-clench, eyes fixed down-valley; the soldiers
around him glance uneasily at one another.

PHYSICS
Saul's purple mantle and the tent canvas stir in the wind; banners sway; contact shadows ground
everyone on the slope.

LIGHTING
Midday sun from high-left, 5600K, hard shadows; light dust haze.

AUDIO
Wind over the peak, uneasy soldier murmur, and Goliath's distant booming voice echoing up from
the valley. Offscreen VO (huge and distant): "What is your answer, people of Israel?" Diegetic
sound only, no music, no on-screen text.

POSITIVE LOCKS
Saul stands a clear head above the average soldiers around him; he keeps the gold diadem, the
deep-purple crimson-bordered mantle and bronze scale armor; Goliath stays offscreen (voice only,
never in frame); single high-left sun. Diegetic sound only, no music, no on-screen text.
```

---

## Clip 8 — Scene 2: Consternation; "we need a champion" (13s)

### UPLOAD ORDER
| Slot | `@tag` | Becomes |
|---|---|---|
| 1 | `@saul_tent_3qf` | the command-tent interior |
| 2 | `@saul` | King Saul |
| 3 | `@saul_council` | the three counsellors (#1 speaks) |
| 4 | `@general` | Saul's general |

### Prompt
```
SCENE CONTEXT
Inside King Saul's command tent, consternation on Saul's face; his men glance sideways at him. A
counsellor urges finding a champion, and Saul answers that he needs a brave man to face the
giant.

ACTIVE REFERENCES
@saul_tent_3qf — the command-tent interior at a three-quarter angle: a carpeted dais with a
carved dark-wood throne at the far-left, a wooden map table to the right, an armor stand right
of centre near the entrance, a large deep-red patterned carpet over the centre of the floor, and
a partly open entrance flap in the far wall showing the valley; warm daylight from the flap plus
oil-lamp glow. 100% matches the reference.
@saul — King Saul: tall, broad, careworn; greying hair, salt-and-pepper beard, gold diadem with
a central rosette, bronze fish-scale armor under a deep-purple crimson-bordered mantle. Voice:
weary, regal, low. 100% matches the reference.
@saul_council — three distinct older counsellors, robes over armor, rank indicators; counsellor
#1 speaks. Voice (#1): earnest, deferential. 100% matches the reference.
@general — a senior commander at Saul's side. 100% matches the reference.

LOCATION MAP
Foreground: the near edge of the map table. Midground: Saul by the dais at frame-left, his three
counsellors and the general grouped around the map table centre-right on the deep-red carpet.
Background: the open entrance flap and daylight in the far wall. Camera on the shadow side, eye-
level.

FIRST FRAME / BLOCKING
Three-quarter interior wide, eye-level: Saul at the dais frame-left, jaw set in consternation;
the counsellors and the general around the map table on the red carpet, glancing sideways at
him.

FORMAT MODE
Sequential cuts, no timecodes. Cuts only at the specified points, the camera does not cut on its
own.

OPTICS
CUT 1: 47° two-shot of Saul and his men. CUT 2: 29° on Counsellor #1. CUT 3: 29° on Saul. No
drift mid-segment.

CAMERA
Eye-level, gentle handheld with a 1 cm tremor; a small push on Saul's answer.

ACTION
CUT 1 — Saul's face tight with worry; his men glance sideways at him.
CUT 2 — Counsellor #1 steps in, deferential: "We need to find a champion, O King."
CUT 3 — Saul, low and weary but hardening: "Yes. I need one of my men who is brave enough to go
down there and show that brute that we are not playing here."

PERFORMANCE
Saul carries the weight — brow furrowed, a slow breath before he speaks; the counsellor careful
and bowing slightly; the general avoids his eye. Restraint throughout; pore-level realism, warm
lamp catch-lights in living eyes.

PHYSICS
Canvas walls sway faintly; oil-lamp flames flicker; robes and the purple mantle hang with mass;
daylight from the flap and warm lamp glow both fall consistently.

LIGHTING
Warm daylight from the open flap in the far wall plus soft warm oil-lamp glow, 4000K, gentle
shadows; the deep-red carpet and textiles catch the warm light.

AUDIO
Muffled wind and distant camp sound through the flap, cloth and lamp ambience, the two lines.
Diegetic sound only, no music, no on-screen text.

POSITIVE LOCKS
Tent layout holds — dais throne far-left, map table right, armor stand right of centre near the
entrance, large deep-red carpet over the centre floor, open flap showing the valley; Saul keeps
the gold diadem, deep-purple crimson-bordered mantle and bronze scale armor; the light direction
agrees between the flap and the lamps. Diegetic sound only, no music, no on-screen text.
```

---

## Clip 9 — Scene 2: Generals stall; wealth decree (15s)

### UPLOAD ORDER
| Slot | `@tag` | Becomes |
|---|---|---|
| 1 | `@saul_tent_3qf` | the command-tent interior |
| 2 | `@saul` | King Saul |
| 3 | `@general` | Saul's general |
| 4 | `@saul_council` | the counsellors |

### Prompt
```
SCENE CONTEXT
In the command tent, Saul looks to his generals, who avoid his eye by studying the clouds;
Goliath's voice needles from below; Saul decrees a great reward for whoever defeats the
Philistine.

ACTIVE REFERENCES
@saul_tent_3qf — the command-tent interior at a three-quarter angle: dais throne far-left, map
table right, armor stand right of centre near the entrance, a large deep-red carpet over the
centre floor, a partly open entrance flap in the far wall showing the valley; warm daylight plus
lamp glow. 100% matches the reference.
@saul — King Saul; gold diadem with a central rosette, greying hair and salt-and-pepper beard,
deep-purple crimson-bordered mantle over bronze fish-scale armor. Voice: weary, regal. 100%
matches the reference.
@general — a senior commander at Saul's side. 100% matches the reference.
@saul_council — three distinct older counsellors around the map table. 100% matches the
reference.

LOCATION MAP
Foreground: the map table. Midground: Saul frame-left by the dais, the general and counsellors
around the table on the deep-red carpet. Background: the open flap and daylight. Camera on the
shadow side, eye-level. Goliath is far below, offscreen — voice only.

FIRST FRAME / BLOCKING
Three-quarter interior medium-wide: Saul turning his head left then right toward his generals,
who tip their faces up as if studying the tent roof and the sky beyond the flap.

FORMAT MODE
One continuous shot, the camera does not cut on its own.

OPTICS
47° neutral medium-wide, easing to 29° on Saul for the decree. Natural motion blur.

CAMERA
Eye-level, a slow drift from the evasive generals to settle on Saul as he gives the order.

ACTION
Saul looks left and right; his generals lift their eyes and study the clouds, avoiding him. From
far below Goliath's voice needles up: "I am waiting." Saul draws a breath and decrees: "Announce
to our army that I will shower whoever defeats that Philistine with wealth to last him beyond the
rest of his days."

PERFORMANCE
The generals' evasion is comic-restrained — eyes up, lips pressed, one clearing his throat;
Saul's flash of frustration then resolve, a firm set of the jaw on the decree. Pore-level
realism, warm catch-lights.

PHYSICS
Canvas and the purple mantle sway; oil-lamp flames flicker; the hide map lifts faintly at its
edge in the draught from the flap.

LIGHTING
Warm daylight from the flap plus oil-lamp glow, 4000K, gentle shadows; deep-red textiles warm in
the light.

AUDIO
Cloth and lamp ambience, wind and faint camp sound through the flap, Goliath's distant booming
"I am waiting," then Saul's decree. Lines as above. Diegetic sound only, no music, no on-screen
text.

POSITIVE LOCKS
Tent layout holds (throne far-left, map table right, armor stand right of centre near the
entrance, deep-red centre carpet, open flap showing the valley); Saul's regalia consistent;
Goliath stays offscreen (voice only, never in frame); light direction consistent. Diegetic sound
only, no music, no on-screen text.
```

---

## Clip 10 — Scene 3: Funny soldiers — "lie at his feet and beg" (15s)

### UPLOAD ORDER
| Slot | `@tag` | Becomes |
|---|---|---|
| 1 | `@israel_camp_3qb` | the rear ranks (looking up-slope) |
| 2 | `@funny_soldier_1` | Funny Soldier #1 (lanky) |
| 3 | `@funny_soldier_2` | Funny Soldier #2 (stout) |
| 4 | `@saul_council` | the departing counsellor |
| 5 | `@saul` | Saul glaring (insert) |
| 6 | `@saul_tent_3qf` | the tent entrance (insert) |

### Prompt
```
SCENE CONTEXT
A counsellor leaves to make the announcement; at the back of the Israelite ranks two comic
soldiers whisper — one vows to beg for his life, the other mocks him — then both look up
innocently as King Saul turns to glare from his tent.

ACTIVE REFERENCES
@israel_camp_3qb — the Israelite camp seen from the front edge looking back up-slope into the
rear ranks: rows of goat-hair tents, weapon racks, banners, a rocky path; the command tent
higher up the slope; sun from screen-right. 100% matches the reference.
@funny_soldier_1 — LOCKED CAMEO: lanky with a long neck, a prominent hooked nose, wild
expressive brows, a gap-toothed grin, and an oversized helmet that keeps slipping. Voice: nervy,
conspiratorial whisper. 100% matches the reference.
@funny_soldier_2 — LOCKED CAMEO: short and stout, a round ruddy face, a huge bushy mustache and
unibrow, and a permanently dented helmet. Voice: gruff, slow, dim. 100% matches the reference.
@saul_council — a counsellor walking off up-slope toward the tent to make the announcement. 100%
matches the reference.
@saul — King Saul at the command-tent entrance up-slope, glaring down; gold diadem, deep-purple
crimson-bordered mantle over bronze scale armor. 100% matches the reference.
@saul_tent_3qf — the command-tent entrance flap Saul glares from (used for the insert only). 100%
matches the reference.

LOCATION MAP
Foreground: the two funny soldiers at the back of the ranks, camera-close. Midground: rows of
tents and soldiers; the counsellor moving off up-slope. Background: the command tent higher on
the slope where Saul appears. Sun from screen-right.

FIRST FRAME / BLOCKING
On the two funny soldiers in the rear rank, heads together conspiratorially; behind them a
counsellor is already walking away up-slope toward the tent.

FORMAT MODE
Sequential cuts, no timecodes. Cuts only at the specified points, the camera does not cut on its
own.

OPTICS
CUT 1: 47° two-shot of the funny soldiers as the camera pushes in. CUT 2: 29° on Funny Soldier
#1 whispering. CUT 3: 29° on Funny Soldier #2. CUT 4: 18° insert up at Saul glaring. CUT 5: back
to 47° on both soldiers looking up. No drift mid-segment.

CAMERA
Eye-level handheld with a 1 cm tremor; a quick push in to the two at the back at the start; the
insert to Saul is a tighter locked frame from below.

ACTION
CUT 1 — the counsellor leaves up-slope; the camera pushes in to the two soldiers at the back,
heads together.
CUT 2 — Funny Soldier #1 whispers, wide-eyed: "If no one comes forward and he picks me to fight
that monster down there, I tell you — I will go lie at his feet and beg for my life."
CUT 3 — Funny Soldier #2 snickers, then mutters deadpan: "Go lie at — his feet, Funny."
CUT 4 — INSERT: up at the command tent, King Saul turns and glares down at his men.
CUT 5 — both soldiers instantly tip their faces up to the clouds, wide-eyed and innocent,
holding still.

PERFORMANCE
Funny Soldier #1's terror is theatrical, hands fluttering, helmet slipping over one eye; Funny
Soldier #2 is slow and dim, mustache twitching on the snicker; on Saul's glare both freeze and
gaze skyward with cartoonish innocence. Restraint on the button — only the eyes move. Pore-level
realism.

PHYSICS
Helmets shift on their heads — #1's oversized helmet slipping, #2's dented; banners and tent
canvas sway; dust drifts; contact shadows ground both men.

LIGHTING
Midday sun from screen-right (matching the back-plate), 5600K, hard shadows; light dust haze.

AUDIO
Camp murmur and wind, the two whispered lines and Funny Soldier #2's snicker, then a beat of
guilty silence on Saul's glare. Lines as above. Diegetic sound only, no music, no on-screen text.

POSITIVE LOCKS
Funny Soldier #1 lanky with a slipping oversized helmet, hooked nose and gap-toothed grin; Funny
Soldier #2 short and stout with a bushy mustache-unibrow and a dented helmet — cameo signatures
identical; Saul in the insert keeps the gold diadem and deep-purple crimson-bordered mantle; sun
from screen-right throughout. Diegetic sound only, no music, no on-screen text.
```

---

_Companion to: [Goliath_Complex_Script.md](script_&_scenes/Goliath_Complex_Script.md) · [Goliath_Complex_Scene_&_Clip_Breakdown.md](script_&_scenes/Goliath_Complex_Scene_&_Clip_Breakdown.md) · [assets/MANIFEST.md](assets/MANIFEST.md). Next block: Scene 4 (Clips 11–14)._
