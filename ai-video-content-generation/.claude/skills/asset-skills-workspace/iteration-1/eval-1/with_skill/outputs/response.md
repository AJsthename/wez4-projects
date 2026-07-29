# Prop Asset: Chunky 90s TV Remote (with power-button interaction arrow)

Since the grandma has to press the power button on camera, this sheet needs two things beyond a normal prop sheet: the power button locked down in exact words (position, color, shape), and a red arrow pointing at it so the video model knows precisely where her thumb goes.

## Image-Generation Prompt

```
Product-style reference sheet of a chunky 1990s TV remote control on a solid mid-gray
studio background, even soft studio lighting, soft shadows grounding the object,
subtle studio reflections on the plastic surfaces.
Four views of the same remote, consistent across all views:
[1] front view (button side facing camera), [2] back view showing the battery
compartment cover, [3] side profile showing the thick wedge-shaped body,
[4] three-quarter view with a bold red arrow pointing directly at the large round
red power button in the top-left corner of the button panel.
Object: a large, thick handheld remote about the length of an adult hand, heavy
1990s design; matte dark-gray plastic body with slightly rounded edges, faint
scuffs and worn glossy spots from years of use; dense grid of many small rubber
buttons — rows of gray number buttons 0–9, smaller black function buttons, and a
tall volume rocker and channel rocker near the middle; the power button is clearly
the biggest button on the remote: a large round bright-red rubber button, alone at
the top-left, visibly larger than every other button, with a small white power
symbol printed on it; dark translucent infrared window at the top edge.
Clean sheet layout, no text labels, no hands, no scenery.
```

## Why the sheet is built this way

- **Four views on mid-gray:** the video model gets front, back, side, and three-quarter references to hold onto instead of hallucinating unseen angles; gray stays neutral against any scene lighting.
- **Volume cues prompted in** (shadows, studio reflections, plastic texture, wear marks): a flat-looking reference produces cardboard-cutout artifacts once the model moves the remote through 3D space.
- **Power button described exactly** (largest button, round, bright red, top-left, white power symbol, isolated from the other buttons): small details are the first thing generation drops — the sheet is where this gets locked so the press-shot reads instantly.
- **Red arrow on the three-quarter view:** the field-tested hack for interaction points. One arrow, one target — it tells the video model exactly where the grandma's hand goes. If the generator fights the arrow, generate the clean sheet first, accept it, then add the arrow in an edit pass.

## QA Checklist — accept or reject the generated sheet

- **Volume test first:** does it look like a real object photographed in a studio — visible thickness in the side view, shadows under it, soft reflections on the plastic? Flat/sticker-like → reject.
- **Same remote in every view?** Button count, button grid layout, rocker positions, proportions, and wear marks must match across all four views. Back view inventing new geometry → reject.
- **Power button correct and dominant?** Large, round, red, top-left, clearly the biggest button, visible in at least the front and three-quarter views. If it blends into the button grid or moved position → reject (the whole shot depends on it).
- **Background actually solid mid-gray?** Scenery, textured surfaces, or gradient backdrops → reject.
- **Arrow unambiguous?** One bold red arrow pointing at exactly the power button and nothing else. Pointing vaguely at the button cluster → reject or fix in an edit pass.

Reject fast and regenerate in batches — a prop sheet is cheap, broken prop continuity across the video is not.

## After acceptance

Register the accepted sheet with the asset-librarian skill (suggested element name: `tv_remote_90s`) so video prompts can reference it by `@tag` instead of re-describing it. For the press shot, reference the annotated three-quarter view so the model sees the arrow.
