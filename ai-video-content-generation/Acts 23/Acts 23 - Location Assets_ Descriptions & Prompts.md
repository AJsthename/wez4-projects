# Acts 23 — Location Assets: Triage, Descriptions & Generation Prompts

**Project:** 90-Second Humorous Clip on Acts 23
**Style:** Realism/Hyperrealism
**Status:** Triage locked · 4 plates to generate · Prompts ready · Scene numbers updated to the final dialogue script
**Plate standard:** Empty of people · camera at a 3/4 angle showing two walls and depth (interiors) · spatial layout, not inventory · light source stated · every object physically grounded

---

## Triage Result (from the original 4-location list + the final script's new escort scene)

| Location | Verdict | Reason |
|---|---|---|
| Conspiracy Chamber | **PLATE — Priority 1** | 4 of 6 scenes; most-used location; invented specific space |
| Commander's Office | **PLATE — Priority 1** | Scene 3 cutaway; invented ancient/modern mash-up, model can't default to it |
| Herod's Palace (Paul's quarters) | **PLATE — Priority 1** | 2 scenes incl. finale; invented lounge+terrace layout for the golf gag |
| Night Road out of Jerusalem | **PLATE — Priority 2** | 1 scene only, but blocking depends on specific geometry (gate → road path → roadside spot for the time travelers), and mixed moon/torch night lighting is exactly where text-only generation improvises badly. Single scene = lower priority, not a skip. |
| Sanhedrin Court | **CUT** | Appears in no scene of the final script — trial exists only in commentary |

**Locked design decisions:** chamber → medium vaulted cellar (40+ men visibly overfill it) · office → Roman room with corporate desk island (executive desk + ergonomic chair + desk lamp) · palace → interior lounge opening onto garden terrace (golf ball has somewhere to go) · palace styling → period Roman luxury, no modern objects (anachronism ownership stays with time travelers + commander) · night road → gate in background right, road running diagonally past the camera (the column's marching path), foreground roadside verge as the time travelers' spectator spot.

**Lighting coding baked into the plates** (from the production plan): chamber = warm oil-lamp orange/brown · office = neutral grey-blue daylight · palace = golden afternoon light · night road = cool blue moonlight + warm torch pools.

---

## 1. Conspiracy Chamber — Priority 1

*Used in Scenes 1, 2, 3, 6 (split)*

### Description

Medium underground vaulted stone cellar — big enough for wide shots, small enough that 40+ men visibly overfill it. Two thick stone columns support a low vaulted ceiling. Long dark wooden table in the center with low benches. Clay oil lamps on iron wall brackets are the only light — warm flickering orange, deep shadows in the corners. A narrow stone staircase descends through an arched doorway in the far wall: this is the entrance the time travelers appear from/near in Scene 3. First-century Judean construction, no modern objects.

**Per-shot props (not in the plate):** hunger banners, chips bag, juice tumbler.

### Image-Generation Prompt

```
Underground stone conspiracy chamber, empty of people, camera at a three-quarter angle
into the room showing two walls and the depth of the space, eye-level, photorealistic.
Layout: rough-hewn stone walls with a low vaulted ceiling supported by two thick stone
columns; a long dark wooden table in the center of the room surrounded by low wooden
benches; on the left wall, a row of clay oil lamps on iron wall brackets casting warm
flickering light; in the far wall, a narrow stone staircase descending into the room
through an arched doorway; packed earth and stone floor with a few worn floor cushions
near the table.
Night, lit only by the oil lamps — warm orange and brown tones, deep shadows in the
corners, secretive tense mood. First-century Judean architecture, aged stone, aged wood,
no modern objects.
Every object physically grounded and logically placed.
```

### QA Checklist

- [ ] 3/4 depth: two walls and real depth visible — a flat wall-facing shot → reject
- [ ] Entrance staircase + arched doorway clearly present in the far wall (Scene 3 staging depends on it)
- [ ] All lamps mounted on brackets, brackets attached to wall; no floating flames or sourceless light pools
- [ ] Table and benches sit flat on the floor, columns actually reach the ceiling
- [ ] Light is warm orange and clearly comes FROM the lamps — shadow directions agree
- [ ] Room reads medium-small: 40 men would crowd it
- [ ] Zero people, zero modern objects
- [ ] Physics audit corner to corner — one floating object means the batch is sloppy → discard and regenerate

---

## 2. Roman Commander's Office — Priority 1

*Used in Scene 3 (wordless sushi cutaway, 0:45–0:51)*

### Description

A Roman stone fortress office with one deliberate anachronistic island in the middle: a sleek modern dark-wood-and-steel executive desk, a black leather ergonomic office chair behind it, and a small modern desk lamp on it. Everything else is period: stone columns, a red legion banner with a golden eagle on the far wall, a weapon rack with spears and shields on the left wall, tall narrow windows letting in flat grey-blue daylight, marble floor. Bureaucratic, neutral, slightly sterile mood.

**Per-shot props (not in the plate):** sushi plate, tablet-scroll, coffee cup.

### Image-Generation Prompt

```
Roman military commander's office inside a stone fortress, empty of people, camera at a
three-quarter angle into the room showing two walls and the depth of the space, eye-level,
photorealistic.
Layout: smooth stone walls with two stone columns; on the far wall, a large red Roman
legion banner with a golden eagle emblem hanging flat against the stone; on the left wall,
a wooden weapon rack holding spears and two shields; tall narrow windows high on the far
wall letting in flat daylight; in the center of the room, as a deliberate anachronism, a
sleek modern executive desk in dark wood and steel with a black leather ergonomic office
chair behind it and a small modern metal desk lamp standing on the desktop; polished
marble floor.
Overcast daylight from the high windows — neutral grey and blue tones, bureaucratic
slightly sterile mood. Everything Roman first-century except the modern desk, office
chair and desk lamp.
Every object physically grounded and logically placed.
```

### QA Checklist

- [ ] 3/4 depth: two walls plus depth visible
- [ ] The gag reads in one frame: unmistakably modern desk + office chair inside an unmistakably Roman room — if the desk drifts Roman or the room drifts modern → reject
- [ ] Exactly the three modern objects (desk, chair, lamp); models may add monitors, papers, phones → reject any extras
- [ ] Banner hangs flat and attached; weapon rack supported; spears actually resting in it
- [ ] Desk and chair grounded on the marble floor, lamp standing on the desk (cordless is fine — it's the future-past, but no cord to nowhere)
- [ ] Grey-blue neutral light consistent with the high windows
- [ ] Zero people
- [ ] Full physics audit — floating object → discard batch

---

## 3. Herod's Palace — Paul's Quarters + Garden Terrace — Priority 1

*Used in Scenes 4, 6 (split)*

### Description

One plate, two playable areas. Interior: a luxurious Roman lounge — marble floor, a plush kline lounge couch with silk cushions on the left, a low marble table beside it, flowing silk drapes and marble columns on the right. Far side: wide arched openings leading out to a sunlit garden terrace with a manicured green lawn, trimmed hedges, and a small stone fountain — the golf stage. Golden afternoon light streams in through the arches. Period Roman luxury only — the opulence reads "5-star resort" without a single modern object.

**Per-shot props (not in the plate):** golf club + ball, food tray, goblet, Paul's loose chains.

### Image-Generation Prompt

```
Luxurious Roman palace guest quarters opening onto a sunlit garden terrace, empty of
people, camera at a three-quarter angle into the room showing the interior and the depth
toward the terrace, eye-level, photorealistic.
Layout: polished marble floor; on the left, a plush Roman kline lounge couch with silk
cushions and a low round marble side table beside it; on the right wall, marble columns
with flowing cream silk drapes between them; in the far wall, three wide open archways
leading out to a garden terrace with a manicured flat green lawn, low trimmed hedges,
and a small stone fountain visible in the middle distance.
Golden late-afternoon sunlight streaming in through the archways, warm and peaceful,
soft long shadows across the marble. First-century Roman luxury — marble, silk, brass,
polished stone — opulent and immaculate, no modern objects.
Every object physically grounded and logically placed.
```

### QA Checklist

- [ ] 3/4 depth AND the two-stage layout: interior lounge in foreground, lawn clearly visible and reachable through the arches — if the terrace is missing or reads as a painting/window → reject
- [ ] Lawn is flat and open enough to stage a golf swing
- [ ] Drapes hang from actual attachment points between columns; couch and tables grounded
- [ ] Fountain in the garden is grounded and plausibly plumbed (stone base, not floating)
- [ ] Golden light direction consistent: sun comes from the terrace side, shadows fall into the room
- [ ] Luxury reads instantly (the "prison = palace" joke) but zero modern objects
- [ ] Zero people
- [ ] Full physics audit — floating object → discard batch

---

## 4. Night Road out of Jerusalem — The Great Escort — Priority 2

*Used in Scene 5 (1:12–1:22)*

### Description

Night exterior. A massive arched stone city gate set into Jerusalem's high ancient walls stands in the background right, its doors open, torches burning in iron brackets on either side of the arch. From the gate, a wide packed-earth road runs diagonally across the frame toward the left foreground and continues past the camera — this is the escort column's marching path. On the near side of the road, left foreground, a flat rocky roadside verge with low scrub and a couple of boulders: the Time Travelers' spectator spot. Beyond the road, rolling dark Judean hills with scattered olive trees. Full moon, clear starry sky. Two light temperatures: cool blue moonlight over the whole landscape, warm orange torchlight pooling at the gate.

**Per-shot elements (not in the plate):** the entire escort column (soldiers, horsemen, carried torches), Paul on horseback, juice pipe, chips bag.

### Image-Generation Prompt

```
Night exterior road leading out of an ancient walled city, empty of people, camera at a
three-quarter angle to the road showing both the city gate and the road's path into the
foreground, eye-level, photorealistic.
Layout: in the background on the right, a massive arched stone city gate set into high
ancient stone walls, its heavy wooden doors standing open, one burning torch in an iron
bracket on each side of the arch; a wide packed-earth road running from the gate
diagonally across the frame toward the left foreground and continuing past the camera;
on the near side of the road in the left foreground, a flat rocky roadside verge with
low scrub bushes and two large boulders; beyond the road, rolling dark hills with
scattered olive trees fading into the distance.
Full moon in a clear starry sky — cool blue moonlight over the landscape and road,
warm orange torchlight pooling on the stone around the gate, the packed-earth road
catching both tones. First-century Judean architecture and landscape, aged stone,
packed earth, no modern objects.
Every object physically grounded and logically placed.
```

### QA Checklist

- [ ] Road path reads clearly: from the gate, diagonally across frame, past the camera — if the road dead-ends, forks confusingly, or exits frame early, the column has nowhere to march → reject
- [ ] Foreground verge is flat and roomy enough for two standing characters with the road visible behind them (Scene 5 blocking depends on it)
- [ ] Gate is structurally sound: arch supported, doors attached to hinges, torches sitting in brackets attached to the wall
- [ ] Two light temperatures both present and sourced: cool blue from the moon (shadows agree with its position), warm orange only pooling near the torches at the gate
- [ ] Scale reads: the gate is massive relative to the road — a column of hundreds must plausibly fit through it
- [ ] Sky is night — moon and stars visible, no dusk/day drift
- [ ] Zero people, zero modern objects (no paving, no signage, no lamp posts)
- [ ] Full physics audit corner to corner — floating object → discard batch

---

## Generation & Handoff Workflow

1. **Generate** 2–4 candidates per plate; audit like a physics inspector, corner to corner. One levitating object = the whole batch was sloppy — discard and regenerate rather than fixing.
2. **Register** accepted plates as named elements. Suggested tags: `conspiracy_chamber`, `commander_office`, `palace_suite`, `jerusalem_night_road`.
3. **Asset pipeline status after this pass:** characters ✅ (7 sheets) · props ✅ (5 sheets) · locations ✅ (4 plates) → **16 total assets to generate**, then registration, then video prompt writing per scene.

---

_Supersedes the location table in the production plan: Sanhedrin Court cut (no scene uses it); Conspiracy Chamber sized as medium vaulted cellar; Commander's Office locked as corporate-desk-island; Herod's Palace locked as lounge + garden terrace in period Roman luxury; Night Road out of Jerusalem added for the final script's Scene 5 escort punchline. Scene numbers throughout refer to the final dialogue script (v2)._
