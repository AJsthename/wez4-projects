# The Goliath Complex — Brand & Wardrobe Assets: Descriptions & Generation Prompts

**Project:** "The Goliath Complex" (Gulayat) — ANN / David & Goliath, 1 Samuel 17
**Franchise note:** ANN = **Ancient News Network**. The logo and crew wardrobe recur across *every* ANN episode, not just this one — treat them as **franchise-level assets** and reuse the same tags in future projects.
**Style:** Realism/Hyperrealism · brand marks are clean modern vector-style graphics; wardrobe follows the mid-gray sheet standard.

## Brand palette (locked)

| Role | Hex | Use |
|------|-----|-----|
| Accent / brand color | **`#2596be`** (bright teal-blue) | the constant ANN color — reads on both light and dark |
| Light / knockout | **`#ffffff`** (white) | the mark on **dark** backgrounds (white would vanish on light) |
| Neutral text (implied) | near-black charcoal | secondary text/outline on **light** backgrounds (teal stays the accent) |

**Alternation rule (as requested):** teal is always present. On a **light** background the mark is **teal** (+ charcoal); on a **dark** background the mark is **white + teal**. Each view below is generated on one background but ships in both — note the inverted variant.

> ⚠️ **Text-rendering caveat.** AI image generators often garble letters. "ANN" is short, which helps, but for the *final* production logo, set the wordmark in a real vector tool (Illustrator/Figma) and composite it — use the generated images for the **mark/concept and color system**, and QA the letterforms hard (see checklists). Every prompt below asks for exactly the three letters **A-N-N**.

---

# Section A — ANN Logo System

Shared identity concept (keep consistent across all three views): **a news network that broadcasts from ancient history** — fuse a **broadcast-signal motif** (radiating arcs/waves) with an **ancient time cue** (a sundial / obelisk / laurel). Modern, confident, minimal.

## A1. Monogram — `@ann_logo_monogram` (dark background)

**Description:** The pure typographic mark — the three letters **ANN** as a tight, bold, modern geometric wordmark, the two N's sharing a clean vertical stroke, with a small broadcast-signal arc accent rising off the top. On a dark ground: white letters, teal signal accent.

### Image-Generation Prompt
```
Flat vector logo design, a bold modern monogram of the three letters "ANN" (A, N, N), centered on a
solid dark charcoal background (near-black).
The letters are a tight geometric sans-serif wordmark in pure white (#ffffff), the two N's sharing a
clean shared vertical stroke; a small set of three concentric broadcast-signal arcs in bright teal-blue
(#2596be) radiates from the top-right corner of the mark as an accent.
Minimal, crisp, high-contrast, perfectly legible, flat 2D, no 3D, no gradients, no photographic texture,
no background scenery. Centered with even margins. The text reads exactly A-N-N, three letters only.
```
### QA Checklist
- [ ] **Spells exactly "ANN"** — three letters, correct shapes, no extra/missing/warped letters
- [ ] White letters + **teal signal accent**; nothing else colored
- [ ] Flat vector look (no 3D bevels, no gradients, no photo texture)
- [ ] Crisp edges, centered, even margins, high contrast on the dark ground
- [ ] Ships inverted too: on light bg → **teal** letters + charcoal accent (regenerate/recolor to confirm)

## A2. Icon — `@ann_logo_icon` (light background)

**Description:** The standalone symbol (app-icon / emblem) — **no letters**, or a single subtle initial. A rounded-badge emblem containing an abstract mark: an obelisk/sundial gnomon with broadcast arcs radiating from its tip. On a light ground: teal mark, charcoal hairline.

### Image-Generation Prompt
```
Flat vector app-icon emblem, centered on a solid light off-white background (#ffffff / very pale grey).
A rounded-square badge containing a single abstract symbol: a simple upright obelisk / sundial gnomon
with three concentric broadcast-signal arcs radiating from its tip, suggesting a news signal sent from
ancient times. The mark is bright teal-blue (#2596be) with a thin charcoal hairline; the badge interior
is clean white. Minimal, geometric, iconic, instantly readable at small size.
Flat 2D, no 3D, no gradients, no text, no photographic texture, no scenery. Centered with even margins.
```
### QA Checklist
- [ ] Works as a **standalone icon** with no wordmark — reads clearly at small size
- [ ] Teal mark on a clean light ground; charcoal hairline only (no other colors)
- [ ] The concept reads: "signal / broadcast" + "ancient" (arcs + obelisk/sundial)
- [ ] Flat vector, crisp, centered, balanced within the badge
- [ ] Ships inverted too: on dark bg → **white + teal** mark

## A3. Horizontal Lockup — `@ann_logo_lockup` (dark background)

**Description:** The full horizontal signature — the **icon at left**, then the **ANN** wordmark, with a small "ANCIENT NEWS NETWORK" tagline beneath the letters. Used in corner bugs, lower-thirds, and on the jacket back. On a dark ground: white wordmark + teal icon + white tagline.

### Image-Generation Prompt
```
Flat vector horizontal logo lockup, centered on a solid dark charcoal background (near-black).
Left: the ANN icon — a rounded badge with an obelisk/sundial gnomon and three teal-blue (#2596be)
broadcast arcs radiating from its tip.
Right of it, vertically centered: a bold geometric sans-serif wordmark "ANN" in white (#ffffff), and
directly beneath it, small, wide-tracked uppercase tagline "ANCIENT NEWS NETWORK" in white.
Clean spacing between icon and wordmark, aligned to a shared baseline. Minimal, broadcast-brand, crisp.
Flat 2D, no 3D, no gradients, no photographic texture, no scenery. The wordmark reads exactly A-N-N.
```
### QA Checklist
- [ ] Layout: **icon left · "ANN" wordmark right · tagline beneath**, cleanly aligned
- [ ] Wordmark spells exactly **"ANN"**; tagline reads **"ANCIENT NEWS NETWORK"** (check every letter)
- [ ] White wordmark/tagline + teal icon; consistent with the monogram and icon
- [ ] Flat vector, crisp, balanced horizontal spacing
- [ ] Ships inverted too: on light bg → **teal** icon + charcoal wordmark/tagline

> If the generator can't render "ANCIENT NEWS NETWORK" cleanly, generate the lockup **without the tagline** (icon + "ANN" only) and add the tagline in a vector edit.

---

# Section B — ANN Crew Wardrobe

## B1. ANN Crew Jacket — `@ann_jacket`

**Description:** The signature jacket the ANN field team wears on every time-incursion — practical, modern expedition/press outerwear that reads instantly on camera as "the crew." A weather-resistant technical shell in graphite charcoal with **teal-blue (`#2596be`)** accents and **white** details, brand-consistent. The **ANN icon** sits palm-sized on the left chest; the **horizontal lockup** runs large across the upper back (press-crew style). Designed once; worn by all crew (Chris, Clarissa, Mr Tec Nical, and the lab team on shoots) in **different sizes** — the design is identical, only the fit scales per wearer.

Why now: the jacket carries the logo, so the logo has to exist first (Section A) — generate A1–A3, accept them, then place the **icon** (chest) and **lockup** (back) here.

### Image-Generation Prompt
```
Character-wardrobe reference sheet of a modern technical field jacket on a solid mid-gray studio
background, even soft studio lighting, soft grounding shadow, photorealistic.
Three views of the same jacket, consistent across all views (shown on an invisible/mannequin form, no person):
[1] front view, [2] back view, [3] three-quarter view.
Jacket: a weather-resistant graphite-charcoal technical shell jacket, matte fabric, zip front, stand
collar, several utility pockets with flap and zip closures, slightly futuristic but grounded expedition
styling; bright teal-blue (#2596be) accent piping along the shoulders, zip pulls and inner cuffs; thin
white (#ffffff) trim details. On the LEFT CHEST, a small palm-sized ANN icon patch (a rounded teal badge
with an obelisk-and-broadcast-arcs mark). Across the UPPER BACK between the shoulder blades, a large ANN
horizontal lockup — the icon plus a bold white "ANN" wordmark. Clean, well-fitted, brand-crew look.
Clean sheet layout, no person, no head, no text labels other than the jacket's own ANN branding, no scenery.
```
### QA Checklist
- [ ] Same jacket across all three views — cut, pockets, collar, accent placement consistent
- [ ] **Left-chest ANN icon** (palm-sized) present in front & 3/4; **large ANN lockup across the back** in back view
- [ ] Branding spells **"ANN"** correctly (check letters); teal + white accents match the [brand palette](#brand-palette-locked)
- [ ] Reads as **modern technical/expedition** wear (the deliberate anachronism vs the ancient world)
- [ ] Fabric has real volume — folds, seams, sheen, grounding shadow (not a flat cutout)
- [ ] Background solid mid-gray; no person/mannequin visible, no stray text
> **If the logo garbles on the jacket:** generate the jacket clean (accent colors + blank patches), then composite the accepted `@ann_logo_icon` and `@ann_logo_lockup` onto the chest and back in an edit pass. **Sizing:** this is the single master design — when each ANN character sheet is generated, dress them in this jacket so wardrobe stays identical; fit scales to the wearer, the design does not change.

---

## Handoff & notes

- **Register** all four elements via the **asset-librarian** skill as a new kind of entry — brand/wardrobe assets. Suggested tags: `@ann_logo_monogram`, `@ann_logo_icon`, `@ann_logo_lockup`, `@ann_jacket`. Put the **palette hexes and "spells ANN"** into Critical details so every downstream prompt restates them.
- **Dependency:** the jacket depends on the logo (icon + lockup) being accepted first.
- **Wardrobe ↔ character sheets:** `@ann_jacket` is the wardrobe reference; the ANN crew **character sheets** should show them wearing this exact jacket so identity + wardrobe stay locked together.
- **Decisions I made for you (change freely):** monogram/lockup on dark grounds, icon on light; icon concept = obelisk/sundial + broadcast arcs; jacket base = graphite charcoal with teal/white accents; tagline = "ANCIENT NEWS NETWORK". Say the word to swap any of these.
- **Next wardrobe pieces** (when you're ready, same standard): crew cap/beanie with the icon, field vest, lanyard/ID, backpack livery — all carrying the same logo system.

_These are brand & wardrobe assets — a sibling to the character, prop, and location asset files._
