# Prop Asset: Chunky 90s TV Remote (with hero power button)

## Primary image-generation prompt

```
Product reference photo of a single chunky 1990s television remote control, studio prop photography, shot straight-on from above (top-down view) on a plain neutral light-gray seamless background, soft even lighting, no shadows cutting across the buttons.

The remote: oversized and thick, roughly 22 cm long and 6 cm wide, heavy matte dark charcoal-gray plastic body with slightly rounded edges, faint wear and scuffing on the corners, visible seam line along the sides, a slotted battery cover on the back implied by its bulk. Dense grid of many small rubber buttons: a full 0-9 number pad with worn white printed digits, gray volume up/down rocker, gray channel up/down rocker, a row of four small rectangular function buttons (MENU, MUTE, AV, TXT) in faded pastel green, yellow and blue, and a small dark red record dot button. Small printed white labels under each button, slightly yellowed with age. Fake brand text "TELEMAX 2000" printed in silver near the bottom. A dark translucent IR window at the top edge.

HERO FEATURE - the power button: one single, unmistakably large round POWER button at the very top of the button layout, centered, clearly the biggest button on the remote (about three times the size of any other button), bright glossy red rubber, slightly domed, with a bold white power symbol (circle with vertical line) printed on it and the word "POWER" in white letters directly beneath it. Generous empty spacing around the power button so it stands apart from the dense button grid below it. No other red round buttons anywhere near it.

Photorealistic, sharp focus across the entire remote, high detail on button textures and printed labels, neutral white balance, catalog / prop-department reference style, the remote fills most of the frame, nothing else in the image.
```

## Optional second angle (same prop, for consistency)

If your video model accepts multiple reference images, generate a matching 3/4 perspective view so the model understands the remote's thickness:

```
Same prop, second reference angle: the identical chunky 1990s remote control ("TELEMAX 2000", matte dark charcoal-gray plastic, dense small rubber buttons, one oversized glossy red domed POWER button at the top with a white power symbol and "POWER" label), now shown at a 3/4 angle resting on the same plain neutral light-gray background, revealing its thick body height of about 3 cm and the slotted battery cover on the underside edge. Studio prop photography, soft even lighting, photorealistic, sharp focus, catalog reference style.
```

## Guidance for the shot where grandma presses the power button

- **Why the prompt is built this way:** The power button is described with five redundant disambiguators (largest button, top-center position, red color, round/domed shape, white power symbol + "POWER" text, isolation spacing). Video models latch onto whichever cue survives generation, so stacking them makes "press THE power button" reliably targetable.
- **Deliberately avoided:** No other red or round buttons in the layout, so nothing competes with the hero button. Keep it that way if you edit the prompt.
- **Framing:** Top-down flat view is the most useful single reference for a press interaction — it shows the exact button layout the video model must reproduce. Add the 3/4 view only if your pipeline supports multiple refs.
- **In your video prompt later,** reference the button the same way: "the large round red POWER button at the top of the remote" — matching the wording of the asset prompt improves consistency.
- **QA the generated image before locking it in:** check that (1) the power button is visibly the largest button, (2) it is red and the only red round button, (3) the power symbol is legible, (4) labels aren't garbled beyond acceptability (small label gibberish is fine; the "POWER" label and brand text should be readable), (5) the remote reads as thick/chunky, not a slim modern remote. Regenerate if any of these fail.
- **Fake brand:** "TELEMAX 2000" is invented to avoid real-brand artifacts (e.g., the model drawing a Sony or Philips layout that overrides your button description). Swap it for any invented name you prefer.
