# Pancake Run — Asset Registry

Human-readable companion to `asset_manifest.json` (the machine-readable source of truth).
Last updated: 2026-07-19

## Quick reference table

| Tag | Type | File | Ver | Status | Key details |
|---|---|---|---|---|---|
| `@mom` | Character | `mom_sheet_v2.png` | v2 | Approved | Red polka dot apron, round glasses |
| `@kitchen` | Location | `kitchen_v1.png` | v1 | Approved | Primary set for pancake scenes |
| `@pan` | Prop | `pan_v3_arrow.png` | v3 | Approved | Red arrow marks the handle grip point (annotation only) |

## How to reference assets in video prompts

1. **Attach the file** listed above as an image reference for every asset appearing in the shot.
2. **Use the tag in prompt text**, e.g.:
   > The mom (@mom, exactly as shown in the character reference) stands at the stove in the kitchen (@kitchen, matching the location reference). She grips the frying pan (@pan) at the point indicated by the red arrow in the prop reference. Note: the red arrow is an annotation and must not appear in the video.
3. **Do not re-describe approved assets from scratch.** The reference image is the source of truth; only describe what changes in the scene (pose, action, lighting, camera).
4. **Only reference `approved` assets.** Drafts and superseded versions (e.g. `mom_sheet_v1`) must not be used in prompts.

## Per-asset notes

### @mom — Mom (character)
- File: `mom_sheet_v2.png` (v2, approved; v1 superseded)
- Canonical look: red polka dot apron, round glasses. These must stay consistent across all shots unless a scene explicitly changes wardrobe.

### @kitchen — Kitchen (location)
- File: `kitchen_v1.png` (v1, approved)
- Use as the environment reference; keep layout and set dressing consistent with the image.

### @pan — Frying Pan (prop)
- File: `pan_v3_arrow.png` (v3, approved)
- The red arrow is a **grip annotation**, not part of the prop's design. When prompting hand interactions, direct the model to grip at the arrow's location, and explicitly state the arrow itself must not render in the output.

## Updating this registry

- New version of an asset: save as `<id>_v<n+1>.png`, update `file`/`version` in `asset_manifest.json`, append an entry to that asset's `history`, and update the table here. Keep old files for rollback; mark old versions superseded.
- New asset: add an entry to `asset_manifest.json` with a unique `id`/`@tag`, then mirror it here once approved.
- Keep the reference PNGs alongside these files in the project root (or update the `file` fields to relative paths if you move them into an `assets/` folder).
