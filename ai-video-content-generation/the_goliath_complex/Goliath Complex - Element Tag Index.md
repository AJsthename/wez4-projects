# The Goliath Complex — Element Tag Index

**Project:** "The Goliath Complex" (Gulayat) — ANN / David & Goliath, 1 Samuel 17
**Purpose:** the master `@tag` map for every asset this project will generate — characters, locations, props, brand/wardrobe, and scale references. Copy a tag from here whenever you generate or reference an asset, so names stay consistent everywhere.
**Scheme (asset-librarian):** tags are lowercase, underscores, short, unique, and **derived once and never changed** — a video prompt references the tag forever, so renaming later silently breaks every prompt already written.

> **Status = `planned`.** Nothing here is finalized yet. When an asset passes its QA checklist and gets registered via the **asset-librarian** skill, its row moves into the live registry with a real File path and `status: final`. This index is the naming plan.
>
> **Two registries hold the final rows:** episode-native assets (ancient cast, locations, props, scale refs) → [assets/MANIFEST.md](assets/MANIFEST.md); shared ANN assets (crew cast, logo system, wardrobe) → [ANN Franchise - Shared Cast, Brand & Wardrobe.md](../ANN%20Franchise%20-%20Shared%20Cast,%20Brand%20&%20Wardrobe.md). The ANN tags below are listed for planning; they get registered in the franchise file, not this episode's manifest.

---

## Characters — ancient cast

| Element | Tag | Sheet type | Identity anchor (from the Scale Bible) |
|---------|-----|-----------|----------------------------------------|
| David (shepherd) | `@david` | three-view | ~158 cm, youth via build/face not height; rosy, hazel eyes, sheepskin mantle |
| King Saul | `@saul` | three-view | 185 cm, head-and-shoulders above the people; greying beard, kingly-careworn |
| Goliath (Gulayat) | `@goliath` | four-panel (+ helmet inset) | 297 cm, ~2× shoulder width; bronze fish-scale armor, full dark beard |
| Goliath's shield-bearer | `@shield_bearer` | three-view | 165 cm, sturdy; dwarfed by Goliath; carries the tower shield |
| Jesse | `@jesse` | three-view | 164 cm, elderly dignified father, grey beard, robes |
| Eliab (eldest brother) | `@eliab` | three-view | 170 cm, tall soldierly proud bearing |
| Abinadab (brother) | `@abinadab` | three-view | 166 cm, soldierly |
| Shammah (brother) | `@shammah` | three-view | 165 cm, soldierly |
| Saul's counsellors (×3) | `@saul_counsellors` | 3-variation group sheet | older, robes over armor, three distinct faces/beards |
| Funny soldier #1 (lanky) | `@funny_soldier_1` | three-view · **locked cameo** | long neck, hooked nose, wild brows, gap-toothed, oversized slipping helmet |
| Funny soldier #2 (stout) | `@funny_soldier_2` | three-view · **locked cameo** | short & stout, round ruddy face, bushy mustache/unibrow, dented helmet |
| Israelite soldier #1 | `@israelite_soldier_1` | three-view | distinct named face, Israelite military attire |
| Israelite soldier #2 | `@israelite_soldier_2` | three-view | distinct named face, Israelite military attire |
| Israelite soldiers (crowd) | `@israelite_soldiers` | 3–4 variation group sheet | fearful baseline; vary faces/builds so no clones |
| Philistine soldiers (crowd) | `@philistine_soldiers` | 3–4 variation group sheet | foreign warrior gear, distinct from Israelites |
| Average soldier (scale base) | `@avg_soldier` | three-view | ×1.00 base unit; the yardstick for the Cast Scale Lineup |

## Characters — modern ANN cast

| Element | Tag | Sheet type | Identity anchor |
|---------|-----|-----------|-----------------|
| Chris (ANN reporter) | `@chris` | three-view | young, mid-to-late 20s (max ~30); 176 cm, caucasian; reporter attire, tablet, the two-hour watch |
| Clarissa (ANN reporter) | `@clarissa` | three-view | young, mid-to-late 20s (max ~30); 175 cm, african/ebony; distinctive hair, tablet |
| Mr Tec Nical (ANN cameraman) | `@tec_nical` | three-view | 179 cm, east-asian/indian, bulky; camera-op gear, headcam, backpack |
| Professor Phro Nesis | `@phro_nesis` | three-view | 175 cm, caucasian; lab coat, scientist |
| Doctor Sue Nesis | `@sue_nesis` | three-view | 160 cm, east-asian; lab coat, scientist |
| Mr Kata Lambano | `@kata_lambano` | three-view | 177 cm, bangladeshi; professional attire |
| ANN team (background ensemble) | `@ann_team` | variation group sheet | vary height/build/features so no clones |

> **Wardrobe lock:** every ANN character sheet is dressed in `@ann_jacket` (below), so identity + wardrobe stay locked together.
> **Narrator:** appears to be **voice-only** (no on-screen presence) — no character sheet planned. Flag it if the narrator is ever seen on camera and needs a tag.

---

## Locations

| Element | Tag | Decision |
|---------|-----|----------|
| Valley of Elah — master panorama | `@valley_elah` | GENERATE (make this first; others match its geography/sun) |
| Valley floor / battlefield plain | `@elah_plain` | GENERATE |
| Israel army camp — front & slope | `@israel_camp` | GENERATE |
| King Saul's command tent (interior) | `@saul_tent` | GENERATE |
| ANN observation peak | `@ann_peak` | GENERATE (light) |
| Jesse's homestead — hillside & yard | `@jesse_house` | GENERATE |
| ANN lab + circular portal stage | `@ann_lab` | GENERATE |

---

## Props

| Element | Tag | Note |
|---------|-----|------|
| Goliath's spear | `@goliath_spear` | shaft taller than Saul |
| Goliath's tower shield | `@goliath_shield` | carried by the shield-bearer |
| Goliath's sword | `@goliath_sword` | David draws it two-handed to behead him |
| David's shepherd's staff | `@david_staff` | ≈ David's own height |
| David's sling, pouch & 5 stones | `@david_sling_kit` | hero weapon; slow-mo stone |
| King Saul's royal armor set | `@saul_armor` | swallows David — the comic beat |
| Jesse's provisions | `@jesse_provisions` | light/optional |
| Provisions handcart | `@provisions_cart` | loaded & ridden off |
| ANN camera rig | `@ann_camera` | video camera + zoom mic |
| ANN drones (pair) | `@ann_drones` | modern quadcopters |
| ANN tablet | `@ann_tablet` | abstract UI, no readable text |
| Chris's ANN smartwatch | `@ann_watch` | + red arrow; the two-hour clock |
| ANN incursion artifact | `@ann_artifact` | optional lore object |

---

## Brand & wardrobe (franchise-level — reuse across all ANN episodes)

| Element | Tag | Note |
|---------|-----|------|
| ANN monogram logo | `@ann_logo_monogram` | dark bg; spells exactly "ANN" |
| ANN icon logo | `@ann_logo_icon` | light bg; obelisk + broadcast arcs |
| ANN horizontal lockup | `@ann_logo_lockup` | icon + wordmark + tagline |
| ANN crew jacket | `@ann_jacket` | depends on logos existing first |

---

## Scale references (single-pass lineups — lock relative size)

| Element | Tag | Covers |
|---------|-----|--------|
| Cast scale lineup | `@cast_scale` | avg soldier · David · Saul · Goliath on one ground line |
| David–Goliath lineup | `@david_goliath_scale` | the face-off two-shot proportions |
| Saul-armor / David lineup | `@saul_armor_david_scale` | the oversized-armor "swallows him" gag |

---

## Copy-paste blocks (bare tags)

**All characters (ancient):**
```
@david @saul @goliath @shield_bearer @jesse @eliab @abinadab @shammah @saul_counsellors @funny_soldier_1 @funny_soldier_2 @israelite_soldier_1 @israelite_soldier_2 @israelite_soldiers @philistine_soldiers @avg_soldier
```

**All characters (modern ANN):**
```
@chris @clarissa @tec_nical @phro_nesis @sue_nesis @kata_lambano @ann_team
```

**Locations:**
```
@valley_elah @elah_plain @israel_camp @saul_tent @ann_peak @jesse_house @ann_lab
```

**Props:**
```
@goliath_spear @goliath_shield @goliath_sword @david_staff @david_sling_kit @saul_armor @jesse_provisions @provisions_cart @ann_camera @ann_drones @ann_tablet @ann_watch @ann_artifact
```

**Brand & wardrobe:**
```
@ann_logo_monogram @ann_logo_icon @ann_logo_lockup @ann_jacket
```

**Scale references:**
```
@cast_scale @david_goliath_scale @saul_armor_david_scale
```

**Everything (all 50 tags):**
```
@david @saul @goliath @shield_bearer @jesse @eliab @abinadab @shammah @saul_counsellors @funny_soldier_1 @funny_soldier_2 @israelite_soldier_1 @israelite_soldier_2 @israelite_soldiers @philistine_soldiers @avg_soldier @chris @clarissa @tec_nical @phro_nesis @sue_nesis @kata_lambano @ann_team @valley_elah @elah_plain @israel_camp @saul_tent @ann_peak @jesse_house @ann_lab @goliath_spear @goliath_shield @goliath_sword @david_staff @david_sling_kit @saul_armor @jesse_provisions @provisions_cart @ann_camera @ann_drones @ann_tablet @ann_watch @ann_artifact @ann_logo_monogram @ann_logo_icon @ann_logo_lockup @ann_jacket @cast_scale @david_goliath_scale @saul_armor_david_scale
```

---

## Notes & assumptions (change freely)

- **`@david` / `@goliath` / `@saul` / `@avg_soldier`** are the tags already used in the Cast Scale Lineup prompt, so they're canonical. (The character-assets workflow once suggested the longer element name `david_shepherd`; the tag stays `@david`.)
- **Group vs individual sheets:** Saul's counsellors, and both soldier crowds, are planned as single **variation group sheets** (one sheet, 3–4 distinct builds) — not one sheet per extra. `@israelite_soldier_1/2` are the two *named/distinct* Israelites; `@israelite_soldiers` is the background crowd.
- **Funny soldiers are recurring cameos** — their locked signature look goes in the manifest's Critical details exactly like a lead's, so they stay identical across every ANN episode.
- **ANN brand/wardrobe + cameo signatures are franchise-level** — reuse the same tags in future ANN projects rather than minting new ones.
- **Optional/light assets** (`@jesse_provisions`, `@ann_artifact`, `@ann_peak`) may be dropped to inline descriptions if they don't earn screen time — keep the tag reserved either way.
