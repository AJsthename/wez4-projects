# Acts 23 — Prop Assets: Triage, Descriptions & Generation Prompts

**Project:** 90-Second Humorous Clip on Acts 23
**Style:** Realism/Hyperrealism
**Status:** Triage locked · 5 sheets to generate · Prompts ready
**Sheet standard:** Product-style on solid mid-gray background · four views (front, back, side, 3/4) · visible volume cues (soft shadows, studio reflections, surface texture) · scale stated · no hands, no readable text, no scenery

---

## Triage Result (from the original 10-prop list)

| Prop | Verdict | Reason |
|---|---|---|
| Futuristic Juice Pipe | **SHEET — Priority 1** | Invented object, 3 of 6 scenes, close-ups, held constantly |
| Chips Bag | **SHEET — Priority 1** | Invented packaging, 3 of 6 scenes, close-up snacking |
| Hunger Strike Signs | **SHEET — Priority 1** | Redesigned as pictogram banner (see below) |
| Tablet/Scroll Hybrid | **SHEET — Priority 2** | Invented hybrid, 2 scenes; models reinvent it per shot without a lock |
| Golf Club + Ball | **SHEET — Priority 2** | Invented "ancient-style" club, punchline-scene sight gag |
| Sushi Plate | Inline | Generic object, one scene, desk dressing |
| Golf Ball | Folded into golf sheet | Plain white ball needs no standalone reference |
| Roman Chains | Inline | One scene, half-occluded; chains render badly in AI video regardless of reference |
| Palace Food Tray | Inline | Generic luxury tray, set dressing |
| Military Escort Props | **CUT** | The 470-soldier escort appears in no scene of the 90-second plot |

**Locked design decisions:** signs → pictogram banner (no text) · juice pipe → spiral-straw tumbler, blue glow · tablet-scroll → wooden rollers + glowing screen · golf → single club + ball on one sheet · chips bag → abstract holographic, no readable text · no red-arrow annotations needed (all interactions are broad gestures).

---

## 1. Futuristic Juice Tumbler — Priority 1

### Description

Hand-sized translucent frosted tumbler, sleek minimal futuristic design. Visible orange juice inside (sells "juice" in one frame). Oversized clear spiral straw winding up from the lid to a mouthpiece with a soft blue light accent. Softly glowing blue light ring around the base — matches TT#1's blue accent scheme (jacket seam, smartwatch). No buttons, no text. Scale: fits comfortably in one hand.

### Image-Generation Prompt

```
Product-style reference sheet of a futuristic juice tumbler on a solid mid-gray studio
background, even soft studio lighting, soft shadows grounding the object, subtle studio
reflections, photorealistic.
Four views of the same object, consistent across all views:
[1] front view, [2] back view, [3] side profile, [4] three-quarter view.
Object: a hand-sized translucent frosted-glass drinking tumbler with a sleek minimal
futuristic design, filled with visible orange juice, an oversized clear spiral straw
winding upward from the lid to a mouthpiece with a soft blue light accent, and a softly
glowing blue light ring around the base. Smooth matte-frosted surface, no buttons,
no readable text, no logos.
Clean sheet layout, no text labels, no hands, no scenery.
```

### QA Checklist

- [ ] Volume test: reads as a photographed physical object — visible shadows, reflections, refraction in the frosted glass. Flat/sticker look → reject
- [ ] Same tumbler in all four views: straw spiral count, glow ring position, lid shape must match
- [ ] Juice clearly visible and orange in every view
- [ ] Exactly one glow ring (base) + one glow accent (mouthpiece) — reject extra lights
- [ ] No text, logos, or buttons anywhere
- [ ] Background solid mid-gray

---

## 2. Futuristic Chips Bag — Priority 1

### Description

Hand-sized pillow-shaped snack bag, full and plump (pristine state — crumpling is per-shot direction). Iridescent holographic foil shifting silver → violet → blue. Abstract geometric triangular pattern on the front — **no readable text or logos anywhere** (AI garbles text; abstract stays consistent). Crisp factory-sealed crimped edges top and bottom. Catches light dramatically — this bag should sparkle in the dark conspiracy chamber.

### Image-Generation Prompt

```
Product-style reference sheet of a futuristic snack chips bag on a solid mid-gray studio
background, even soft studio lighting, soft shadows grounding the object, subtle studio
reflections, photorealistic.
Four views of the same object, consistent across all views:
[1] front view, [2] back view, [3] side profile, [4] three-quarter view.
Object: a hand-sized pillow-shaped snack chips bag, full and plump, made of iridescent
holographic foil shifting between silver, violet and blue, printed with an abstract
geometric triangular pattern, with crisp factory-sealed crimped edges at the top and
bottom. Light-catching metallic foil creases. No readable text, no letters, no logos.
Clean sheet layout, no text labels, no hands, no scenery.
```

### QA Checklist

- [ ] Volume test: bag looks plump and air-filled with real foil creases and reflections — reject flat renders
- [ ] Same bag in all views: pattern style, seal edges, proportions match
- [ ] Zero readable characters — models love inventing brand names on packaging; any letters → reject
- [ ] Holographic silver-violet-blue shift visible
- [ ] Background solid mid-gray

---

## 3. Hunger-Strike Pictogram Banner — Priority 1

### Description

Rough rectangular banner of undyed beige woven linen, stretched between two simple dark wooden sticks. Hand-painted in dark brown pigment: a large round bread loaf crossed out by a bold X. Slightly crooked, handmade brushwork; frayed cloth edges. **No letters or writing anywhere** — the pictogram IS the message. Made by zealots, not designers. Period-plausible materials keep modern iconography exclusive to the time travelers.

### Image-Generation Prompt

```
Product-style reference sheet of a handmade protest banner on a solid mid-gray studio
background, even soft studio lighting, soft shadows grounding the object, subtle studio
reflections, photorealistic.
Three views of the same object, consistent across all views:
[1] front view held upright, [2] back view showing the blank reverse of the cloth,
[3] three-quarter view.
Object: a rough rectangular banner of undyed beige woven linen cloth stretched between
two simple dark wooden hand-held sticks, hand-painted in dark brown pigment with a large
round bread loaf crossed out by a single bold X, slightly crooked handmade brushwork,
frayed cloth edges, first-century materials. No letters, no writing, no symbols other
than the crossed-out bread loaf.
Clean sheet layout, no text labels, no hands, no scenery.
```

### QA Checklist

- [ ] Pictogram unambiguous: reads as "bread, forbidden" in half a second — if the loaf looks like a rock or the X is faint → reject
- [ ] Zero letters or extra symbols — models may add "NO!" or glyphs; any writing → reject
- [ ] Cloth has visible weave texture and frayed edges (handmade, not printed)
- [ ] Same banner in all views; back view is blank cloth
- [ ] Background solid mid-gray

---

## 4. Tablet-Scroll Hybrid — Priority 2

### Description

An open scroll the size of an open magazine: two dark wooden rollers with polished brass end caps at top and bottom, and stretched between them a thin, flexible, softly glowing pale-blue screen displaying faint unreadable glyphs. Held two-handed like a scroll, lit like a tablet — the gag must read in a single frame. Wood grain and brass reflections sell the "ancient" half; the even screen glow sells the "tech" half.

### Image-Generation Prompt

```
Product-style reference sheet of an ancient scroll and digital tablet hybrid device on a
solid mid-gray studio background, even soft studio lighting, soft shadows grounding the
object, subtle studio reflections, photorealistic.
Four views of the same object, consistent across all views:
[1] front view, [2] back view, [3] side profile, [4] three-quarter view.
Object: an open scroll the size of an open magazine, with two dark polished wooden rollers
capped with brass at the top and bottom, and stretched between the rollers a thin flexible
softly glowing pale-blue digital screen displaying faint unreadable glyphs. Visible wood
grain on the rollers, warm brass reflections, even cool glow from the screen. The back
view shows plain parchment-like backing behind the screen.
Clean sheet layout, no text labels, no hands, no scenery.
```

### QA Checklist

- [ ] The hybrid reads instantly: wooden scroll + glowing screen visible in the same view — if it looks like just a scroll or just a tablet → reject
- [ ] Volume test: wood grain, brass highlights, screen glow casting faint light — flat look → reject
- [ ] Same object in all views: roller caps, proportions, screen tone match
- [ ] Screen glyphs stay faint and unreadable (intentional gibberish is fine; real words are not)
- [ ] Background solid mid-gray

---

## 5. Ancient Golf Club + Ball — Priority 2

### Description

One driver-style club: polished dark wooden shaft, hammered bronze club head with visible hammer-mark texture, leather-wrapped grip with visible stitching. Next to it, a plain white regulation golf ball with dimples. Club scaled for a standing adult swing (~1.1 m). The bronze-and-leather materials say "ancient," the silhouette says "golf" — both must survive every view.

### Image-Generation Prompt

```
Product-style reference sheet of an ancient-style golf club and golf ball on a solid
mid-gray studio background, even soft studio lighting, soft shadows grounding the objects,
subtle studio reflections, photorealistic.
Four views of the same two objects, consistent across all views:
[1] front view, [2] back view, [3] side profile, [4] three-quarter view.
Objects: a driver-style golf club with a polished dark wooden shaft, a hammered bronze
club head with visible hammer-mark texture, and a leather-wrapped grip with visible
stitching, scaled for a standing adult swing; displayed beside it, a plain white
regulation golf ball with dimples.
Clean sheet layout, no text labels, no hands, no scenery.
```

### QA Checklist

- [ ] Silhouette unmistakably golf club (driver shape) — if it drifts toward walking stick, mace, or hockey stick → reject
- [ ] Bronze head shows hammered texture and metallic reflections; shaft shows wood grain
- [ ] Same club in all views: head shape, grip length, proportions match
- [ ] Ball is plain white with dimples, correct scale relative to club head
- [ ] Background solid mid-gray

---

## Inline Descriptions (no sheet — paste into scene/location prompts)

- **Sushi plate (Commander's office):** "a lacquered black plate of assorted sushi rolls and nigiri with chopsticks resting across it, sitting on the desk"
- **Roman chains (Paul, Scene 5):** "loose iron manacles on his wrists with a short broken chain dangling from each, clearly not restraining him"
- **Palace food tray (Scenes 5–6):** "a polished brass tray piled with fresh figs, grapes, bread and a golden goblet of juice"
- **Paul's drink (Scene 5):** "sipping from a golden goblet"
- **Commander's coffee cup (optional desk dressing):** "a modern white ceramic coffee cup steaming on the desk"

---

## Generation & Handoff Workflow

1. **Generate** 2–4 candidates per prop, QA against the checklists, reject fast.
2. **Register** accepted sheets as named elements. Suggested tags: `juice_tumbler`, `chips_bag`, `hunger_banner`, `scroll_tablet`, `golf_set`.
3. **Remaining asset pass:** the 4 location assets (Conspiracy Chamber, Commander's Office, Herod's Palace room, Sanhedrin Court).

---

_Supersedes the prop table in the production plan: escort props cut; signs redesigned as pictogram banner; sushi, chains, food tray and golf ball moved to inline descriptions._
