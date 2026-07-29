# Character Assets: Adel + Goblin Minions

Two separate sheets are needed: one for your main character Adel, and one **group variation sheet** for the goblin minions (they appear as a group in scene 3, so a single goblin reference would produce an "army of clones" in the video — the sheet must show distinct variations of the same goblin type).

---

## Asset 1 — Adel (main character)

```
Character reference sheet on a solid mid-gray studio background, even soft lighting.
Three views of the same character, consistent across all views:
[1] front-facing close-up portrait of the face,
[2] full-body front view showing the complete outfit,
[3] full-body three-quarter back view showing the raincoat hood and back.
Character: 9-year-old girl, small slim build, light-brown skin, messy dark curly hair
falling just past her ears with loose strands sticking out, large curious brown eyes,
faint freckles across the nose, eyebrows slightly raised in an alert, inquisitive expression.
Wearing a bright yellow rubberized raincoat with a hood down, slightly oversized with
rolled cuffs and a few small scuffs, over a plain white t-shirt, dark blue leggings,
and mud-flecked red rubber rain boots.
Neutral standing pose, arms relaxed. Clean sheet layout, no text labels, no props, no scenery.
```

### QA checklist — accept or reject Adel's sheet

- **Same girl in every view?** Face shape, curl pattern, and raincoat details (cuffs, scuffs, hood) must match across all three views. Any drift → reject.
- **Face view clear and large?** The front close-up is the identity anchor — if it's small, soft, or shadowed → reject.
- **Outfit fully visible head to toe?** Boots to hood, nothing cropped or occluded.
- **Back view shows the hood?** The raincoat hood is her defining back-side feature; if the 3/4 back view hides it → reject.
- **Hair reads "messy"?** If the curls come out neat and styled, regenerate — messy is part of her identity.
- **Age reads as ~9?** AI models drift older; if she reads as a teenager → reject.
- **Background actually solid mid-gray?** Gradients, scenery, or props sneaking in → reject.

Note: since the yellow raincoat is worn "in most scenes" but not all, this sheet locks her raincoat look. If a later scene shows her without the raincoat, generate a second outfit sheet then — don't overload this one.

---

## Asset 2 — Goblin minions (group, scene 3)

Because they appear as a chasing pack, this sheet uses the group-variation layout: 4 distinct goblins sharing the same species and faction traits, differing in what reads at a distance.

```
Character reference sheet on a solid mid-gray studio background, even soft lighting.
Four distinct variations of a goblin minion standing side by side, same species and
same ragged war-band, each differing in height, build, ear shape, posture, and gear wear:
[1] short and pot-bellied, one chipped ear, hunched posture,
[2] tall and wiry, long crooked nose, upright and twitchy,
[3] squat and muscular, heavily scarred arms, aggressive stance,
[4] scrawny runt, oversized ears, skittish crouch.
All four share: mottled green warty skin, pointed ears, yellow eyes, sharp crooked teeth,
and matching ragged dark-brown leather scraps with crude rust-red cloth armbands
marking their war-band. Full-body front views.
Clean sheet layout, no text labels, no props, no scenery.
```

### QA checklist — accept or reject the goblin sheet

- **Genuinely distinct?** If any two goblins could be twins, regenerate with stronger stated differences (push height and silhouette contrast first).
- **Still the same species/faction?** All four must share the green warty skin, pointed ears, and rust-red armbands — the shared traits are what makes them read as one pack.
- **Silhouettes differ at a distance?** Squint test: four distinguishable outlines. This is what prevents the clone-army look in the chase shots.
- **Full bodies visible?** Feet to ear-tips, no cropping or occlusion between figures.
- **Background actually solid mid-gray?** Reject anything with scenery or gradients.

Reject fast and regenerate in batches — a flawed sheet poisons every downstream shot.

---

## Next step

Once each sheet passes QA, register the accepted images as named elements via the asset librarian so your video prompts can reference them by tag. Suggested names: `Adel` and `goblin_minion` — short, unique, memorable. In your scene 3 video prompt you'd then reference `@Adel` and `@goblin_minion` instead of re-describing them.
