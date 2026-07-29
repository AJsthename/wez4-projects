# The Goliath Complex — Scale Bible (Character Reference Sheet Table)

Single source of truth for size across the whole pipeline (reference sheet → clip → compile). Built with the **asset-scale** skill.

**Base unit:** the *average man/soldier* (~160 cm) = **×1.00**. Every character is expressed relative to it.
**Design height** is internal bookkeeping only — **never write centimetres into an image/video prompt** (models ignore them). Prompt with **head-count** and the **landmark chain** below instead.
**Note:** David (158 cm) is essentially average height for this cast — his youth must read through **build, face, and rosy complexion, not height**.

| Character | Design height* | ×base | Head-count | Build note |
| --- | --- | --- | --- | --- |
| David | 158 cm | 0.99 | ~7.5 | reddish/rosy complexion, handsome, slight, wiry — **youth reads via build/face, not height** |
| King Saul | 185 cm | 1.16 | ~8.3 | tall, broad-shouldered, kingly but careworn; full greying beard; head-and-shoulders above the people (1 Sam 9:2) |
| Eliab | 170 cm | 1.06 | ~7.8 | eldest brother; tall, soldierly, proud impressive bearing (1 Sam 16:6) |
| Goliath | 297 cm | 1.86 | ~8.5 + **~2× shoulder width** | colossal mass, heavy brow, thick dark beard, weathered; the giant reads through *mass*, not height alone |
| Goliath's Shield-bearer | 165 cm | 1.03 | ~7.6 | **sturdy and strong** (must bear the heavy tower shield) yet massively dwarfed by Goliath; loyal, watchful subordinate |
| Philistine Soldiers | 160–165 cm | 1.00–1.03 | ~7.4–7.6 | foreign warrior gear, distinct from Israelites; vary faces/builds across the group |
| Saul's Counsellors #1, #2, #3 | 157–162 cm | 0.98–1.01 | ~7.3–7.5 | older; robes over armor; rank indicators; three distinct faces/beards |
| Saul's General | 170 cm | 1.06 | ~7.8 | senior military commander; broad, grizzled, best-equipped Israelite officer (plumed helmet, officer's cloak + sash); authoritative — a clear head below Saul |
| Funny soldier #1 | 162 cm | 1.01 | ~7.5 | comic **lanky/gangly** build + **locked signature** (recurring cameo): very long neck, prominent hooked nose, wild expressive eyebrows, gap-toothed grin, oversized helmet that keeps slipping |
| Funny soldier #2 | 157 cm | 0.98 | ~7.3 | comic **short & stout** build + **locked signature** (recurring cameo): round ruddy face, huge bushy mustache/unibrow, permanently dented helmet — the visual foil to #1 |
| Chris (ANN) | 176 cm | 1.10 | ~8.1 | **young — mid-to-late 20s (max ~30)**; caucasian; modern reporter attire, tablet, watch |
| Clarissa (ANN) | 175 cm | 1.09 | ~8.0 | **young — mid-to-late 20s (max ~30)**; african, ebony; modern clothing, tablet, distinctive hair |
| Mr Tec Nical (ANN) | 179 cm | 1.12 | ~8.2 | east asian (chinese) or indian, moderately bulky/chubby; camera-op gear, headcam, backpack |
| Professor Phro Nesis | 175 cm | 1.09 | ~8.0 | caucasian; lab coat, scientist attire |
| Doctor Sue Nesis | 160 cm | 1.00 | ~7.4 | east asian (chinese); lab coat, scientist attire |
| Mr Kata Lambano | 177 cm | 1.11 | ~8.1 | mixed-race African-European, light tawny/golden-brown complexion (lighter than Clarissa's ebony); modern coordinator attire |
| Jesse | 164 cm | 1.03 | ~7.6 | elderly dignified father; grey beard, robes |
| ANN team members | variable | — | — | ensemble; vary height/build/features so no clones |
| Israeli Soldiers #1, #2 | 157–162 cm | 0.98–1.01 | ~7.4 | Israelite military attire; two distinct faces |
| Abinadab | 166 cm | 1.04 | ~7.7 | middle brother; soldierly (1 Sam 16:8) |
| Shammah | 165 cm | 1.03 | ~7.6 | middle brother; soldierly (was "Shammar" — read as Shammah, 1 Sam 16:9) |
| Israeli Soldiers (background) | 157–162 cm | 0.98–1.01 | ~7.4 | background crowd palette; varied |
| average man/soldier | 157–162 cm | **1.00 (base)** | ~7.4 | reference unit |

\*Design height ≈ head-count × ~21.5 cm (adult head). Goliath is given a proportionally larger head so he isn't a stretched man.

---

## Landmark chain (the phrasing bank — copy these into video prompts)

Camera-robust because each line states where two **bodies meet**, not a ratio (which perspective distorts):

- David ≈ average soldier height — **David's youth is build/face, not height**
- David's crown ≈ **Saul's chin/mouth**
- David's crown ≈ **Goliath's navel/waist** (~53% up his body)
- Average soldier's crown ≈ Goliath's navel/waist
- Saul's crown ≈ **Goliath's mid-chest** (~62%)
- Saul stands ~**a head above** the average soldier ("head and shoulders above the people," 1 Sam 9:2)
- Shield-bearer's crown ≈ **just above Goliath's waist** (script: "the shield bearer is slightly above his waist in height")
- Goliath ~**2× the shoulder width** of any man — mass sells the giant more than height alone

> **Guard — David's height (do not shrink him).** The script has Eliab sneer that David is "head and shoulders below us all" and call him a "pipsqueak." That is **in-character insult, not a scale directive.** David stays ~158 cm (≈ average soldier height); his youth reads through slight build, smooth face, and rosy complexion. Only Saul's "head and shoulders above" is literal. Don't let a prompt-writer copy Eliab's line into a size instruction.

> **Recurring-cameo signatures.** The two funny soldiers (and any minor comic character) carry a **locked, memorable signature look** so the audience thinks "oh, it's that guy!" whenever they reappear across projects. Register those signatures in the manifest exactly like a lead's critical details so they stay identical everywhere.

---

## Prop & location scale anchors

Anchor every prop to a body, not to centimetres — so scale survives generation:

- **Goliath's spear** — shaft "like a weaver's beam," **taller than Saul**; oversized iron head.
- **Goliath's armor & tower shield** — sized to his 297 cm frame; the tower shield ≈ the 165 cm shield-bearer's torso-to-head.
- **Saul's royal armor** — sized to a 185 cm broad king, so on 158 cm David it **visibly swallows him**: helmet slips over the eyes, mail hem past his shins, sword nearly his own height (the comic beat — 1 Sam 17:38-39).
- **David's staff** ≈ David's own height (~his shoulder-to-crown when planted); **sling** hand-sized; **5 smooth stones** fist-sized in the shepherd's pouch.
- **Goliath's coat of mail / greaves** — massive plates, heavy, over-scaled; sword long enough that David needs both hands (v.51).
- **Jesse's provisions** — grain basket cart-loaded; 10 loaves, 10 cheeses, hand-to-forearm sized.
- **ANN gear** (video camera, zoom mic, headcam, 2 drones, tablets, backpacks, circular time-portal stage) — scaled to the modern 160–179 cm actors.

---

_Consumed by: asset-planner (breakdown), asset-character (sheets + lineup), asset-librarian (manifest Scale field), seedance-clean (per-shot landmark phrasing). See the **Cast Scale Lineup** section in the character-assets file for the single-pass lineup that locks these relationships at the reference stage._
