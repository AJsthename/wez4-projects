---
name: asset-librarian
description: >
  Maintain the element registry for AI video projects — the manifest of finalized character, location, and prop assets. Use whenever an asset is finalized and needs saving/naming, when the user says "register this element", "save this asset", "name this character", "add to the manifest", asks "what assets do we have", "which elements exist", or needs the @tag name for an asset while writing a video prompt. Also use at the start of any video prompt-writing session to check which elements already exist so prompts reference exact saved images instead of re-describing them. Every finalized asset must pass through this skill.
---

# Asset Librarian

Enforce strict asset management: every finalized character, location, and prop is saved and explicitly named as an **element**, so script prompts can cleanly reference those exact images. An unregistered asset might as well not exist — three weeks into a project, "that dragon image somewhere in Downloads" is a lost asset.

**The registry is `assets/MANIFEST.md` at the project root.** One manifest per video project.

---

## THE MANIFEST

Create it on first registration; keep this exact structure:

```markdown
# Asset Manifest — [Project Name]

## Characters
| Element | Tag | File | Scale | Critical details | Status |
|---------|-----|------|-------|------------------|--------|
| Mom | @mom | assets/characters/mom_sheet_v2.png | — | auburn shoulder-length hair, green apron, gold ring left hand | final |
| David | @david | assets/characters/david_v1.png | 0.99× base; crown ≈ Saul's chin, ≈ Goliath's navel | rosy complexion, slight wiry youth, sheepskin mantle left shoulder | final |
| Goliath | @goliath | assets/characters/goliath_v1.png | 1.86× base; ~2× shoulder width; Saul's crown ≈ his mid-chest | colossal mass, bronze scale armor, heavy brow, thick dark beard | final |

## Locations
| Element | Tag | File | Scale | Critical details | Status |
|---------|-----|------|-------|------------------|--------|
| Adel's room | @adels_room | assets/locations/adels_room_v1.png | — | bed left wall under window, desk far right, blue walls | final |

## Props
| Element | Tag | File | Scale | Critical details | Status |
|---------|-----|------|-------|------------------|--------|
| TV remote | @remote | assets/props/remote_v3_arrow.png | hand-sized | red arrow marks the green power button, upper left | final |

## Scale references
| Element | Tag | File | Covers | Status |
|---------|-----|------|--------|--------|
| Cast scale lineup | @cast_scale | assets/scale/cast_lineup_v1.png | David, Saul, Goliath, avg soldier — all principals, one ground line | final |
| David–Goliath lineup | @david_goliath_scale | assets/scale/david_goliath_v1.png | the face-off two-shot proportions | final |
```

**Column meanings:**

- **Element** — the human name used in conversation and scripts ("Mom", "Adel's room", "fantasy dragon").
- **Tag** — the `@tag` video prompts will use. Lowercase, underscores, short, unique. Derived from the element name once and never changed — prompts reference it forever.
- **File** — relative path to the accepted sheet/plate image. Keep assets under `assets/characters/`, `assets/locations/`, `assets/props/`, `assets/scale/`.
- **Scale** — the element's size relative to the project base unit, from the **asset-scale** Scale Bible: a ratio + the **landmark line(s)** for pairs it appears with ("crown ≈ Goliath's navel"), or a body-anchored size for props ("hand-sized", "taller than Saul"). Like Critical details, this is **restated in words** in every multi-character prompt, because sheets can't encode relative size. Leave `—` when the element never needs a size comparison.
- **Critical details** — the small, droppable details (logos, text, exact colors, marked buttons) that must be **restated in words** in every video prompt even though they're on the reference image. This column exists because generation drops small details; whoever writes the prompt copies these into the text. Include a recurring cameo's **locked signature features** here.
- **Status** — `draft` (generated, not yet accepted), `final` (passed QA, safe to reference), `retired` (superseded — note the replacement).

**Scale references** are their own element type: single-pass lineup images (from **asset-scale**) that lock relative size. Upload the relevant lineup alongside the identity sheets in any multi-character shot. They carry no "critical details" of their own — their whole job is proportion.

---

## REGISTRATION RULES

1. **Register at finalization, not before.** An asset enters as `final` only after passing its QA checklist (each asset skill defines its own). Work-in-progress sheets may sit as `draft` but never get referenced in video prompts.
2. **One element, one tag, forever.** Renaming a tag silently breaks every prompt written so far. To change an asset, add a new versioned file and update the File column — the tag stays.
3. **Versions in filenames, not new elements.** `mom_sheet_v3.png` replaces `v2` in the File column. A genuinely different character (Mom in winter clothes behaving as a distinct reference) is a new element with a new tag (`@mom_winter`).
4. **Fill "Critical details" at registration time**, while the QA pass is fresh — that's when you know exactly which small details the video prompts must restate.
   - **Fill "Scale" from the asset-scale Scale Bible** at the same time — the ratio plus the landmark line(s) for the pairs this element shares a frame with. Register the project's cast-lineup image(s) as `scale reference` elements.
5. **Annotated variants are separate rows** when they serve a different purpose: the arrow-marked remote for the button-press shot is its own row if the clean remote is also used elsewhere.

---

## SERVING PROMPT-WRITERS

When someone writes a video prompt (e.g. with the seedance-clean skill), the librarian's job is lookup:

- Confirm the element exists and is `final`.
- Hand over the **Tag** (for the reference) and the **Critical details** (to restate in the prompt text).
- For a **multi-character shot**, also hand over each element's **Scale** line and the matching **scale reference** tag (e.g. `@cast_scale`) to upload alongside — the sheets alone can't hold relative size.
- If a needed element is missing or still `draft` — flag it and route to the matching asset skill (**asset-character**, **asset-location**, **asset-prop**, or **asset-scale** for a missing lineup) instead of letting the prompt improvise a description.

Keep the manifest sorted and clean: it is read far more often than it is written.
