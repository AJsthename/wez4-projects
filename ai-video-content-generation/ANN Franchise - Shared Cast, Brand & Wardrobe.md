# ANN Franchise — Shared Cast, Brand & Wardrobe

**ANN = Ancient News Network.** These assets recur across **every** ANN episode, not just one storyline — the reporting crew, the lab team, the logo system, and the crew wardrobe. This file is their **single source of truth**: design them once, register the accepted files here, and every episode references the same `@tags`. Individual episodes (e.g. `the_goliath_complex/`) list these under a "Franchise assets used" section and read the File paths from here — they do **not** re-register or re-tag them.

**Managed via the asset-librarian skill.** Same registry format as an episode manifest; same status discipline (`draft` → `final` → `retired`).

> **Golden rule — reuse, never re-mint.** A new ANN episode reuses `@chris`, `@ann_jacket`, `@ann_logo_lockup`, etc. verbatim. Minting a new tag for the same recurring element is the one thing that breaks franchise continuity. New *versions* of an asset change the File path, never the tag.

---

## Brand palette (locked)

| Role | Hex | Use |
|------|-----|-----|
| Accent / brand color | **`#2596be`** (bright teal-blue) | the constant ANN color — reads on light and dark |
| Light / knockout | **`#ffffff`** (white) | the mark on **dark** backgrounds |
| Neutral text | near-black charcoal | secondary text/outline on **light** backgrounds |

**Alternation rule:** teal is always present. Light bg → **teal (+ charcoal)** mark; dark bg → **white + teal** mark.

---

## ANN Logo System

| Element | Tag | File | Critical details | Status |
|---------|-----|------|------------------|--------|
| ANN monogram | `@ann_logo_monogram` | — | dark bg; **spells exactly "ANN"** (3 letters); white letters + teal `#2596be` broadcast arcs; flat vector, no 3D/gradients. Ships inverted (teal + charcoal) on light bg | draft |
| ANN icon | `@ann_logo_icon` | — | light bg; **no letters**; teal `#2596be` obelisk/sundial gnomon + concentric broadcast arcs, charcoal hairline; reads at small size. Ships inverted (white + teal) on dark bg | draft |
| ANN horizontal lockup | `@ann_logo_lockup` | — | icon left · **"ANN"** wordmark right · **"ANCIENT NEWS NETWORK"** tagline beneath; white + teal on dark. Used in corner bugs, lower-thirds, jacket back | draft |

> **Text-rendering caveat:** AI generators garble letters. Use generated images for the **mark + color system**; set the final wordmark in a vector tool and composite. QA every letter of "ANN" / "ANCIENT NEWS NETWORK".

## ANN Crew Wardrobe

| Element | Tag | File | Critical details | Status |
|---------|-----|------|------------------|--------|
| ANN crew jacket | `@ann_jacket` | — | graphite-charcoal technical shell; teal `#2596be` accent piping + white trim; **`@ann_logo_icon` palm-sized on left chest**, **`@ann_logo_lockup` large across upper back**; one master design, fit scales per wearer. **Depends on the logos being accepted first.** | draft |

> **Wardrobe ↔ cast lock:** dress every ANN character sheet in `@ann_jacket` so identity + wardrobe stay locked together.
> **Future wardrobe pieces (same standard):** crew cap/beanie w/ icon, field vest, lanyard/ID, backpack livery — reserve tags when added.

---

## ANN Cast

Recurring on-screen crew. Heights are ×base (base = average man ~160 cm) from the Scale Bible; carry each episode's scale line forward.

| Element | Tag | File | Scale | Critical details | Status |
|---------|-----|------|-------|------------------|--------|
| Chris | `@chris` | — not filed | 1.10× base | **young reporter, mid-to-late 20s (max ~30)**; caucasian; modern attire, carries `@ann_tablet` and wears `@ann_watch` (the two-hour clock); wears `@ann_jacket` | final |
| Clarissa | `@clarissa` | — not filed | 1.09× base | **young reporter, mid-to-late 20s (max ~30)**; african, ebony; distinctive hair; modern reporter attire, tablet; wears `@ann_jacket` | final |
| Mr Tec Nical | `@tec_nical` | — not filed | 1.12× base | east-asian/indian, moderately bulky; cameraman — `@ann_camera`, worn headcam + backpack; wears `@ann_jacket` | final |
| Professor Phro Nesis | `@phro_nesis` | — not filed | 1.09× base | caucasian; lab coat, scientist (lab team) | final |
| Doctor Sue Nesis | `@sue_nesis` | — not filed | 1.00× base | east-asian; lab coat, scientist (lab team) | final |
| Mr Kata Lambano | `@kata_lambano` | — not filed | 1.11× base | bangladeshi; professional attire (lab team) | final |
| ANN team (background ensemble) | `@ann_team` | — not filed | variable (~×1.0–1.12) | background ANN crowd palette — 4 distinct modern staff, varied gender/ethnicity/age/build/hair; ANN brand (graphite + teal #2596be, small ANN badge and/or lanyard); role mix (crew jacket / lab coat / utility gilet / coordinator); no clones, none duplicating a named principal's signature | final |

> **Narrator:** appears voice-only (no on-screen presence) — no sheet planned. Add a tag if ever seen on camera.
> **Episode note:** the reporting trio (`@chris`, `@clarissa`, `@tec_nical`) is core to every episode; the lab team (`@phro_nesis`, `@sue_nesis`, `@kata_lambano`) may or may not appear per episode — the tag stays reserved either way.

> ### Cast came before brand — deliberately. Read this before the franchise pass.
> The registration order below has logos → jacket → cast, so every crew sheet would be generated *wearing the accepted* `@ann_jacket`. In practice the cast came first: all seven sheets are generated and `final` while the three logos and the jacket are still `draft`. **Crew wardrobe currently lives in each sheet's own prompt text**, which is enough to keep a single episode consistent, so the brand assets are consciously **deferred** rather than blocking.
>
> The one thing that inverts when the franchise pass happens: `@ann_jacket` can no longer *define* the wardrobe, because seven accepted sheets already show it. Build the jacket **to match those sheets** — read its real design off them, write that into Critical details, and generate to match. Defining a new jacket at that point would drift the wardrobe away from cast sheets that are already locked and in use.
>
> Also note **no crew sheet is filed in the repo yet** — the tags resolve only inside the generation platform. Export and file all seven.

---

## Copy-paste blocks (bare tags)

**ANN cast:**
```
@chris @clarissa @tec_nical @phro_nesis @sue_nesis @kata_lambano @ann_team
```
**ANN brand & wardrobe:**
```
@ann_logo_monogram @ann_logo_icon @ann_logo_lockup @ann_jacket
```

---

## Dependencies & registration order

1. **Logos first:** `@ann_logo_monogram`, `@ann_logo_icon`, `@ann_logo_lockup` (the jacket and every branded surface need them).
2. **Jacket second:** `@ann_jacket` (composites the accepted icon + lockup).
3. **Cast third:** each crew sheet is generated wearing the accepted `@ann_jacket`.
4. **Register** each accepted asset here (set File, flip Status to `final`); put palette hexes and "spells ANN" into Critical details so downstream prompts restate them.

_Franchise-level sibling to the per-episode character/prop/location asset files. First consumer: The Goliath Complex._
