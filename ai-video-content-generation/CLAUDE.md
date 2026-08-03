# CLAUDE.md — AI Video Content Generation Rulebook

This is the master rulebook for the entire AI video content generation system. Everything produced in this project — scripts, asset sheets, manifests, and Seedance prompts — follows the rules here. When a more specific skill or project file conflicts with this document, the more specific one wins for its narrow domain, but the principles below are the defaults everywhere.

> This document is a living rulebook. It is expected to be edited and expanded as the workflow matures. When a new durable rule emerges from real production work, record it here rather than letting it live only in one project's head.

---

## 0. The Prime Directive: Tips Are Heuristics, Not Laws

The [pro_tips_and_guidelines.md](pro_tips_and_guidelines.md) file and the skills are a **toolbox, not a checklist**. Every technique in them was learned in a specific situation and is only worth applying when that situation is actually present.

**Before applying any tip, technique, or template, ask: does this task actually need it?**

- A tip written for **building a script or emotion from scratch** (e.g. #1 anatomical emotion detailing, #22 classic story structure) adds little to a project that already ships with a **locked, fully-directed script** where the beats, dialogue, and tension are already written. In that case, borrow only the *elements* that translate the existing intent into visible instructions — do not re-invent the story.
- A tip that solves a **problem you don't have** is noise. Don't add a Dutch angle (#27) to a calm scene, don't split location views (#16) when the model renders the location fine, don't build a scale bible when only one character is ever on screen.
- Techniques can be **partially** applied. Take the coordinate-system idea from #3 without adopting its screen-text rules; take handheld motion from #28 without speed ramps from #30.

When you apply a technique, it should be because you identified a concrete need for it in *this* shot, *this* asset, or *this* project — not because it appears in the list. State briefly *why* a technique fits when you use it in a non-obvious place, so the choice is reviewable.

**Viability check, every time:** _Is this relevant here? What does it cost? What breaks if I skip it? Is a lighter partial version enough?_ If a technique doesn't clearly earn its place, leave it out.

---

## 1. What This Project Is

An AI video production pipeline that turns a script into finished cinematic clips generated with **Seedance 2.0**. The core insight of the whole system: **video generations have no memory of each other**, so consistency (of characters, locations, props, scale, and voice) has to be manufactured up front through reusable reference assets and disciplined prompting.

Current projects live in their own top-level folders:
- `Acts 23/` — biblical-humor short (Paul before the Sanhedrin).
- `the_goliath_complex/` — David & Goliath (1 Samuel 17).

Each project is self-contained: its script, asset descriptions, generated images, and Seedance prompts stay inside its own folder.

---

## 2. The Canonical Workflow

Follow this order. Skipping ahead is the source of most wasted generations.

```
Script / concept
      │
      ▼
[asset-planner]      → the asset production list: what characters, locations, props need sheets
      │
      ▼
[asset-scale]        → (only if >1 character and relative size carries meaning) the Scale Bible + cast lineup
      │
      ▼
[asset-character]    → character sheet prompts + QA
[asset-location]     → location plate prompts + QA (or a documented SKIP)
[asset-prop]         → prop sheet prompts + QA
      │
      ▼
[asset-librarian]    → register every FINAL asset in assets/MANIFEST.md with its @tag
      │
      ▼
[seedance-clean]     → write the shot prompts, referencing @tags + restating critical details
      │
      ▼
Generate → iterate → splice
```

**Rules for the workflow:**
- **Plan before you generate.** Run `asset-planner` on any new script before producing a single sheet. Discovering a missing asset mid-shoot is the failure the planner exists to prevent.
- **Decide scale before sheets exist.** Each sheet fills its own frame, so relative size cannot be added afterward. If size matters (a giant vs a boy), `asset-scale` runs *first*.
- **Nothing gets referenced until it's `final`.** A video prompt may only `@tag` an asset that has passed its QA checklist and been registered by the librarian. Draft assets are never referenced.
- **The manifest is the single source of truth** for what exists, what its tag is, and which critical details must be restated in prompt text. Check it at the start of every prompt-writing session.

---

## 3. The Skills and When to Use Them

| Skill | Use it when | Output |
|-------|-------------|--------|
| `asset-planner` | A new script/concept exists and you need to know what to build | Prioritized asset production list |
| `asset-scale` | >1 character shares frame and comparative size matters | Scale Bible (ratios + landmark chain) + cast-lineup spec |
| `asset-character` | A character/creature/group needs a reference sheet | Image-gen prompt + QA checklist |
| `asset-location` | An environment needs a reference plate (or a skip decision) | Image-gen prompt + QA, or a documented SKIP |
| `asset-prop` | An object is held/used/interacted with or recurs | Image-gen prompt + QA checklist |
| `asset-librarian` | An asset is finalized, or you need a `@tag` / critical details | Updated `assets/MANIFEST.md` |
| `seedance-clean` | Writing any Seedance shot prompt | A single standalone prompt in a code block |

Always **consult the relevant skill before doing its job by hand.** The skills encode hard-won detail (QA checklists, tag rules, scale landmark syntax) that is easy to forget.

---

## 4. Non-Negotiable Prompting Principles

These come from the `seedance-clean` skill and apply to every Seedance prompt without exception:

1. **Write the visible.** The model reacts to what can be seen and measured, never to mood words. Translate every abstraction into something observable — "tense" becomes "jaw clenches, half the face in shadow, fist slowly closing."
2. **Positive phrasing only.** State the target, never the prohibition. "Stays upright, feet planted," never "does not fall." (This is also tip #35 — Seedance inverts negatives.)
3. **Context isolation.** Every prompt is a sealed, single-shot document with no memory of other shots. Never carry in scene numbers, prior-scene summaries, "as above" phrasing, or unused tags/characters.
4. **References set identity; text sets action.** A `@tag` locks appearance; the text locks what happens and restates droppable critical details (logos, exact colors, marked buttons, small text). Both are required. Keep appearance text minimal so it doesn't fight the reference image.
5. **Never place an `@tag` in a shot where that object isn't present** — the model will force it into frame.
6. **Concrete units.** Speeds in km/h. Atmosphere in percent/meters. FOV in degrees (from the anchor table, discrete steps only). White balance in Kelvin. Relative height via body landmarks ("crown reaches his navel"), never ratios or centimeters.
7. **One idea, one action, one camera strategy per shot** (tip #3). If a prompt is doing too much, it will hallucinate.
8. **Camera block sits third** (subject → action → camera → style → constraints). Style is distributed into its home blocks, never a prefix at the top.
9. **No director names, no signature-work references, no equipment model names** — they get ignored or break complex moves. Describe the *look*, not the gear (this is the disciplined form of tip #2: extract the optical *character*, not the brand).
10. **English prompts only.**
11. **Cage a size, don't just state it — landmarks are a floor, so always write the ceiling too.** A single landmark line ("his crown reaches Goliath's waist") tells the model where the *minimum* gap is and nothing about the maximum, so it drifts upward over the clip. Learned the hard way: across three video models, Goliath held the right ratio for ~2 seconds and then inflated into a ~15 m titan. The fix has four parts, and all four are needed:
    - **Multiple contacts, not one.** State two or three places where the bodies *meet* — crown-to-belt, knee-to-hip, hanging-elbow-to-helmet. One contact can be satisfied by an inflating figure; three mutually-contradicting ones cannot.
    - **An explicit ceiling, in body terms.** "A little under twice his height", "two men one on the other's shoulders would overtop him", "both figures fit whole in one frame on one visible ground line", "the same size in the last frame as in the first."
    - **Ban unbounded scale vocabulary.** *colossal, enormous, monumental scale, towering, gigantic, earth-shaking, ground tremor* do not name a size, they name "more" — and the model keeps delivering more. Describe **build** instead ("heavyweight-wrestler mass, human proportions"), and make weight **relative** ("his steps land heavier and slower than the other man's; the ground stays firm"). Seismic sound and physics cues are read as evidence the figure must be bigger, and it gets resized to justify them.
    - **Anchor every multiple to something in the frame.** "Twice a man's shoulder width" has no on-screen referent; "twice `@shield_bearer`'s shoulder width" does. In a solo shot, use whatever *is* present — nearby crowd figures, or the character's own oversized prop — because a solo shot with no yardstick has nothing holding the size at all.

    Two supporting rules: **avoid god's-eye overheads in a scale shot** (an overhead discards the shared ground line the comparison depends on, and the model re-guesses both sizes on the new angle — use a high three-quarter that keeps both pairs of feet in frame); and **spec a large character's props oversized for whoever handles them, never fitted to them — but cap the prop too** (a shield anchored to "a grown man" comes out fitted to the ordinary bearer and wrong for the giant; a shield anchored to "enormous, built for a giant, taller than a man" comes out four times too big. Give the prop a ratio, a ceiling, a measurable landmark — "≈1.35× the bearer's height, never past 1.5×, his crown reaching only about seven-tenths of the way up it" — and a real-world size class **verified to be in the right class**. A capped prop is a second yardstick for the giant; an uncapped one is a second thing to go wrong.)

    **This principle is the one exception to §4's video-only framing — it governs image/asset prompts too.** The `@goliath_shield` sheet took four passes to land and each failure taught a different part of the rule: v1 fitted to the handler came out too small; v2 came back ~4× oversized from superlatives, no ceiling, and a yardstick figure described as "small" (which the model shrank instead of holding the object); v3 had correct, internally consistent ratios and was overridden anyway by a **wrongly-chosen size-class analogue** ("the same class as a Roman scutum" — a man-fitted shield), proving that a concrete real-world comparison outranks every ratio line in the prompt and must be checked for class before it is named.

    Three hard rules for scale-critical asset sheets: **(a) no human figure, hand, or silhouette in a referenceable sheet** — it bleeds into every video generation that attaches it and it consumes view slots; carry size through **internal proportion cues** instead (grip sized to a normal forearm at a stated fraction of the object's width, boss/control as a fraction of the whole, an explicit aspect ratio). **(b)** Prove the ratio on a **separate QA-only comparison image** that is checked once and never registered or uploaded. **(c)** State empty hardware **positively** — "no hands" in a trailing exclusion list produced a leather glove gripping the strap; "the strap and grip are empty and unoccupied, bare leather and bare wood" does not.
12. **(Video prompts only — never image/asset prompts) Clean-plate audio, titles in post.** A Seedance generation must produce only **diegetic sound**: environmental and action sound effects plus any spoken line. It must **never** generate a musical score, songs, or lyrics, and **never** render on-screen text, captions, subtitles, titles, or lower-thirds. Seedance injects a background score unprompted, so state the exclusion as a positive lock (`"diegetic sound only, no music, no on-screen text"`). Music beds and title/subtitle overlays are added later **in the edit**, where they stay controllable and removable — baking them into the generation makes the clip impossible to re-cut or re-score. Image/asset prompts have no audio and need no captions, so this rule does not touch them.

---

## 5. Asset & File Conventions

**Directory layout (per project):**
```
<project>/
  <script / study / production-plan>.md
  script_&_scenes/            (where used)
  assets/
    MANIFEST.md               ← the element registry (single source of truth)
    characters/
    locations/
    props/
    scale/
  <project> - Seedance Prompts.md
```

**Two-tier registry (episode vs franchise):**
- Each episode has its own `assets/MANIFEST.md` for episode-native elements (that story's cast, locations, props, scale references).
- **Recurring franchise elements** — a show's persistent brand, wardrobe, and recurring cast — live in a **shared franchise file at the repo root** (e.g. `ANN Franchise - Shared Cast, Brand & Wardrobe.md`), registered once and reused across every episode. Episodes list these under a "Franchise assets used" section and read File paths from the franchise file; they never re-tag or duplicate them. **Reuse the franchise tag verbatim, never re-mint** — a new tag for the same recurring element is what breaks cross-episode continuity.

**Element & tag rules (from `asset-librarian`):**
- **One element, one tag, forever.** Tags are lowercase, underscores, short, unique. Renaming a tag silently breaks every prompt already written — never do it.
- **Versions live in filenames, not new elements.** `mom_sheet_v3.png` replaces `v2` in the File column; the tag is unchanged. A genuinely different reference (Mom in winter) is a new element with a new tag.
- **Fill "Critical details" and "Scale" at registration time**, while the QA pass is fresh. These are the words prompt-writers copy into every shot.
- **Status discipline:** `draft` → `final` (QA-passed, referenceable) → `retired` (superseded, note the replacement).
- **Annotated variants are their own rows** when they serve a distinct purpose (e.g. the arrow-marked prop for a button-press shot vs the clean prop).

---

## 6. Consistency Machinery (the whole point)

Because generations don't share memory, consistency is engineered:

- **Reference sheets** lock appearance across shots. Reuse the *exact* same sheet every time.
- **Voice follows appearance** (tip #34): in Seedance the voice is derived from the character sheet, so referencing the same sheet keeps the voice stable. Locking visuals locks voices.
- **The Scale Bible + cast lineup** lock relative size; the landmark line gets restated in every multi-character prompt and the lineup image uploaded alongside the identity sheets. For any character whose size is the point, the Bible carries a full **scale cage** (multiple body contacts + an explicit ceiling + the banned-vocabulary list) rather than one landmark line, and the cage is restated three times per prompt — in blocking, in the action beat that reveals it, and compressed in the locks. See §4.11 and, as a worked example, [the_goliath_complex/crs_table_Goliath_Complex.md](the_goliath_complex/crs_table_Goliath_Complex.md).
- **Establishing/wide shots first** (tips #13, #29) map a room's geometry so later tight cuts keep everyone correctly placed. Anchor objects (#14) and top-down maps (#17) reinforce this.
- **Match cuts via last-frame handoff** (tip #31) and locked continuity fields (state, wardrobe, light, prop state) carry physical continuity across cuts.
- **Good frames from bad takes** (tip #9) become new lighting/positioning references — feed the win back into the reference pool.

---

## 7. Token & Iteration Economy

- **Iterate surgically** (tips #4, #10, #11). When a long generation is mostly right, tell the model to change only the failing segment. On long shot lists, update only the prompt that changed rather than re-rendering the whole list — it cuts token use dramatically.
- **Sanitize overloaded prompts** (tip #11). Repeated edits accumulate into conflicting instructions; periodically have the prompt studied, optimized, and stripped of what it no longer needs.
- **Multi-shot to batch consistency** (tip #6). For dialogue/action where lighting and positioning must match across reactions, generate multiple cuts in one prompt and splice the successful phases.

---

## 8. Where Each Tip Lives in the System

A quick index so techniques are applied in the right layer (all subject to the §0 viability check):

| Layer | Governing tips |
|-------|---------------|
| **Script / story** | #22 (structure), #21 (state tracking), #33 (post-flashback pauses) |
| **Asset generation** | #12 (60-30-10 + practical light), #15/#26 (3/4 angle, no front-on), #16 (split views), #19 (face swap), #20 (tricky-prop sheets), #23 (sheet format), #24 (soft lighting) |
| **Scale** | #21 partial; enforced via `asset-scale`; the scale cage (bounded size, banned superlatives, no overheads, oversized props) — see §4.11 |
| **Prompt writing** | #1 (anatomical emotion), #2 (photographer specificity), #3 (system-prompt adherence), #5 (second-by-second), #7 (phonetic dialogue), #8 (maximize detail), #35 (no negatives) |
| **Cinematography** | #25 (mood via location), #27 (Dutch angle/framing), #28 (handheld), #29 (wide-shot locking), #30 (speed ramps) |
| **Editing / transitions** | #6 (multi-shot), #31 (match cut), #32 (whip pan) |
| **Audio / on-screen text (video prompts only)** | #34 (voice lock via sheet), #35 (no negatives), #36 (clean-plate audio — diegetic SFX only, music & titles in post) — see §4.12 |
| **Continuity** | #9 (frames from bad takes), #13/#14/#17 (establishing, anchors, maps), #34 (voice lock) |
| **Efficiency** | #4, #10, #11 |

---

## 9. Working Style in This Repo

- **Keep projects self-contained.** Don't cross-reference one project's assets from another.
- **Prefer editing existing project files** over spawning new ones; this project already has established file names per project (script, asset descriptions, Seedance prompts).
- **Every finalized asset passes through the librarian.** No exceptions — an unregistered asset effectively does not exist.
- **When a rule proves itself in production, write it down here.** This file is the durable memory of how we make videos; the skills are the how-to for each step.
