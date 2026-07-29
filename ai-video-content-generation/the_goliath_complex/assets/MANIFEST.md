# Asset Manifest — The Goliath Complex (Gulayat)

The live element registry for this episode (1 Samuel 17 / ANN). One manifest per video project. Managed via the **asset-librarian** skill.

**How to read status:** `draft` = named/planned, not yet generated or not yet QA-passed — **do not reference in video prompts yet**. `final` = passed its QA checklist, safe to `@tag`. `retired` = superseded (note the replacement).

**On first generation:** when an asset passes QA, set its **File** to the accepted image path (keep files under `assets/characters/`, `assets/locations/`, `assets/props/`, `assets/scale/`) and flip **Status** to `final`. Scale and Critical details are pre-filled from the design files so prompt-writers can copy them straight in.

> **Franchise assets are NOT registered here.** The ANN cast, logo system, and crew wardrobe are franchise-level and shared across every ANN episode — their source-of-truth registry is [ANN Franchise - Shared Cast, Brand & Wardrobe.md](../../ANN%20Franchise%20-%20Shared%20Cast,%20Brand%20&%20Wardrobe.md). This episode *uses* them; see the "Franchise assets used" section at the bottom.

Naming plan and copy-paste tag blocks: [Goliath Complex - Element Tag Index.md](../Goliath%20Complex%20-%20Element%20Tag%20Index.md).

---

## Characters

| Element | Tag | File | Scale | Critical details | Status |
|---------|-----|------|-------|------------------|--------|
| David (shepherd) | `@david` | — | 0.99× base; crown ≈ Saul's chin, ≈ Goliath's navel | youth reads via build/face **not height**; sun-bronzed ruddy flush, reddish-auburn shoulder-length waves, bright hazel eyes, undyed shepherd's tunic, sheepskin mantle over one shoulder, **no armor** | draft |
| King Saul | `@saul` | — | 1.16× base; ~a head above soldiers; crown ≈ Goliath's mid-chest | tall broad-shouldered, careworn; short greying hair + full salt-and-pepper beard; **gold diadem band w/ central rosette medallion**; bronze fish-scale armor under a **deep-purple mantle with a crimson-red border** (worn regalia — the set he gives David is the separate `@saul_armor`) | draft |
| Goliath (Gulayat) | `@goliath` | — | 1.86× base; **~2× shoulder width**; David's crown ≈ his navel, Saul's crown ≈ his mid-chest | colossal mass (mass, not just height); coppery-bronze fish-scale lamellar cuirass, bronze pauldrons w/ central boss, engraved vambraces, greaves; heavy brow, thick dark beard; domed bronze helmet (flies off Clip 89) | draft |
| Goliath's shield-bearer | `@shield_bearer` | — | 1.03× base; crown ≈ just above Goliath's waist | broad thick-set strongman at ordinary height (bears the tower shield); **Philistine faction** — banded bronze corselet, bronze cap w/ short feather crest, bronze/slate/teal/oxblood palette; hard watchful subordinate; the shield he carries is the separate prop `@goliath_shield` | draft |
| Jesse | `@jesse` | — | 1.03× base | elderly village patriarch (60s–70s), long grey-white beard, thin grey hair under a striped head-wrap; layered earth-tone robes + ochre mantle + sash; warm wise paternal baseline; not a soldier | draft |
| Eliab (eldest brother) | `@eliab` | — | 1.06× base; taller than avg soldier, shorter than Saul; David's crown ≈ Eliab's chin | tall broad handsome man-at-arms; short dark hair, full dark beard, family resemblance to David; proud-stern faint disdain; well-equipped Israelite kit (leather + bronze-scale cuirass, blue-thread tassel). **Guard:** his "head and shoulders below us all" jibe is insult, **not** a scale directive — David stays ~avg height | draft |
| Abinadab (brother) | `@abinadab` | — | 1.04× base | sturdy solid line-soldier, broad/slightly stocky; short dark hair, full rough dark beard, broad square-jawed honest face; family resemblance to David/Eliab; standard Israelite kit (blue-thread tassel); distinct from tall-proud Eliab & lean Shammah | draft |
| Shammah (brother) | `@shammah` | — | 1.03× base | lean/wiry, slightly younger-looking (still a bearded adult); short dark hair, shorter neat dark beard, wary alert face; family resemblance to David/brothers; lightly-equipped Israelite kit (blue-thread tassel); distinct from Eliab & Abinadab | draft |
| Saul's counsellors (×3) | `@saul_counsellors` | — | 0.98–1.01× base | one group sheet — 3 distinct older faces/beards, robes over armor, rank indicators | draft |
| Funny soldier #1 (lanky) | `@funny_soldier_1` | — | 1.01× base | **LOCKED CAMEO** — long neck, prominent hooked nose, wild expressive brows, gap-toothed grin, oversized helmet that keeps slipping | draft |
| Funny soldier #2 (stout) | `@funny_soldier_2` | — | 0.98× base | **LOCKED CAMEO** — short & stout, round ruddy face, huge bushy mustache/unibrow, permanently dented helmet (foil to #1) | draft |
| Israelite soldier #1 | `@israelite_soldier_1` | — | 0.98–1.01× base | distinct named face, Israelite military attire | draft |
| Israelite soldier #2 | `@israelite_soldier_2` | — | 0.98–1.01× base | distinct named face, Israelite military attire | draft |
| Israelite soldiers (crowd) | `@israelite_soldiers` | — | 0.98–1.01× base | group sheet, 3–4 variations, fearful baseline, vary faces/builds | draft |
| Philistine soldiers (crowd) | `@philistine_soldiers` | — | 1.00–1.03× base | group sheet, 3–4 variations, foreign warrior gear (distinct from Israelites) | draft |
| Average soldier (scale base) | `@avg_soldier` | — | **×1.00 (base unit)** | the yardstick for the Cast Scale Lineup; generic build | draft |

## Locations

| Element | Tag | File | Scale | Critical details | Status |
|---------|-----|------|-------|------------------|--------|
| Valley of Elah — master panorama | `@valley_elah` | — | — | two facing mountains + valley floor; left green/treed w/ tent camp, right barren rocky; stream on floor; sun high-left. **Generate first — others match its geography/sun** | draft |
| Valley floor / battlefield plain | `@elah_plain` | — | — | open central ground for two-shots; both slopes visible in bg; pebbled stream bank near-left edge; heat shimmer 30% | draft |
| Israel army camp — front & slope | `@israel_camp` | — | — | front edge overlooking valley + tents behind; 3/4 angle slope depth; weapon racks/banners/fire rings grounded | draft |
| King Saul's command tent (interior) | `@saul_tent` | — | — | 3/4 interior; dais throne far-left, map table center, **armor stand right wall** (sets up Clip 79–80 gag), open flap far wall shows valley | draft |
| ANN observation peak | `@ann_peak` | — | — | standing outcrop foreground + valley visible far below; reads higher than the valley geography | draft |
| Jesse's homestead — hillside & yard | `@jesse_house` | — | — | house + yard w/ table against the wall + pasture slope below; 3/4 angle; morning light low-right; pastoral green vs arid valley | draft |
| ANN lab + circular portal stage | `@ann_lab` | — | — | central circular stage ringed by 4 inward laser emitters; modern sci-fi; brand-neutral screens, **no readable text** | draft |

## Props

| Element | Tag | File | Scale | Critical details | Status |
|---------|-----|------|-------|------------------|--------|
| Goliath's spear | `@goliath_spear` | — | shaft **taller than Saul** | weaver's-beam thick dark hardwood shaft, massive leaf-shaped iron head, iron butt-spike | draft |
| Goliath's tower shield | `@goliath_shield` | — | covers a grown man shin-to-shoulder | carried by the shield-bearer; bronze face + domed central boss; strap & grip on the back | draft |
| Goliath's sword | `@goliath_sword` | — | so large David needs **both hands**, nearly his own height | broad straight double-edged dark iron blade, bronze crossguard & pommel; David draws it in Clip 91 | draft |
| David's shepherd's staff | `@david_staff` | — | ≈ **David's own height** when planted | humble worn crooked hardwood, hooked/knobbed top, hand-worn grip patch ("a stick" gag) | draft |
| David's sling, pouch & 5 stones | `@david_sling_kit` | — | sling hand-length; stones **fist-sized** | two-cord leather shepherd's sling, leather drawstring pouch, 5 smooth grey-tan river stones; hero slow-mo stone (Clip 89) | draft |
| King Saul's royal armor set | `@saul_armor` | — | sized for **185 cm king**; swallows 158 cm David | bronze scale-and-chain breastplate, domed helmet, gilded sword; the "swallows him" gag (Clip 80) | draft |
| Jesse's provisions | `@jesse_provisions` | — | loaves/cheeses **hand-sized**; basket two-handed | grain basket, 10 rustic flat loaves, 10 pale cheeses (light/optional — may go inline) | draft |
| Provisions handcart | `@provisions_cart` | — | waist-high | simple two-wheel wooden handcart, plank bed, pull handles (assumed hand/push cart) | draft |
| ANN camera rig | `@ann_camera` | — | shoulder-held; mic ~a forearm | matte-black modern video camera + shotgun zoom mic; **brand-neutral, no logos** | draft |
| ANN drones (pair) | `@ann_drones` | — | two-hand carry each | matte-grey modern quadcopters, gimbal cam; **brand-neutral, no text** | draft |
| ANN tablet | `@ann_tablet` | — | hand-held | modern glass/aluminium slate; abstract blue UI, **no readable text**, brand-neutral | draft |
| Chris's ANN smartwatch | `@ann_watch` | — | wrist-sized | modern smartwatch + **red arrow on the face**; abstract countdown ring (no text); the two-hour incursion clock | draft |
| ANN incursion artifact | `@ann_artifact` | — | two-hand held | ancient stone-and-bronze device, faint blue seam-glow, unreadable glyphs (optional) | draft |

## Scale references

| Element | Tag | File | Covers | Status |
|---------|-----|------|--------|--------|
| Cast scale lineup | `@cast_scale` | — | `@avg_soldier`, `@david`, `@saul`, `@goliath` — all principals on one ground line | draft |
| David–Goliath lineup | `@david_goliath_scale` | — | the face-off two-shot proportions | draft |
| Saul-armor / David lineup | `@saul_armor_david_scale` | — | the oversized-armor "swallows him" gag | draft |

---

## Franchise assets used (shared — registered elsewhere)

These recur across every ANN episode; their canonical rows and accepted files live in [ANN Franchise - Shared Cast, Brand & Wardrobe.md](../../ANN%20Franchise%20-%20Shared%20Cast,%20Brand%20&%20Wardrobe.md). Referenced here only so this episode's full inventory is visible — **do not duplicate their File paths here; read them from the franchise file.**

- **ANN crew (cast):** `@chris` · `@clarissa` · `@tec_nical` · `@phro_nesis` · `@sue_nesis` · `@kata_lambano` · `@ann_team`
- **ANN brand:** `@ann_logo_monogram` · `@ann_logo_icon` · `@ann_logo_lockup`
- **ANN wardrobe:** `@ann_jacket`

---

## Registration rules (reminder)

1. Register at **finalization**, not before — `draft` → `final` only after the asset's QA checklist passes.
2. **One element, one tag, forever.** To revise an asset, add a new versioned File (`david_v2.png`) and update the File column — the tag never changes.
3. Fill **Critical details** and **Scale** at registration time (pre-filled above from the design files — verify against the accepted image).
4. Annotated variants (e.g. a red-arrow prop) are their own row when they serve a distinct purpose.
5. Keep the manifest sorted and clean — it's read far more than it's written.
