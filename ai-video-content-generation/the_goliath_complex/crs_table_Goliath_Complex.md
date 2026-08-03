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
| Goliath | 297 cm | 1.86 | ~8.5 + **~2× shoulder width** | heavyweight mass, heavy brow, thick dark beard, weathered; the giant reads through *mass*, not height alone — and he is a huge **man**, capped at *a little under twice* a man's height (see the scale cage below) |
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
- Goliath's **kneecap** ≈ the shield-bearer's **hip**; Goliath's hanging **elbow** ≈ just above the shield-bearer's **feather crest**
- Goliath ~**2× the shoulder width** of any man — mass sells the giant more than height alone
- **Ceiling:** Goliath stands *a little under twice* a man's height — two average men one on the other's shoulders would overtop him

> **Guard — David's height (do not shrink him).** The script has Eliab sneer that David is "head and shoulders below us all" and call him a "pipsqueak." That is **in-character insult, not a scale directive.** David stays ~158 cm (≈ average soldier height); his youth reads through slight build, smooth face, and rosy complexion. Only Saul's "head and shoulders above" is literal. Don't let a prompt-writer copy Eliab's line into a size instruction.

---

## The scale cage — bounding a giant

**Field-tested, Clip 3 (Scene 1).** A single landmark line is *not enough* for Goliath. Across three
different video models the "shield-bearer's crown just above Goliath's waist" instruction held for
about two seconds and then the model kept growing him — ending on a ~15 m titan whose calves the
bearer no longer reached. A landmark on its own is a *floor* with no *ceiling*, so the model reads
the surrounding superlatives as permission to escalate.

**Two causes, both fixable in the prompt:**

1. **Unbounded vocabulary.** *colossal, enormous mass, monumental scale, towering, earth-shaking,
   ground tremor* are open-ended intensifiers. They do not describe a size, they describe "more",
   and the model obliges — frame after frame. **Ban them from Goliath's prompt text.** He is "a
   giant of a man built on human proportions, heavyweight-wrestler mass." Mass words are fine when
   they describe *build*; they are poison when they describe *scale*.
2. **God's-eye overheads in a scale shot.** A top-down destroys the shared ground line that the
   whole comparison rests on, so the model re-guesses both figures' sizes from scratch on the new
   angle. Use a **high three-quarter** that keeps both pairs of feet in frame instead.

**The cage — state several body-meeting contacts plus an explicit ceiling.** One contact can be
satisfied while the figure still inflates; four mutually-contradicting contacts cannot:

- @shield_bearer's crown reaches just above Goliath's waist, **at his belt line**
- Goliath's **kneecap** sits level with @shield_bearer's **hip** ← the line that directly forbids
  the observed failure (bearer below the giant's calf)
- With Goliath's arm hanging, his **elbow** rides just above @shield_bearer's **feather crest**
- Goliath's shoulders ≈ **twice** @shield_bearer's shoulder width
- **Ceiling:** "two men of @shield_bearer's height standing one on the other's shoulders would
  overtop Goliath"; "both men fit whole inside the frame together on one visible ground line"

**Anchor the multiple to a named figure in the shot, not to "a man."** "Twice a man's shoulder
width" has no referent on screen; "twice @shield_bearer's shoulder width" does. When Goliath is
alone in frame, use whatever *is* in frame as the yardstick — the nearest soldiers of
`@philistine_army` (they reach about his waist), or his own planted `@goliath_spear` (head at about
his shoulder). A solo shot with no yardstick has nothing holding his size at all.

**Restate the cage three times per shot:** in FIRST FRAME / BLOCKING (full list), in ACTION at the
reveal beat, and compressed in POSITIVE LOCKS — plus "the same size in the last frame as in the
first."

**Weight is relative, not seismic.** A ~297 cm man is heavy, not geological. "His steps are heavier
and slower than the bearer's, a low puff of dust at each boot, the ground staying firm and still"
delivers the dramatic weight; "earth-shaking footfalls / ground tremor" reads to the model as
evidence he must be enormous, and it resizes him to justify the tremor. Same trap in AUDIO and in
STYLE ("monumental scale").

> **The cage applies to prop sheets too — and a prop needs its own ceiling.** `@goliath_shield`
> v1 was specced "covers a grown man shin-to-shoulder" and generated at exactly that — a
> *well-fitted* shield for the 165 cm bearer rather than one built for a 297 cm champion. The v2
> re-spec then over-corrected to roughly **4–5× the man's height** — a gate, not a shield — because
> it repeated the Clip 3 mistakes inside a prop prompt: *"enormous"*, *"built for a giant warrior"*,
> *"with room to spare"*, a bare "taller than a man" floor with no maximum, and (worst) a *"**small**
> grey silhouette"* for the yardstick, which invited the model to shrink the reference figure instead
> of holding the prop's size.
>
> A giant's prop is described as **oversized for the person handling it, by a stated amount, with a
> ceiling and a measurable landmark**: `@goliath_shield` = ≈1.35× the bearer's height (never past
> 1.5×), lower rim at his ankles, top rim ~2.5 head-heights above his crown, **his crown reaching
> only ~7/10 of the way up the shield**, width ≈ twice his shoulder span, aspect ≈ 2.5:1.
>
> **Two further traps, both learned on v3 of this same prop:**
>
> 1. **A size-class analogue is the strongest lever in a prop prompt — so a wrongly-chosen one is the
>    most destructive thing in it.** v3's ratios were correct and internally consistent, and the model
>    ignored all of them because the prompt also said *"the same size class as a Roman scutum or a
>    Norman kite shield"* — two **man-fitted** shields. The concrete analogue beat every ratio line
>    and the shield came back at ~0.85× the man. Check that the analogue actually sits in the target
>    class before naming it (a door leaf does; a scutum does not), and drop function phrases that
>    imply a comfortable fit ("a shield he could hold").
> 2. **Never bake a yardstick figure into a referenceable sheet.** v3 put a grey silhouette in every
>    view, which meant every video prompt attaching that sheet would be attaching a picture of a man —
>    a direct bleed risk into the generation — and it consumed two of the four view slots, so the
>    sheet delivered only three object views. **The referenceable sheet holds the object alone.**
>    Carry absolute size through **internal proportion cues** instead — strap and grip sized to a
>    normal forearm and spanning only ~⅓ of the width, boss ≈ ¼ of the width, a stated aspect ratio —
>    which read as "built for someone far larger" with no person in frame. Prove the ratio in a
>    **separate QA-only comparison image** that is checked once and never uploaded. Also state
>    positively that straps and grips are **empty** — "no hands" as a negative produced a glove.
>
> The capped prop then doubles as a second yardstick for the giant; an *uncapped* prop is a second
> thing to go wrong.

---

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
