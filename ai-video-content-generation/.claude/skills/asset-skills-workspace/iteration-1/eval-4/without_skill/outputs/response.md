# Asset tracking set up for Pancake Run

Your three approved assets are now registered. I created two files at the project root:

## 1. `asset_manifest.json` — the source of truth
A machine-readable registry with one entry per asset. Each entry records:

- **`id` / `tag`** — the short handle you use in prompts (`@mom`, `@kitchen`, `@pan`)
- **`type`** — character / location / prop
- **`file` + `version`** — which PNG is current (`mom_sheet_v2.png`, `kitchen_v1.png`, `pan_v3_arrow.png`)
- **`status`** — all three are `approved`, meaning they're cleared for use in video prompts
- **`canonical_features`** — the details that must stay consistent (mom's red polka dot apron and round glasses; the pan's red arrow noted as a grip *annotation*, not part of the prop)
- **`prompt_usage`** — a ready-made instruction for how to invoke the asset in a video prompt
- **`history`** — version log so you can bump versions later without losing track

## 2. `ASSETS.md` — the human-readable companion
A quick-reference table plus per-asset notes and the referencing rules. Glance at this while writing prompts.

## How your video prompts should reference these

1. Attach the asset's PNG as an image reference for every asset in the shot.
2. Use the tag in the prompt text, e.g.:
   > The mom (@mom, exactly as shown in the character reference) stands at the stove in the kitchen (@kitchen). She grips the frying pan (@pan) at the point indicated by the red arrow in the prop reference — the arrow is an annotation and must not appear in the video.
3. Don't re-describe approved assets from scratch — the reference image defines the look; the prompt only describes what changes (pose, action, camera, lighting).

## Two things worth flagging

- **The pan's red arrow**: it's registered as an annotation marking the handle grip point. Every prompt that uses `@pan` for a hand interaction should point at the arrow *and* state that the arrow must not render in the output. The manifest's `prompt_usage` field already includes this wording.
- **Versioning going forward**: when you regenerate an asset, save it as `<id>_v<n+1>.png`, update `file`/`version` in the manifest, and append to `history`. Old versions stay on disk as superseded — never reference them in prompts.

Drop the three PNGs next to these files (or move everything into an `assets/` folder and update the `file` paths) and you're ready to write shot prompts.
