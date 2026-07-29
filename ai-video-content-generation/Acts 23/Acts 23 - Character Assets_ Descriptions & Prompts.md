# Acts 23 — Character Assets: Refined Descriptions & Generation Prompts

**Project:** 90-Second Humorous Clip on Acts 23
**Style:** Realism/Hyperrealism (not 3D animation)
**Status:** Descriptions locked · Prompts ready for generation
**Sheet standard:** Solid mid-gray background · three views (face close-up, full-body front, 3/4 back) · no props, no text, no scenery · baseline expressions only

---

## Locked Design Decisions (Summary)

| # | Decision | Lock |
|---|----------|------|
| 1 | TT#1 wardrobe | Navy jacket, white tee, slim black jeans, white minimal sneakers, smartwatch, blue glow accent |
| 2 | TT#2 wardrobe/hair | Burgundy blazer, black tank, black jeans, black low-tops, sleek straight mid-part chest-length hair, silver earpiece |
| 3 | Future signal | Thin blue glow piping — his collar edge, her lapel edge |
| 4 | Heights | Relative only: TT#1 half a head taller than TT#2 |
| 5 | Pharisee era | Period-plausible 1st-century dress; no modern tallit/tefillin |
| 6 | Props | All off character sheets → separate prop assets (smartwatch excepted, it is worn) |
| 7 | Paul | No chains on sheet; clean cream robes stay |
| 8 | Angel | No baked-in glow; folded wings to mid-calf; 3/4-back view required |
| 9 | Commander | Casual armor = no helmet, undone top shoulder buckles, visible tunic sleeves |
| 10 | Expressions | Baseline only on sheets; arcs (hunger, grins, collapse) driven per-shot in video prompts |
| 11 | Crowd | One group sheet, 4 distinct archetype variations |

> **Note on relative height:** Each character sheet is generated separately, so the TT#1-taller-than-TT#2 relationship cannot be encoded in the sheets themselves. State it explicitly in every two-shot video prompt ("he stands half a head taller than her").

---

## 1. Time Traveler #1 (Male) — "The Observer"

### Refined Description

- **Age/Build:** Mid-twenties African man, tall, lean athletic build
- **Skin:** Deep dark brown, even tone
- **Hair:** Clean low-cut fade, **single straight shaved razor line on the left temple**
- **Face:** Clean-shaven (deliberate — every ancient-world character is bearded, so a bare face reads "not from here" in any shot), strong straight eyebrows, dark brown eyes, **small mole on left cheekbone**
- **Baseline expression:** Relaxed slight smile
- **Wardrobe:** Fitted navy sport jacket with **one thin glowing blue seam along the collar edge**, plain white crew-neck t-shirt, slim-fit black jeans (no distressing), minimal white leather low-top sneakers (no visible logos), slim black smartwatch with thin blue light accent on left wrist
- **Off-sheet (separate props):** Glowing juice pipe (blue internal light)

### Image-Generation Prompt

```
Character reference sheet on a solid mid-gray studio background, even soft lighting, photorealistic.
Three views of the same character, consistent across all views:
[1] front-facing close-up portrait of the face,
[2] full-body front view showing the complete outfit,
[3] full-body three-quarter back view.
Character: African man in his mid-twenties, tall lean athletic build, deep dark brown skin,
clean low-cut fade haircut with a single straight shaved razor line on the left temple,
clean-shaven, strong straight eyebrows, dark brown eyes, small mole on his left cheekbone,
relaxed slight smile.
Wearing a fitted modern navy sport jacket with a single thin glowing blue seam running along
the collar edge, a plain white crew-neck t-shirt, slim-fit black jeans with no distressing,
minimal white leather low-top sneakers with no visible logos, and a slim black smartwatch
with a thin blue light accent on his left wrist.
Neutral standing pose, arms relaxed. Clean sheet layout, no text labels, no props, no scenery.
```

### QA Checklist (accept/reject the generated sheet)

- [ ] Same face, fade + razor line, and outfit in all three views (razor line stays on the LEFT temple)
- [ ] Face view large, sharp, well-lit; mole present on left cheekbone
- [ ] Full outfit visible collar to sneakers, nothing cropped
- [ ] Glow seam is one thin line on the collar edge only — reject if glow spreads or multiplies
- [ ] Background solid mid-gray, no gradients or scenery
- [ ] Clean-shaven in every view (models love adding stubble — reject if present)

---

## 2. Time Traveler #2 (Female) — "The Snack Enthusiast"

### Refined Description

- **Age/Build:** Mid-twenties African woman, tall with confident upright posture (half a head shorter than TT#1)
- **Skin:** Warm golden-beige, glowing healthy tone
- **Hair:** Sleek straight, **middle part**, chest-length, dark brown-black, high natural shine
- **Face:** Oval face, high cheekbones, large dark brown almond-shaped eyes, full defined eyebrows, **small beauty mark under the right eye**
- **Baseline expression:** Warm, slightly asymmetric smile (full mischievous grin driven per-shot)
- **Wardrobe:** Fitted deep burgundy blazer with **one thin glowing blue seam along the lapel edge**, black tank top, slim-fit black jeans (matches TT#1 — team unity), clean black leather low-top sneakers, small silver earpiece in right ear
- **Off-sheet (separate props):** Futuristic holographic chips bag

### Image-Generation Prompt

```
Character reference sheet on a solid mid-gray studio background, even soft lighting, photorealistic.
Three views of the same character, consistent across all views:
[1] front-facing close-up portrait of the face,
[2] full-body front view showing the complete outfit,
[3] full-body three-quarter back view.
Character: African woman in her mid-twenties, tall with a confident upright posture,
warm golden-beige skin, oval face, high cheekbones, large dark brown almond-shaped eyes,
full defined eyebrows, a small beauty mark under her right eye, warm slightly asymmetric smile,
sleek straight dark brown-black hair with a middle part, falling to chest length, high natural shine.
Wearing a fitted deep burgundy blazer with a single thin glowing blue seam running along
the lapel edge, a black tank top, slim-fit black jeans with no distressing,
clean black leather low-top sneakers, and a small silver earpiece in her right ear.
Neutral standing pose, arms relaxed. Clean sheet layout, no text labels, no props, no scenery.
```

### QA Checklist

- [ ] Same face, hair part, and outfit in all three views (beauty mark stays under the RIGHT eye)
- [ ] Face view large, sharp, well-lit
- [ ] Hair is sleek and straight with a clean middle part in every view — reject waves or changed part
- [ ] Back view shows chest-length hair from behind (defining back-side feature)
- [ ] Glow seam is one thin line on the lapel edge only
- [ ] Full outfit visible, sneakers included
- [ ] Background solid mid-gray

---

## 3. Paul — "The Confident Prisoner"

### Refined Description

- **Age/Build:** Early fifties Middle Eastern man, average height, dignified bearing
- **Skin:** Olive to light brown
- **Hair:** Dark brown with grey streaks, medium length, slightly tousled but dignified
- **Beard:** Full, well-kept, salt-and-pepper
- **Baseline expression:** Calm peaceful eyes, faint serene smile
- **Wardrobe:** Clean, well-maintained cream/off-white linen robes (1st-century Roman-provincial style — the cleanliness IS the joke), simple leather sandals
- **Off-sheet (separate props):** Roman chains (loose/broken) — added per-scene, not baked into the sheet

### Image-Generation Prompt

```
Character reference sheet on a solid mid-gray studio background, even soft lighting, photorealistic.
Three views of the same character, consistent across all views:
[1] front-facing close-up portrait of the face,
[2] full-body front view showing the complete outfit,
[3] full-body three-quarter back view.
Character: Middle Eastern man in his early fifties, average height, dignified upright bearing,
olive to light brown skin, dark brown medium-length hair with grey streaks, slightly tousled
but dignified, full well-kept salt-and-pepper beard, calm peaceful eyes, faint serene smile.
Wearing notably clean, well-maintained cream off-white linen robes in first-century
Roman-provincial style, with simple leather sandals.
Neutral standing pose, arms relaxed. Clean sheet layout, no text labels, no props,
no chains, no scenery.
```

### QA Checklist

- [ ] Same face, beard, and robes in all three views
- [ ] Robes read as CLEAN and well-kept — reject dirty, torn, or ragged robes (the model will default to "prisoner = ragged")
- [ ] No chains, shackles, or rope anywhere on the sheet
- [ ] Salt-and-pepper beard consistent across views
- [ ] Face view large and sharp; expression serene, not stern
- [ ] Background solid mid-gray

---

## 4. Pharisee Leader — "The Intense Conspirator"

### Refined Description

- **Age/Build:** Late forties Middle Eastern man, medium build
- **Skin:** Light to medium brown
- **Hair:** Dark, receding, covered by a **tall ornate head wrap** (taller/richer than the crowd's — differentiator #1)
- **Beard:** Full and dark with a **prominent grey streak down the chin** (differentiator #2)
- **Baseline expression:** Intense wide dark eyes, dramatic stern zealotry — depicted WELL-FED (hunger arc is per-shot video direction)
- **Wardrobe:** Dark earth-tone woolen robes, 1st-century Judea, with a **distinct dark-red trim band along the mantle edges** (differentiator #3), mantle with corner tassels (tzitzit) including a blue thread, simple leather sandals
- **Era lock:** Period-plausible — no modern striped tallit, no tefillin

### Image-Generation Prompt

```
Character reference sheet on a solid mid-gray studio background, even soft lighting, photorealistic.
Three views of the same character, consistent across all views:
[1] front-facing close-up portrait of the face,
[2] full-body front view showing the complete outfit,
[3] full-body three-quarter back view.
Character: Middle Eastern man in his late forties, medium build, light to medium brown skin,
dark receding hair covered by a tall ornate dark cloth head wrap, full dark beard with a
prominent grey streak down the chin, intense wide dark eyes, dramatic stern expression.
Wearing dark earth-tone woolen robes in first-century Judean style with a distinct dark-red
trim band along the edges of his mantle, corner tassels with a blue thread on the mantle,
and simple leather sandals.
Neutral standing pose, arms relaxed. Clean sheet layout, no text labels, no props, no scenery.
```

### QA Checklist

- [ ] All three differentiators present in every view: tall head wrap, grey chin streak, red trim band
- [ ] No modern prayer shawl stripes, no tefillin/phylacteries — reject if the model sneaks in modern Orthodox iconography
- [ ] He looks well-fed and vigorous (baseline), not gaunt
- [ ] Same face and robes across views
- [ ] Face view large, sharp; expression intense but not cartoonish
- [ ] Background solid mid-gray

---

## 5. Roman Commander (Claudius Lysias) — "The Disinterested Bureaucrat"

### Refined Description

- **Age/Build:** Mid-forties Roman man, sturdy military build
- **Skin:** Light olive to tan
- **Hair:** Short dark brown, grey at the temples, practical military cut
- **Face:** Clean-shaven, heavy-lidded eyes
- **Baseline expression:** Bored, unimpressed, mildly annoyed
- **Wardrobe (casual armor, concretized):** Roman lorica segmentata plate armor with **no helmet**, **top shoulder buckles undone**, **red tunic sleeves visible** beneath the armor, leather strip skirt (pteruges), Roman military boots. Relaxed stance, weight on one hip
- **Off-sheet (separate props):** Sushi plate, tablet-scroll hybrid, coffee cup — desk dressing for the office location/scenes

### Image-Generation Prompt

```
Character reference sheet on a solid mid-gray studio background, even soft lighting, photorealistic.
Three views of the same character, consistent across all views:
[1] front-facing close-up portrait of the face,
[2] full-body front view showing the complete outfit,
[3] full-body three-quarter back view.
Character: Roman man in his mid-forties, sturdy military build, light olive to tan skin,
short dark brown hair with grey at the temples in a practical military cut, clean-shaven,
heavy-lidded eyes, bored unimpressed expression.
Wearing Roman lorica segmentata plate armor worn casually: no helmet, the top shoulder
buckles undone, red tunic sleeves visible beneath the armor plates, a skirt of leather
strips, and Roman military boots.
Relaxed standing pose with weight on one hip, arms loose. Clean sheet layout, no text labels,
no weapons, no props, no scenery.
```

### QA Checklist

- [ ] Armor reads "off duty": no helmet, undone shoulder buckles visible, tunic sleeves showing
- [ ] No sword, spear, or shield — reject armed versions (models default Romans to battle-ready)
- [ ] Same face and armor detail across views
- [ ] Expression bored/unimpressed, not fierce
- [ ] Face view large and sharp
- [ ] Background solid mid-gray

---

## 6. Angel — "The Heavenly Caddy"

### Refined Description

- **Age/Build:** Ageless, appears mid-thirties, male
- **Skin:** Warm light skin, ethnically ambiguous features — **no baked-in glow** (radiance driven by lighting in video prompts)
- **Hair:** Light brown, shoulder-length, flowing
- **Baseline expression:** Friendly, relaxed, gentle smile
- **Wings:** Large white feathered wings, **folded along the back, wingtips reaching mid-calf**
- **Wardrobe:** Clean flowing white robes, simple modern cut (not theatrical), cream sash, simple sandals
- **Off-sheet (separate props):** Golf clubs, golf ball

### Image-Generation Prompt

```
Character reference sheet on a solid mid-gray studio background, even soft lighting, photorealistic.
Three views of the same character, consistent across all views:
[1] front-facing close-up portrait of the face,
[2] full-body front view showing the complete outfit,
[3] full-body three-quarter back view clearly showing the folded wings from behind.
Character: man of ageless appearance looking mid-thirties, warm light skin with ethnically
ambiguous features, light brown shoulder-length flowing hair, friendly relaxed face with
a gentle smile.
Large white feathered wings folded along his back, wingtips reaching down to mid-calf.
Wearing clean flowing white robes with a simple modern cut, a cream sash at the waist,
and simple sandals.
Natural skin with no glow or luminous effects.
Neutral standing pose, arms relaxed. Clean sheet layout, no text labels, no props,
no halo, no scenery.
```

### QA Checklist

- [ ] 3/4-back view clearly shows both folded wings — reject if wings are cropped, spread wide, or missing from the back view
- [ ] Wingtips reach roughly mid-calf, consistent size across views
- [ ] No glow, halo, light rays, or lens flares — reject any baked-in radiance
- [ ] Same face, hair, and robes across views
- [ ] Robes read modern-clean, not theatrical/baroque
- [ ] Background solid mid-gray

---

## 7. The 40+ Pharisees (Crowd) — "The Hungry Mob"

### Refined Description — Group Asset, 4 Archetypes

One group sheet with four distinct variations (prevents the "army of clones" problem in crowd shots — the video model uses these as a palette):

1. **Young Zealot** — early 30s, tall and lanky, patchy short dark beard, eager forward-leaning posture
2. **Heavyset Elder** — 60s, broad heavyset build, full grey beard, robe straining at the middle
3. **Wiry Schemer** — late 40s, thin wiry build, long narrow face, salt-streaked dark beard
4. **Short Stocky One** — 50s, short round build, thick black beard

**Shared faction markers (constant across all four):** dark earth-tone woolen robes, mantles with corner tassels (tzitzit) with blue thread, simple head wraps, leather sandals. Baseline: well-fed, stern, zealous — hunger/collapse is per-shot direction.

**Off-sheet (separate props):** "No Food Until Paul Dies" banners/signs.

### Image-Generation Prompt

```
Character reference sheet on a solid mid-gray studio background, even soft lighting, photorealistic.
Four distinct variations of first-century Judean Pharisee conspirators standing side by side,
same faction, full-body front views:
[1] a man in his early thirties, tall and lanky, patchy short dark beard, eager
forward-leaning posture;
[2] a man in his sixties, broad heavyset build, full grey beard, robe straining at the middle;
[3] a man in his late forties, thin wiry build, long narrow face, salt-streaked dark beard;
[4] a man in his fifties, short stocky round build, thick black beard.
All four share the same faction dress: dark earth-tone woolen robes in first-century Judean
style, mantles with corner tassels with a blue thread, simple dark cloth head wraps, and
leather sandals. All look well-fed with stern zealous expressions.
Clean sheet layout, no text labels, no props, no scenery.
```

### QA Checklist

- [ ] All four are genuinely distinct at a glance — different heights, builds, beard colors. If any two could be twins, regenerate with stronger stated differences
- [ ] Faction dress is consistent across all four (same robe style, head wraps, tassels)
- [ ] No modern prayer shawls or tefillin
- [ ] All four fully visible head to sandals, none cropped
- [ ] All look well-fed and vigorous (baseline)
- [ ] Background solid mid-gray

---

## Generation & Handoff Workflow

1. **Generate** each sheet from its prompt (batch-generate 2–4 candidates per character — rerolling is cheaper than iterating on a mediocre sheet).
2. **QA** each candidate against its checklist. Reject fast; drifting details poison every downstream shot.
3. **Register** each accepted sheet as a named element (asset librarian) so video prompts can reference it by tag. Suggested names: `tt1_observer`, `tt2_snacker`, `paul`, `pharisee_leader`, `commander_lysias`, `angel_caddy`, `pharisee_mob`.
4. **Prop sheets next:** juice pipe, chips bag, sushi plate, tablet-scroll, golf clubs, banners, chains — separate prop-asset pass.
5. **Location sheets:** Conspiracy Chamber, Commander's Office, Herod's Palace room, Sanhedrin Court.

---

_Refined from the original draft descriptions per locked design decisions — supersedes the character section of the draft asset notes._
