# Pancake Run — Asset Registry Set Up

All three approved assets are now registered as elements in the project manifest at `assets/MANIFEST.md`. Your video prompts can reference them by their `@tag` from now on.

## Registered elements

| Element | Tag | File | Critical details | Status |
|---------|-----|------|------------------|--------|
| Mom | `@mom` | `assets/characters/mom_sheet_v2.png` | red polka dot apron, round glasses | final |
| Kitchen | `@kitchen` | `assets/locations/kitchen_v1.png` | — | final |
| Frying pan (arrow-marked) | `@pan_arrow` | `assets/props/pan_v3_arrow.png` | red arrow points at the handle grip | final |

## What was created

- `assets/MANIFEST.md` — the single registry for this project. It is the source of truth for every finalized character, location, and prop.
- `assets/characters/`, `assets/locations/`, `assets/props/` — the folder structure the manifest expects.

## One action needed from you

Move the three image files into their manifest locations so the paths resolve:

- `mom_sheet_v2.png` → `assets/characters/mom_sheet_v2.png`
- `kitchen_v1.png` → `assets/locations/kitchen_v1.png`
- `pan_v3_arrow.png` → `assets/props/pan_v3_arrow.png`

## How to use this when writing video prompts

1. **Reference by tag.** Attach the file from the manifest as the reference image and refer to the element as `@mom`, `@kitchen`, or `@pan_arrow` in the prompt.
2. **Restate the critical details in words.** Video generation drops small details even when they are on the reference image, so every prompt featuring Mom should still say "red polka dot apron, round glasses" in the text, and any shot using the marked pan should say "red arrow points at the handle grip." That is exactly what the Critical details column is for — copy it into the prompt.
3. **Tags never change.** If you later upgrade Mom to `mom_sheet_v3.png`, only the File column gets updated — the `@mom` tag stays, so no existing prompt breaks.
4. **The arrow-marked pan is its own element.** `@pan_arrow` is specifically for the shot(s) that need the handle-grip callout. If you later generate a clean, unmarked pan for general cooking shots, we register it as a separate element (e.g. `@pan`) rather than overwriting this one.

All three assets are marked `final` since you approved them, which means they are safe to reference in video prompts immediately.
