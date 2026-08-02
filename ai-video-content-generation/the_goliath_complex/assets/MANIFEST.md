# Asset Manifest — The Goliath Complex (Gulayat)

The live element registry for this episode (1 Samuel 17 / ANN). One manifest per video project. Managed via the **asset-librarian** skill.

**How to read status:** `draft` = named/planned, not yet generated or not yet QA-passed — **do not reference in video prompts yet**. `final` = generated, tagged and QA-passed, safe to `@tag`. `retired` = superseded (note the replacement).

> ### ⚠️ Archival gap — 53 assets are generated, 4 are filed
> Every row marked `final` below exists and is tagged **in the generation platform**, so its `@tag` resolves there. But only four images have actually been saved into this repo: `@david`, `@saul`, `@goliath`, `@avg_soldier`. The rest show `— not filed` in the File column.
>
> This is the exact failure the librarian exists to prevent: a tag that only lives inside a generation tool is one account change, one expired session, or one cleared history away from being lost, and there is no way to re-create an accepted sheet exactly. **Export the remaining 49 and file them** under the folders below, then fill in the File column. Until then treat those rows as referenceable but *unbacked*.
>
> The gap grows with every generation session and never shrinks on its own — and it is about to matter more, because Seedance prompt-writing is the next phase and every prompt will lean on these tags.

**Folder convention (as actually used):** `assets/character_assets/` · `assets/location_assets/` · `assets/prop_assets/` · `assets/scale_assets/`. Filenames carry the tag (`@david.png`); original inspiration images live in `og_refs/` and are **not** elements.

> **Franchise assets are NOT registered here.** The ANN cast, logo system, and crew wardrobe are franchise-level and shared across every ANN episode — their source-of-truth registry is [ANN Franchise - Shared Cast, Brand & Wardrobe.md](../../ANN%20Franchise%20-%20Shared%20Cast,%20Brand%20&%20Wardrobe.md). This episode *uses* them; see the "Franchise assets used" section at the bottom.

Naming plan, status board and copy-paste tag blocks: [Goliath Complex - Element Tag Index.md](../Goliath%20Complex%20-%20Element%20Tag%20Index.md).

---

## Characters

| Element | Tag | File | Scale | Critical details | Status |
|---------|-----|------|-------|------------------|--------|
| David (shepherd) | `@david` | `character_assets/@david.png` | 0.99× base; crown ≈ Saul's chin, ≈ Goliath's navel | youth reads via build/face **not height**; sun-bronzed ruddy flush, reddish-auburn shoulder-length waves, bright hazel eyes, undyed shepherd's tunic, sheepskin mantle over one shoulder, **no armor** | final |
| King Saul | `@saul` | `character_assets/@saul.png` | 1.16× base; ~a head above soldiers; crown ≈ Goliath's mid-chest | tall broad-shouldered, careworn; short greying hair + full salt-and-pepper beard; **gold diadem band w/ central rosette medallion**; bronze fish-scale armor under a **deep-purple mantle with a crimson-red border** (worn regalia — the set he gives David is the separate `@saul_armor`) | final |
| Goliath (Gulayat) | `@goliath` | `character_assets/@goliath.png` | 1.86× base; **~2× shoulder width**; David's crown ≈ his navel, Saul's crown ≈ his mid-chest | colossal mass (mass, not just height); coppery-bronze fish-scale lamellar cuirass, bronze pauldrons w/ central boss, engraved vambraces, greaves; heavy brow, thick dark beard; domed bronze helmet (flies off Clip 89) | final |
| Average soldier (scale base) | `@avg_soldier` | `character_assets/@avg_soldier.png` | **×1.00 (base unit)** | the yardstick for the Cast Scale Lineup; generic build | final |
| Goliath's shield-bearer | `@shield_bearer` | — not filed | 1.03× base; crown ≈ just above Goliath's waist | broad thick-set strongman at ordinary height (bears the tower shield); **Philistine faction** — banded bronze corselet, bronze cap w/ short feather crest, bronze/slate/teal/oxblood palette; hard watchful subordinate; the shield he carries is the separate prop `@goliath_shield` | final |
| Jesse | `@jesse` | — not filed | 1.03× base | elderly village patriarch (60s–70s), long grey-white beard, thin grey hair under a striped head-wrap; layered earth-tone robes + ochre mantle + sash; warm wise paternal baseline; not a soldier | final |
| Eliab (eldest brother) | `@eliab` | — not filed | 1.06× base; taller than avg soldier, shorter than Saul; David's crown ≈ Eliab's chin | tall broad handsome man-at-arms; short dark hair, full dark beard, family resemblance to David; proud-stern faint disdain; well-equipped Israelite kit (leather + bronze-scale cuirass, blue-thread tassel). **Guard:** his "head and shoulders below us all" jibe is insult, **not** a scale directive — David stays ~avg height | final |
| Abinadab (brother) | `@abinadab` | — not filed | 1.04× base | sturdy solid line-soldier, broad/slightly stocky; short dark hair, full rough dark beard, broad square-jawed honest face; family resemblance to David/Eliab; standard Israelite kit (blue-thread tassel); distinct from tall-proud Eliab & lean Shammah | final |
| Shammah (brother) | `@shammah` | — not filed | 1.03× base | lean/wiry, slightly younger-looking (still a bearded adult); short dark hair, shorter neat dark beard, wary alert face; family resemblance to David/brothers; lightly-equipped Israelite kit (blue-thread tassel); distinct from Eliab & Abinadab | final |
| Saul's council (×3) | `@saul_council` | — not filed | 0.98–1.01× base | one group sheet — 3 distinct older faces/beards, robes over armor, rank indicators. **Tag was planned as `@saul_counsellors`; the generated asset's tag wins** | final |
| Saul's general | `@general` | — not filed | *(unrecorded — measure against `@avg_soldier`)* | senior commander at Saul's side in the command tent; ranks above the council's advisers. **Generated without a planning row — verify this description against the sheet and fill in Scale** | final |
| Funny soldier #1 (lanky) | `@funny_soldier_1` | — not filed | 1.01× base | **LOCKED CAMEO** — long neck, prominent hooked nose, wild expressive brows, gap-toothed grin, oversized helmet that keeps slipping | final |
| Funny soldier #2 (stout) | `@funny_soldier_2` | — not filed | 0.98× base | **LOCKED CAMEO** — short & stout, round ruddy face, huge bushy mustache/unibrow, permanently dented helmet (foil to #1) | final |
| Israelite army (crowd) | `@israelite_army` | — not filed | 0.98–1.01× base | group sheet, 3–4 variations, fearful baseline, vary faces/builds. **Tag was planned as `@israelite_soldiers`** | final |
| Philistine army (crowd) | `@philistine_army` | — not filed | 1.00–1.03× base | group sheet, 3–4 variations, foreign warrior gear (distinct from Israelites). **Tag was planned as `@philistine_soldiers`** | final |
| Israelite soldier #1 | `@israelite_soldier_1` | — | — | **retired before generation** — speaking Israelites are cast from a mixture of `@avg_soldier`, `@funny_soldier_1` and `@funny_soldier_2`. Tag reserved so it is never re-minted | retired |
| Israelite soldier #2 | `@israelite_soldier_2` | — | — | **retired before generation** — same as #1 | retired |

**The cast is complete.** For any scene needing named/speaking Israelites, mix `@avg_soldier` (the straight soldier) with `@funny_soldier_1` and `@funny_soldier_2` (the two locked comic faces) rather than minting new faces to keep consistent.

## Locations

Each location ships **up to** three plates — **`_3qf`** (three-quarter front), **`_3qb`** (three-quarter back), **`_cctv`** (overhead top-down) — and each plate is its own row, because each is a distinct reference a prompt attaches on its own. Prompts and per-plate QA: [Goliath Complex - Location Assets_ Descriptions & Prompts.md](../Goliath%20Complex%20-%20Location%20Assets_%20Descriptions%20&%20Prompts.md).

**All 17 wanted plates exist — locations are complete.** Four possible plates are marked `n/a`: one that would break the film's left/right convention, and three skipped because the location's scenes don't need that angle. A written prompt stays on file for each skipped plate, so producing one later costs a generation, not a re-derivation.

| Element | Tag | File | Critical details | Status |
|---------|-----|------|------------------|--------|
| Valley of Elah — front | `@valley_elah_3qf` | — not filed | two facing mountains + valley floor; **left green/treed w/ tent camp, right barren rocky**; stream on floor; sun high-left. The master orientation every other location obeys. **Re-label from `@valley_elah_3QF` (lowercase)** | final |
| Valley of Elah — back | — | — | ⛔ **deliberately not produced** — a 180° reverse would flip Israel/Philistine to the wrong sides and break the left/right convention | n/a |
| Valley of Elah — top-down | `@valley_elah_cctv` | — not filed | whole basin as a map; ridgelines/tent tops overhead; same sun as the front plate. **Currently tagged bare `@valley_elah` — confirm this is the top-down and re-label** | final |
| Valley plain — front | `@valley_plain_3qf` | — not filed | open central ground for two-shots; both slopes visible in bg; pebbled stream bank near-left edge; heat shimmer 30%. **Re-label from `@valley_plain_3QF` (lowercase)** | final |
| Valley plain — back | `@valley_plain_3qb` | — | **skipped by choice** — the front and top-down cover the plain's scenes; prompt stays on file at §2B if a reverse is ever needed | n/a |
| Valley plain — top-down | `@valley_plain_cctv` | — not filed | clearing as a map; cracked earth, stones, stream from overhead; open centre | final |
| Israel camp — front | `@israel_camp_3qf` | — not filed | cleared front edge overlooking valley + tents behind; 3/4 slope depth; racks/banners/fire rings grounded | final |
| Israel camp — back | `@israel_camp_3qb` | — not filed | from the front edge looking back up-slope into the camp; sun screen-flipped to the right | final |
| Israel camp — top-down | `@israel_camp_cctv` | — not filed | tent rows + cleared front edge as a map | final |
| Saul's tent — front | `@saul_tent_3qf` | — not filed | 3/4 interior; dais throne far-left, map table right, **armor stand right of centre near entrance** (sets up Clip 79–80 gag), **large deep-red carpet covers centre floor**, open flap far wall shows valley | final |
| Saul's tent — back | `@saul_tent_3qb` | — | **skipped by choice** — the front and top-down cover the tent's staging; prompt stays on file at §4B if a reverse is ever needed | n/a |
| Saul's tent — top-down | `@saul_tent_cctv` | — not filed | roof omitted; throne, dais, table, armor stand + central carpet as a floor map | final |
| ANN peak — front | `@ann_peak_3qf` | — not filed | standing outcrop foreground + valley visible far below; reads higher than the valley geography | final |
| ANN peak — back | `@ann_peak_3qb` | — not filed | outcrop mid-ground, mountain slope behind, valley behind camera | final |
| ANN peak — top-down | `@ann_peak_cctv` | — not filed | flat standing area + the drop-off edge, read as a map | final |
| Jesse's homestead — front | `@jesse_house_3qf` | — not filed | house + yard w/ **provisions table against the wall** + pasture slope below; 3/4 angle; morning sun low-**right**; pastoral green vs the arid valley | final |
| Jesse's homestead — back | `@jesse_house_3qb` | — not filed | **the up-slope rear wall** — high window openings, exterior stone stair to the roof, jars & firewood at the base; doorway/yard/table hidden behind the building; morning sun low-**left** | final |
| Jesse's homestead — top-down | `@jesse_house_cctv` | — | **skipped by choice** — the front and back plates cover the homestead's scenes; prompt stays on file at §6C (references both accepted plates) if a map view is ever needed | n/a |
| ANN lab — front | `@ann_lab_3qf` | — not filed | central circular stage ringed by **4 inward laser emitters**; workstations left wall, instruments right; brand-neutral screens, **no readable text** | final |
| ANN lab — back | `@ann_lab_3qb` | — not filed | from the doorway side looking back; workstations mirrored to the right wall, instruments left | final |
| ANN lab — top-down | `@ann_lab_cctv` | — not filed | ceiling omitted; stage, 4 emitters, workstations as a floor map | final |

## Props

**12 of 13 generated.** Only `@saul_armor` remains — generations exist, the accepted one is not yet picked.

| Element | Tag | File | Scale | Critical details | Status |
|---------|-----|------|-------|------------------|--------|
| Goliath's spear | `@goliath_spear` | — not filed | shaft **taller than Saul** | weaver's-beam thick dark hardwood shaft, massive leaf-shaped iron head, iron butt-spike | final |
| Goliath's tower shield | `@goliath_shield` | — not filed | covers a grown man shin-to-shoulder | carried by the shield-bearer; bronze face + domed central boss; strap & grip on the back | final |
| Goliath's sword | `@goliath_sword` | — not filed | so large David needs **both hands**, nearly his own height | broad straight double-edged dark iron blade, bronze crossguard & pommel; David draws it in Clip 91 | final |
| David's shepherd's staff | `@david_staff` | — not filed | ≈ **David's own height** when planted | humble worn crooked hardwood, hooked/knobbed top, hand-worn grip patch ("a stick" gag) | final |
| David's sling, pouch & 5 stones | `@david_sling_kit` | — not filed | sling hand-length; stones **fist-sized** | two-cord leather shepherd's sling, leather drawstring pouch, 5 smooth grey-tan river stones; hero slow-mo stone (Clip 89) | final |
| Jesse's provisions | `@jesse_provisions` | — not filed | loaves/cheeses **hand-sized**; basket two-handed | grain basket, 10 rustic flat loaves, 10 pale cheeses | final |
| Provisions handcart | `@provisions_cart` | — not filed | waist-high | simple two-wheel wooden handcart, plank bed, pull handles | final |
| ANN camera rig | `@ann_camera` | — not filed | shoulder-held; mic ~a forearm | matte-black modern video camera + shotgun zoom mic; **brand-neutral, no logos** | final |
| ANN drones (pair) | `@ann_drones` | — not filed | two-hand carry each | matte-grey modern quadcopters, gimbal cam; **brand-neutral, no text** | final |
| ANN tablet | `@ann_tablet` | — not filed | hand-held | modern glass/aluminium slate; abstract blue UI, **no readable text**, brand-neutral | final |
| Chris's ANN smartwatch | `@ann_watch` | — not filed | wrist-sized | modern smartwatch + **red arrow on the face**; abstract countdown ring (no text); the two-hour incursion clock | final |
| ANN incursion artifact | `@ann_artifacts` | — not filed | two-hand held | ancient stone-and-bronze device, faint blue seam-glow, unreadable glyphs. **Tag was planned singular (`@ann_artifact`); the generated asset's plural tag wins** | final |
| King Saul's royal armor set | `@saul_armor` | — | sized for **185 cm king**; swallows 158 cm David | bronze scale-and-chain breastplate, domed helmet, gilded sword; the "swallows him" gag (Clip 80). **Generations exist — accepted one not yet picked** | draft |

## Scale references

| Element | Tag | File | Covers | Status |
|---------|-----|------|--------|--------|
| Cast scale lineup | `@cast_scale` | — not filed | `@avg_soldier`, `@david`, `@saul`, `@goliath` — all principals on one ground line | final |
| David–Goliath lineup | `@david_goliath_scale` | — not filed | the face-off two-shot proportions | final |
| Saul-armor / David lineup | `@saul_armor_david_scale` | — | the oversized-armor "swallows him" gag. **Blocked on `@saul_armor`** — the lineup must be built from the *accepted* armor set, or the gag's proportions won't match the prop used in the shots | draft |

---

## Franchise assets used (shared — registered elsewhere)

These recur across every ANN episode; their canonical rows and accepted files live in [ANN Franchise - Shared Cast, Brand & Wardrobe.md](../../ANN%20Franchise%20-%20Shared%20Cast,%20Brand%20&%20Wardrobe.md). Referenced here only so this episode's full inventory is visible — **do not duplicate their File paths here; read them from the franchise file.**

- **ANN crew (cast):** `@chris` · `@clarissa` · `@tec_nical` · `@phro_nesis` · `@sue_nesis` · `@kata_lambano` · `@ann_team` — **all seven generated and `final`.**
- **ANN brand & wardrobe:** `@ann_logo_monogram` · `@ann_logo_icon` · `@ann_logo_lockup` · `@ann_jacket` — **deferred by decision.** Crew wardrobe currently lives in the crew sheets' own prompt text, which holds this episode together fine. When the franchise pass happens, build the jacket to *match* the accepted crew sheets rather than to define something new.

---

## Registration rules (reminder)

1. Register at **finalization**, not before — `draft` → `final` only after the asset's QA checklist passes.
2. **One element, one tag, forever.** To revise an asset, add a new versioned File (`@david_v2.png`) and update the File column — the tag never changes. *(The five tag corrections recorded in the Tag Index were made while zero video prompts existed, which is the only moment a rename is free.)*
3. Fill **Critical details** and **Scale** at registration time — verify the pre-filled text against the accepted image.
4. Annotated variants (e.g. a red-arrow prop) and **separate camera views of one location** are their own rows, because each is a reference a prompt attaches independently.
5. Keep the manifest sorted and clean — it's read far more than it's written.
