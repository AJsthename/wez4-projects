# Character Assets: Adel + Goblin Minions

Below are ready-to-use image generation prompts for your two character assets, plus guidance on how to use them for consistent AI video generation.

---

## Asset 1: Adel (Main Character)

### Primary prompt — Character reference sheet

> Character reference sheet of Adel, a 9-year-old girl, on a plain neutral light-gray studio background. Full-body turnaround showing three views side by side: front view, side profile view, and back view, all in a relaxed neutral standing pose. Adel has messy dark brown curly hair falling just past her chin, warm brown eyes, light olive skin, a round curious face with faint freckles across her nose, and slightly gapped front teeth visible in a small inquisitive smile. She wears a bright canary-yellow raincoat with a hood down, oversized snap buttons, and a slightly-too-long hem, over a striped navy-and-white t-shirt, dark leggings, and scuffed red rubber boots. Soft, even studio lighting, no shadows on the background, consistent proportions across all three views. Cinematic animation style, high detail, clean silhouette. No text, no labels, no watermark.

### Secondary prompt — Expression sheet (recommended)

> Expression sheet of Adel, a 9-year-old girl with messy dark brown curly hair, warm brown eyes, light olive skin, faint freckles, wearing a bright canary-yellow raincoat with the hood down. Plain neutral light-gray background. A grid of six head-and-shoulders portraits of the same girl, identical face and outfit in each, showing six distinct expressions: 1) wide-eyed curiosity, leaning forward slightly; 2) delighted open-mouth wonder; 3) determined frown with furrowed brows; 4) scared, biting her lip; 5) mischievous sideways grin; 6) laughing with eyes squeezed shut. Soft even studio lighting, consistent proportions and identical character across all six portraits. Cinematic animation style, high detail. No text, no labels, no watermark.

### Optional — Costume variant (hood up, in the rain)

> Adel, a 9-year-old girl with messy dark brown curly hair escaping from under the hood of her bright canary-yellow raincoat, hood pulled up, raindrops beading on the coat. Warm brown eyes, light olive skin, faint freckles, curious expression looking up. Three-quarter body shot, plain neutral gray background, soft even lighting. Cinematic animation style, high detail, consistent with her character reference. No text, no watermark.

**Note:** Since she wears the raincoat in "most scenes" but not all, if any scene shows her without it, generate one more variant sheet of Adel in just the striped navy-and-white t-shirt and dark leggings (same face, hair, boots) so your video model has a reference for those scenes too.

---

## Asset 2: Goblin Minions (Scene 3 chase group)

For a group of minions you want them to read as a *swarm of the same species* with slight individual variation — so the prompt establishes one shared design language, then allows small differences.

### Primary prompt — Goblin minion reference sheet

> Character reference sheet of a goblin minion on a plain neutral light-gray studio background. Full-body turnaround showing three views: front, side profile, and back, in a hunched neutral stance. The goblin is small, about knee-to-waist height on a child, roughly 60 cm tall, with mottled moss-green warty skin, oversized bat-like pointed ears, a long crooked nose, bulging amber eyes, a wide mouth crowded with tiny needle teeth, spindly arms with long-fingered grabby hands, bandy legs, and bare four-toed feet. It wears a ragged patchwork tunic of dull brown burlap tied with a frayed rope belt. Comedic-menacing, more pesky than terrifying — suitable for a children's adventure film. Soft even studio lighting, consistent proportions across all views. Cinematic animation style matching a family adventure film, high detail. No text, no labels, no watermark.

### Secondary prompt — Goblin horde variation sheet

> Group lineup sheet of five goblin minions standing side by side on a plain neutral light-gray background, all clearly the same species: small (about 60 cm tall), mottled moss-green warty skin, oversized bat-like pointed ears, long crooked noses, bulging amber eyes, needle teeth, spindly limbs, ragged brown burlap tunics with rope belts. Each goblin has one small distinguishing trait: one is slightly fatter with a torn ear; one is taller and lankier with a snaggletooth; one is tiny and wears a rusted tin can as a helmet; one has a milky blind left eye; one carries a crooked wooden stick. Varied energetic poses — sneaking, snarling, scampering, pointing, cackling. Comedic-menacing tone for a children's adventure film. Soft even studio lighting, consistent style and proportions. Cinematic animation style, high detail. No text, no labels, no watermark.

### Optional — Chase action reference

> Five goblin minions mid-sprint in a chaotic chase, seen from a low three-quarter angle: small moss-green warty goblins with oversized pointed ears, long crooked noses, bulging amber eyes, ragged brown burlap tunics, arms outstretched and grabbing, tongues out, tripping over each other. Plain neutral gray background, motion-suggesting poses but sharp focus, soft even lighting. Comedic-menacing, children's adventure film tone. Cinematic animation style consistent with the goblin reference sheet. No text, no watermark.

---

## Guidance for using these assets

**1. Lock the style first.** Both prompts say "cinematic animation style" as a placeholder — replace this in *every* prompt with your film's actual look, using identical wording each time, e.g. "3D animated feature film style, Pixar-like soft subsurface skin, warm color grade" or "2D hand-painted Ghibli-inspired watercolor style." Inconsistent style words are the #1 cause of assets that don't cut together.

**2. Generate Adel first, then judge the goblins against her.** The goblins must feel like they live in the same movie — same rendering style, same level of detail, compatible proportions. If your image tool supports reference images, feed Adel's sheet in when generating the goblins.

**3. Use the sheets as reference images for video.** Most AI video tools (Runway, Kling, Veo, Pika, etc.) accept a reference/first-frame image. Use the character sheet (or a clean single-view crop from it) as the identity anchor for every shot featuring that character, and re-describe the key identity features ("messy dark curls, yellow raincoat") in each video prompt as a backup.

**4. Neutral background matters.** The plain gray background makes the sheets clean identity references — the video model won't get confused by environment details bleeding in.

**5. Scale reference for scene 3.** The goblin prompt pins their height relative to a child (~60 cm / knee-to-waist on Adel). When you prompt the chase shots, restate this ("goblins half Adel's height") so the video model doesn't scale them up into full-size monsters.

**6. Quality checklist before accepting a generation:**
- Same face/character in all views of a sheet (this is the most common failure — regenerate if the three views look like siblings rather than the same character)
- No accidental text, labels, or watermarks
- Adel reads as 9 years old, not a teenager
- Raincoat is a consistent shade of yellow across views
- Goblins read as pesky/comedic, not nightmare fuel (unless your film wants that — if so, drop the "comedic-menacing" line and add "sinister, feral")
- All five goblins in the horde sheet are clearly the same species

**7. Aspect ratio.** Generate sheets in landscape (16:9 or 3:2) so the turnaround views fit side by side without cropping.
