# The Goliath Complex — Element Tag Index

**Project:** "The Goliath Complex" (Gulayat) — ANN / David & Goliath, 1 Samuel 17
**Purpose:** the master `@tag` map for every asset this project needs — characters, locations, props, brand/wardrobe, and scale references. Copy a tag from here whenever you generate or reference an asset, so names stay consistent everywhere.
**Scheme (asset-librarian):** tags are lowercase, underscores, short, unique, and **derived once and never changed** — a video prompt references the tag forever, so renaming later silently breaks every prompt already written.

**Status legend:** ✅ `generated` = the sheet/plate exists and is tagged (registered `final`) · ⬜ `to generate` = outstanding work · 🕓 `deferred` = wanted eventually, consciously postponed · ⛔ = deliberately not produced (skipped or retired), **not** a gap.

> ### Where the project stands — 53 generated, 2 to go
> **Cast, locations, crew and props are all but done.** The only remaining work is **`@saul_armor`** (generations exist, the pick is pending) and **`@saul_armor_david_scale`**, which depends on it. Everything else outstanding is a conscious skip or the deferred franchise pass.
>
> | Group | Generated | Outstanding | Not produced (by choice) |
> |---|---|---|---|
> | Ancient cast | 15 | — | 2 retired |
> | ANN crew | 7 | — | — |
> | Location plates | 17 | — | 4 (1 n/a + 3 skipped) |
> | Props | 12 | **1** — `@saul_armor` (pick pending) | — |
> | Scale references | 2 | **1** — blocked on the armor pick | — |
> | Brand & wardrobe | 0 | — | 4 deferred |
>
> **Both remaining items are one decision.** Pick the Saul-armor generation, register it `final`, then build the `@saul_armor_david_scale` lineup from that accepted set — and the asset phase is complete.

> **Two registries hold the final rows:** episode-native assets (ancient cast, locations, props, scale refs) → [assets/MANIFEST.md](assets/MANIFEST.md); shared ANN assets (crew cast, logo system, wardrobe) → [ANN Franchise - Shared Cast, Brand & Wardrobe.md](../ANN%20Franchise%20-%20Shared%20Cast,%20Brand%20&%20Wardrobe.md). The ANN tags below are listed for planning; they get registered in the franchise file, not this episode's manifest.

---

## ⚠️ Tag corrections — read before writing any prompt

Five tags on the generated assets differ from what this index originally planned. **The generated asset is the reality, so the real tag wins** and this index now records it. This was free to fix because no Seedance video prompt has been written yet — once prompts exist, a rename breaks every one of them.

| Originally planned | Actual tag on the asset | Action |
|---|---|---|
| `@saul_counsellors` | **`@saul_council`** | adopted — use `@saul_council` everywhere |
| `@israelite_soldiers` | **`@israelite_army`** | adopted — use `@israelite_army` everywhere |
| `@philistine_soldiers` | **`@philistine_army`** | adopted — use `@philistine_army` everywhere |
| `@elah_plain` | **`@valley_plain`** | adopted — the plain is `@valley_plain_*` in all views |
| `@ann_artifact` | **`@ann_artifacts`** | adopted (plural) — use `@ann_artifacts` everywhere |
| *(unplanned)* | **`@general`** | new element, now registered below |

**Two tags need normalising — please fix these at the source:** `@valley_elah_3QF` and `@valley_plain_3QF` carry an uppercase `3QF` where every other plate uses lowercase `3qf`. Tag matching may be case-sensitive, and a near-miss tag silently fails to attach its reference. Re-label those two assets to `@valley_elah_3qf` and `@valley_plain_3qf`; they are recorded in lowercase below on the assumption you will.

**One tag needs confirming:** the bare `@valley_elah` — the plate count implies it is the master panorama's **top-down**. If so, re-label it `@valley_elah_cctv` to match the scheme. If it is instead a legacy single plate from before the three-view standard, say so and it gets retired.

---

## Characters — ancient cast

| Element | Tag | Sheet type | Identity anchor (from the Scale Bible) | Status |
|---------|-----|-----------|----------------------------------------|--------|
| David (shepherd) | `@david` | three-view | ~158 cm, youth via build/face not height; rosy, hazel eyes, sheepskin mantle | ✅ generated |
| King Saul | `@saul` | three-view | 185 cm, head-and-shoulders above the people; greying beard, kingly-careworn | ✅ generated |
| Goliath (Gulayat) | `@goliath` | four-panel (+ helmet inset) | 297 cm, ~2× shoulder width; bronze fish-scale armor, full dark beard | ✅ generated |
| Goliath's shield-bearer | `@shield_bearer` | three-view | 165 cm, sturdy; dwarfed by Goliath; carries the tower shield | ✅ generated |
| Jesse | `@jesse` | three-view | 164 cm, elderly dignified father, grey beard, robes | ✅ generated |
| Eliab (eldest brother) | `@eliab` | three-view | 170 cm, tall soldierly proud bearing | ✅ generated |
| Abinadab (brother) | `@abinadab` | three-view | 166 cm, soldierly | ✅ generated |
| Shammah (brother) | `@shammah` | three-view | 165 cm, soldierly | ✅ generated |
| Saul's council (×3) | `@saul_council` | 3-variation group sheet | older, robes over armor, three distinct faces/beards | ✅ generated |
| Saul's general | `@general` | three-view | senior commander at Saul's side in the command tent; ranks above the council's advisers | ✅ generated |
| Funny soldier #1 (lanky) | `@funny_soldier_1` | three-view · **locked cameo** | long neck, hooked nose, wild brows, gap-toothed, oversized slipping helmet | ✅ generated |
| Funny soldier #2 (stout) | `@funny_soldier_2` | three-view · **locked cameo** | short & stout, round ruddy face, bushy mustache/unibrow, dented helmet | ✅ generated |
| Israelite army (crowd) | `@israelite_army` | 3–4 variation group sheet | fearful baseline; vary faces/builds so no clones | ✅ generated |
| Philistine army (crowd) | `@philistine_army` | 3–4 variation group sheet | foreign warrior gear, distinct from Israelites | ✅ generated |
| Average soldier (scale base) | `@avg_soldier` | three-view | ×1.00 base unit; the yardstick for the Cast Scale Lineup | ✅ generated |
| Israelite soldier #1 | `@israelite_soldier_1` | — | *(never produced)* | ⛔ **retired — not needed** |
| Israelite soldier #2 | `@israelite_soldier_2` | — | *(never produced)* | ⛔ **retired — not needed** |

> **The two named-Israelite tags are retired.** The speaking Israelites are cast from a **mixture of `@avg_soldier`, `@funny_soldier_1` and `@funny_soldier_2`** instead — three sheets already generated, which between them cover a straight soldier and two locked comic faces. Dedicated `@israelite_soldier_1/2` sheets would only add two more faces to keep consistent for no gain. The tags stay listed and reserved so nobody re-mints them for something else.

**The ancient cast is complete — nothing left to generate.**

## Characters — modern ANN cast (franchise)

| Element | Tag | Sheet type | Identity anchor | Status |
|---------|-----|-----------|-----------------|--------|
| Chris (ANN reporter) | `@chris` | three-view | young, mid-to-late 20s (max ~30); 176 cm, caucasian; reporter attire, tablet, the two-hour watch | ✅ generated |
| Clarissa (ANN reporter) | `@clarissa` | three-view | young, mid-to-late 20s (max ~30); 175 cm, african/ebony; distinctive hair, tablet | ✅ generated |
| Mr Tec Nical (ANN cameraman) | `@tec_nical` | three-view | 179 cm, east-asian/indian, bulky; camera-op gear, headcam, backpack | ✅ generated |
| Professor Phro Nesis | `@phro_nesis` | three-view | 175 cm, caucasian; lab coat, scientist | ✅ generated |
| Doctor Sue Nesis | `@sue_nesis` | three-view | 160 cm, east-asian; lab coat, scientist | ✅ generated |
| Mr Kata Lambano | `@kata_lambano` | three-view | 177 cm, bangladeshi; professional attire | ✅ generated |
| ANN team (background ensemble) | `@ann_team` | variation group sheet | vary height/build/features so no clones | ✅ generated |

> **Narrator:** appears to be **voice-only** (no on-screen presence) — no character sheet planned. Flag it if the narrator is ever seen on camera and needs a tag.

---

## Locations

Every location ships up to **three plates**, each its own tag and its own manifest row: **`_3qf`** (three-quarter front), **`_3qb`** (three-quarter back), **`_cctv`** (overhead top-down). Prompts and QA live in [Goliath Complex - Location Assets_ Descriptions & Prompts.md](Goliath%20Complex%20-%20Location%20Assets_%20Descriptions%20&%20Prompts.md).

| Location | `_3qf` front | `_3qb` back | `_cctv` top-down |
|----------|--------------|-------------|------------------|
| Valley of Elah — master panorama | `@valley_elah_3qf` ✅ | ⛔ **n/a** — a 180° reverse would flip Israel/Philistine to the wrong sides and break the left/right convention every other location inherits (§1) | `@valley_elah_cctv` ✅ *(currently tagged bare `@valley_elah` — confirm & re-label)* |
| Valley floor / battlefield plain | `@valley_plain_3qf` ✅ | ⛔ **skipped by choice** | `@valley_plain_cctv` ✅ |
| Israel army camp — front & slope | `@israel_camp_3qf` ✅ | `@israel_camp_3qb` ✅ | `@israel_camp_cctv` ✅ |
| King Saul's command tent (interior) | `@saul_tent_3qf` ✅ | ⛔ **skipped by choice** | `@saul_tent_cctv` ✅ |
| ANN observation peak | `@ann_peak_3qf` ✅ | `@ann_peak_3qb` ✅ | `@ann_peak_cctv` ✅ |
| Jesse's homestead — hillside & yard | `@jesse_house_3qf` ✅ | `@jesse_house_3qb` ✅ | ⛔ **skipped by choice** |
| ANN lab + circular portal stage | `@ann_lab_3qf` ✅ | `@ann_lab_3qb` ✅ | `@ann_lab_cctv` ✅ |

**Locations are complete — all 17 wanted plates exist.** Three further plates (`@valley_plain_3qb`, `@saul_tent_3qb`, `@jesse_house_cctv`) were **consciously skipped**: the standard is "up to three views", not three views mandatory, and each location already has the coverage its scenes need. Their prompts stay written in §2B, §4B and §6C of the location-assets file, so any of the three can be produced later without re-deriving anything — but none is outstanding work.

---

## Props

| Element | Tag | Note | Status |
|---------|-----|------|--------|
| Goliath's spear | `@goliath_spear` | shaft taller than Saul | ✅ generated |
| Goliath's tower shield | `@goliath_shield` | carried by the shield-bearer | ✅ generated |
| Goliath's sword | `@goliath_sword` | David draws it two-handed to behead him | ✅ generated |
| David's shepherd's staff | `@david_staff` | ≈ David's own height | ✅ generated |
| David's sling, pouch & 5 stones | `@david_sling_kit` | hero weapon; slow-mo stone | ✅ generated |
| Jesse's provisions | `@jesse_provisions` | grain basket, loaves, cheeses | ✅ generated |
| Provisions handcart | `@provisions_cart` | loaded & ridden off | ✅ generated |
| ANN camera rig | `@ann_camera` | video camera + zoom mic | ✅ generated |
| ANN drones (pair) | `@ann_drones` | modern quadcopters | ✅ generated |
| ANN tablet | `@ann_tablet` | abstract UI, no readable text | ✅ generated |
| Chris's ANN smartwatch | `@ann_watch` | + red arrow; the two-hour clock | ✅ generated |
| ANN incursion artifact | `@ann_artifacts` | lore object. **Tag was planned singular (`@ann_artifact`) — the generated asset's plural tag wins** | ✅ generated |
| King Saul's royal armor set | `@saul_armor` | swallows David — the comic beat | ⬜ **pending pick** — generations exist, the accepted one is not yet chosen |

> **`@saul_armor` is the last blocker, and it blocks two things.** Until a generation is picked and registered `final`, the armor cannot be referenced *and* `@saul_armor_david_scale` cannot be built — the lineup's whole job is showing that specific armor swallowing David, so it has to be made from the accepted set. Picking the armor unblocks both remaining assets at once.

---

## Brand & wardrobe (franchise-level — reuse across all ANN episodes)

| Element | Tag | Note | Status |
|---------|-----|------|--------|
| ANN monogram logo | `@ann_logo_monogram` | dark bg; spells exactly "ANN" | 🕓 deferred |
| ANN icon logo | `@ann_logo_icon` | light bg; obelisk + broadcast arcs | 🕓 deferred |
| ANN horizontal lockup | `@ann_logo_lockup` | icon + wordmark + tagline | 🕓 deferred |
| ANN crew jacket | `@ann_jacket` | one master design, fit scales per wearer | 🕓 deferred |

> **Deferred by decision — crew wardrobe currently lives in the prompt text.** The plan had logos → jacket → cast, with every crew sheet generated wearing an accepted `@ann_jacket`. In practice the seven crew sheets came first and carry their wardrobe **described inline in their prompts**, which is enough to keep this episode consistent.
>
> These four stay reserved for a later pass. The thing to know when that pass happens: the crew sheets are already generated, so the jacket asset should be built **to match what those sheets show**, not to define something new — otherwise the wardrobe drifts between the sheets you have and the jacket you make. Capture the jacket's real look off the accepted sheets when you get to it.

---

## Scale references (single-pass lineups — lock relative size)

| Element | Tag | Covers | Status |
|---------|-----|--------|--------|
| Cast scale lineup | `@cast_scale` | avg soldier · David · Saul · Goliath on one ground line | ✅ generated |
| David–Goliath lineup | `@david_goliath_scale` | the face-off two-shot proportions | ✅ generated |
| Saul-armor / David lineup | `@saul_armor_david_scale` | the oversized-armor "swallows him" gag | ⬜ **blocked** — needs the accepted `@saul_armor` first |

---

## Copy-paste blocks (bare tags)

**Ancient characters — generated (15):**
```
@david @saul @goliath @shield_bearer @jesse @eliab @abinadab @shammah @saul_council @general @funny_soldier_1 @funny_soldier_2 @israelite_army @philistine_army @avg_soldier
```

**ANN crew — generated (7):**
```
@chris @clarissa @tec_nical @phro_nesis @sue_nesis @kata_lambano @ann_team
```

**Locations — generated (17 plates):**
```
@valley_elah_3qf @valley_elah_cctv @valley_plain_3qf @valley_plain_cctv @israel_camp_3qf @israel_camp_3qb @israel_camp_cctv @saul_tent_3qf @saul_tent_cctv @ann_peak_3qf @ann_peak_3qb @ann_peak_cctv @jesse_house_3qf @jesse_house_3qb @ann_lab_3qf @ann_lab_3qb @ann_lab_cctv
```

**Props — generated (12):**
```
@goliath_spear @goliath_shield @goliath_sword @david_staff @david_sling_kit @jesse_provisions @provisions_cart @ann_camera @ann_drones @ann_tablet @ann_watch @ann_artifacts
```

**Scale references — generated (2):**
```
@cast_scale @david_goliath_scale
```

**Everything generated so far (53 tags) — safe to reference in prompts:**
```
@david @saul @goliath @shield_bearer @jesse @eliab @abinadab @shammah @saul_council @general @funny_soldier_1 @funny_soldier_2 @israelite_army @philistine_army @avg_soldier @chris @clarissa @tec_nical @phro_nesis @sue_nesis @kata_lambano @ann_team @valley_elah_3qf @valley_elah_cctv @valley_plain_3qf @valley_plain_cctv @israel_camp_3qf @israel_camp_3qb @israel_camp_cctv @saul_tent_3qf @saul_tent_cctv @ann_peak_3qf @ann_peak_3qb @ann_peak_cctv @jesse_house_3qf @jesse_house_3qb @ann_lab_3qf @ann_lab_3qb @ann_lab_cctv @goliath_spear @goliath_shield @goliath_sword @david_staff @david_sling_kit @jesse_provisions @provisions_cart @ann_camera @ann_drones @ann_tablet @ann_watch @ann_artifacts @cast_scale @david_goliath_scale
```

**Still to produce (2 tags) — do NOT reference until final:**
```
@saul_armor @saul_armor_david_scale
```

**Reserved but not being produced (9 tags)** — retired, skipped, or deferred. Listed so nobody re-mints these names for something else:
```
@israelite_soldier_1 @israelite_soldier_2 @valley_plain_3qb @saul_tent_3qb @jesse_house_cctv @ann_logo_monogram @ann_logo_icon @ann_logo_lockup @ann_jacket
```

---

## Notes & assumptions (change freely)

- **`@david` / `@goliath` / `@saul` / `@avg_soldier`** are the tags used in the Cast Scale Lineup prompt, so they're canonical.
- **Group vs individual sheets:** Saul's council and both army crowds are single **variation group sheets** (one sheet, 3–4 distinct builds) — not one sheet per extra.
- **Funny soldiers are recurring cameos** — their locked signature look lives in the manifest's Critical details exactly like a lead's, so they stay identical across every ANN episode.
- **ANN brand/wardrobe + cameo signatures are franchise-level** — reuse the same tags in future ANN projects rather than minting new ones.
- **Optional/light assets** (`@jesse_provisions`, `@ann_artifact`) may be dropped to inline descriptions if they don't earn screen time — keep the tag reserved either way.
- **`@general` was generated without a planning row** — its identity anchor above is inferred from the command-tent scenes (Saul holds court with counsellors *and* generals). Correct the description if the character is something else.
- **Named Israelite soldiers are cast, not generated.** `@avg_soldier` + `@funny_soldier_1` + `@funny_soldier_2` cover every speaking-soldier need between them. Fewer sheets is fewer faces to keep consistent — the retirement is a win, not a shortcut.
- **Skipped location plates are decisions, not debt.** The three-view scheme is *up to* three; a plate earns its place only if a scene needs that angle. `@valley_plain_3qb`, `@saul_tent_3qb` and `@jesse_house_cctv` have finished prompts on file if that ever changes.
