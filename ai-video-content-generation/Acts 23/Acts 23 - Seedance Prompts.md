# Acts 23 — Seedance 2.0 Prompts (per clip)

**Source script:** Acts 23 - Dialogue Script (Final, 90 Seconds).md
**Asset registry:** assets/MANIFEST.md
**Clip plan:** 10 generations (Seedance clips max ~15 s). Scene 2 splits in two, Scene 3 in three (around the Commander cutaway), Scene 6 is two clips composited as a split screen in the edit.

## Generation Settings & Credit Policy

- **Resolution lives in the platform UI, never in the prompt.** All prompts in this doc are deliberately resolution-agnostic (no OUTPUT SETTINGS block, no "4K/8K" wording), so one prompt serves every quality tier unchanged.
- **Test pass: 720p.** Cheap iteration — judge blocking, acting, timing, voice, lighting, and continuity. Reroll and fix prompts at this tier.
- **Final pass: re-render the accepted take's exact prompt at 1080p/4K.** Same prompt, same uploads, same order — only the resolution setting changes.
- **720p QA caveat:** small critical details (the glowing seams on the Travelers' jackets, TT#1's mole, TT#2's beauty mark, banner pictograms) may be soft or invisible at 720p. At the test tier, judge them only as "present/absent," and do the fine-detail check on the high-res final render.
- **Credit-saving order of operations:** lock the cheap clips first; generate the crowd-heavy, most reroll-prone clips (1, 8, 9) only once their prompt pattern is proven on simpler ones.

| Clip | Script beat | Runtime | Status |
|---|---|---|---|
| 1 | Scene 1 — chamber vow + stomach growl | 15 s | ✅ prompt ready |
| 2 | Scene 2a — slurp interrupt + Traveler reveal | 9 s | ✅ prompt ready |
| 3 | Scene 2b — Travelers' replies | 11 s | ✅ prompt ready |
| 4 | Scene 3a — pundit commentary | 10 s | ✅ prompt ready |
| 5 | Scene 3b — Commander sushi cutaway (wordless) | 6 s | ✅ prompt ready |
| 6 | Scene 3c — hungry Pharisees + "where's Paul?" | 9 s | ✅ prompt ready |
| 7 | Scene 4 — palace golf gag | 12 s | pending |
| 8 | Scene 5 — the Great Escort | 10 s | pending |
| 9 | Scene 6 left — Pharisees collapse (split-screen half) | 5 s | pending |
| 10 | Scene 6 right — Paul thriving (split-screen half) | 5 s | pending |

---

## Clip 1 — Scene 1: The Conspiracy Chamber (0:00–0:15)

### UPLOAD ORDER for this prompt

| Slot | File | Becomes |
|---|---|---|
| 1 | assets/location-assets/conspiration_room_lrs.png | @image1 (the chamber) |
| 2 | assets/character-assets/pharisee_leader_crs.png | @image2 (the Leader) |
| 3 | assets/character-assets/pharisee_conspirators_crs.png | @image3 (crowd palette) |

### Prompt

```
SCENE CONTEXT
Night, inside an underground stone conspiracy chamber. More than forty Pharisee men are
packed shoulder to shoulder around a long wooden table in secret council. Their leader
stands at the head of the table and swears a dramatic vow of hunger — and a moment
later his own stomach betrays him with a long loud growl.

ACTIVE REFERENCES
@image1 — the underground vaulted stone chamber: two stone columns, long dark wooden
table with benches, clay oil lamps on iron brackets on the left wall, narrow stone
staircase through an arched doorway in the far wall. 100% matches the reference.
@image2 — the Pharisee Leader: late forties, tall head wrap, grey streak in his chin
beard, dark earth-tone woolen robes with a dark-red trim band along the mantle edges,
corner tassels with a blue thread. Voice: deep, theatrical, over-solemn. 100% matches
the reference.
@image3 — crowd palette of four distinct Pharisee archetypes: the men filling the room
are variations of these four, same faction dress, different heights, builds and beard
colors. 100% matches the reference.

LOCATION MAP
Foreground: the near end of the long wooden table. Midground: the table ringed by
densely packed Pharisees, the Leader standing at its head, holding a rolled scroll in
his right hand. Background: the far stone wall with the arched doorway and the narrow
staircase. The clay oil lamps on the left wall are the only light source. The camera
works from the right side of the room, on the shadow side.

FIRST FRAME / BLOCKING
Wide frame from the right side of the room, eye-level: the Leader stands at the head of
the table in the midground, scroll in his right hand, chin lifted. Pharisees packed
shoulder to shoulder fill every gap around the table, all leaning slightly inward toward
him, faces lit warm from the left. The room is visibly too small for this many men.

FORMAT MODE
Timed multishot, 15 seconds, three segments. Cuts only at the specified points, the
camera does not cut on its own.

OPTICS
Segment 1: 63° FOV observational wide. Segment 2: 29° FOV portrait compression on the
Leader. Segment 3: 47° FOV medium on the Leader and the two men flanking him. No drift
mid-segment. Natural motion blur.

CAMERA
Handheld at eye level from the right, shadow side of the room, with a constant subtle
1–2 cm tremor. In segment 2 the camera pushes in slowly toward the Leader's face at
1 km/h. In segment 3 the camera holds locked distance and lets the silence sit.

ACTION
0.0s to 4.0s — Wide: the packed crowd murmurs in hushed voices, heads leaning in.
The Leader slowly raises the scroll above shoulder height; the murmur dies to silence,
every face turns to him.
4.0s HARD CUT
4.0s to 10.0s — Close on the Leader: chin high, eyes burning, he declares slowly and
gravely: "We make a vow! We shall neither eat nor drink until we have killed Paul!"
The men around him nod gravely, fists pressed to their chests.
10.0s HARD CUT
10.0s to 15.0s — Medium on the Leader and the men flanking him: a long, loud stomach
growl rolls out from the Leader's belly. Every man freezes mid-nod. Eyes dart sideways
toward him while heads stay still. Two full beats of silence. The Leader swallows once,
clears his throat, and stares straight ahead with forced dignity.

PERFORMANCE
The Leader plays the vow as high theater — slow cadence, jaw set, nostrils flaring on
the key words. On the growl he freezes completely, blinks once, jaw tightens, then
rebuilds his rigid posture muscle by muscle. The crowd's comedy is restraint: frozen
bodies, only the eyes moving. Pore-level skin realism, living eyes with warm lamp
catch-lights, visible individual beard hairs.

PHYSICS
Heavy wool robes hang and sway with real mass. The scroll flexes slightly in his grip.
Oil-lamp flames flicker and make the shadows breathe on the stone walls. Packed
shoulders actually touch and compress fabric. Contact shadows ground every man on the
stone floor.

LIGHTING
The clay oil lamps on the left wall are the only light source — warm 2800K flame light,
gently flickering, lighting faces from the left of the camera. Deep shadows fill the
corners and the right side of the room. Secretive, close, conspiratorial exposure with
detail preserved in the shadows.

AUDIO
Hushed overlapping murmurs in segment 1. The Leader's vow in a deep, theatrical,
over-solemn voice that fills the stone room with slight reverb. Low gravelly murmurs of
agreement. At 10.0s one long comically loud stomach growl, about 2 seconds, clearly
coming from the Leader — then total silence, then one dry throat-clear.

STYLE
Photorealistic live-action, cinematic realism, natural fine film grain, real-time speed
throughout.

POSITIVE LOCKS
The same Leader in all three segments: tall head wrap, grey chin streak, dark-red trim
band, scroll in his right hand. The chamber, lamp light and crowd stay identical across
cuts. Every man wears first-century Judean robes; every object in frame is first-century
Judean. The room stays packed with more than forty men in every segment. The oil lamps
remain the only light source. The growl belongs to the Leader and the crowd's freeze
holds until his throat-clear.
```

### Post note

Clip 1 covers 0:00–0:15 of the master edit. The music bed (dark tense strings) is added
in the edit, not generated.

---

## Clip 2 — Scene 2a: The Time Travelers Arrive (0:15–0:24)

### UPLOAD ORDER for this prompt

| Slot | File | Becomes |
|---|---|---|
| 1 | assets/location-assets/conspiration_room_lrs.png | @image1 (the chamber) |
| 2 | assets/character-assets/pharisee_leader_crs.png | @image2 (the Leader) |
| 3 | assets/character-assets/pharisee_conspirators_crs.png | @image3 (crowd palette) |
| 4 | assets/character-assets/tt1_male_crs.png | @image4 (Time Traveler #1) |
| 5 | assets/character-assets/tt2_female_crs.png | @image5 (Time Traveler #2) |
| 6 | assets/prop-assets/tumbler_prs.png | @image6 (juice tumbler) |
| 7 | assets/prop-assets/snack_bag_prs.png | @image7 (chips bag) |

### Prompt

```
SCENE CONTEXT
Night, inside an underground stone conspiracy chamber. More than forty Pharisee men
stand packed around a long wooden table, holding a solemn silence after their vow —
when an absurdly loud slurp and crunch from the back of the room makes every head whip
around. Two strangers in subtly futuristic clothes are leaning against the far wall,
snacking, completely relaxed.

ACTIVE REFERENCES
@image1 — the underground vaulted stone chamber: two stone columns, long dark wooden
table with benches, clay oil lamps on iron brackets on the left wall, narrow stone
staircase through an arched doorway in the far wall. 100% matches the reference.
@image2 — the Pharisee Leader: late forties, tall head wrap, grey streak in his chin
beard, dark-red trim band along the mantle edges, rolled scroll in his right hand.
Voice: deep, theatrical, over-solemn, now cracking with indignation. 100% matches the
reference.
@image3 — crowd palette of four distinct Pharisee archetypes: the men filling the room
are variations of these four, same faction dress, different heights, builds and beard
colors. 100% matches the reference.
@image4 — Time Traveler #1: mid-twenties African man, tall and lean, fitted navy sport
jacket with one thin glowing blue seam along the collar edge, white t-shirt, black
jeans, white sneakers. 100% matches the reference.
@image5 — Time Traveler #2: mid-twenties African woman, half a head shorter than the
man, fitted deep burgundy blazer with one thin glowing blue seam along the lapel edge,
black tank top, black jeans. 100% matches the reference.
@image6 — the futuristic juice tumbler with a spiral straw and a soft blue internal
glow, held by Time Traveler #1. 100% matches the reference.
@image7 — the futuristic chips bag with an abstract holographic surface, held by Time
Traveler #2. 100% matches the reference.

LOCATION MAP
Foreground: the near end of the long wooden table. Midground: the packed council of
Pharisees around the table, the Leader at its head. Background: the far stone wall
with the arched doorway and staircase — the two Time Travelers lean against this wall,
just right of the doorway. Oil lamps on the left wall are the primary light; the
tumbler and the glowing jacket seams add a small cool blue pool of light around the
Travelers. The camera works from the right side of the room, on the shadow side.

FIRST FRAME / BLOCKING
Medium-wide from the right side of the room, eye-level: the council stands in stiff
solemn stillness around the table, the Leader stone-faced at its head with the scroll
in his right hand. Every face is turned inward. The far wall sits in the background of
the frame, its doorway in shadow.

FORMAT MODE
Timed multishot, 9 seconds, three segments. Cuts only at the specified points, the
camera does not cut on its own.

OPTICS
Segment 1: 47° FOV medium-wide on the council. Segment 2: 47° FOV standing two-shot of
the Time Travelers against the far wall. Segment 3: 29° FOV portrait compression on
the Leader. No drift mid-segment. Natural motion blur.

CAMERA
Handheld at eye level from the right, shadow side of the room, constant subtle 1–2 cm
tremor. Segment 2 holds a steady standing two-shot. Segment 3 sits close on the
Leader's face and holds.

ACTION
0.0s to 3.0s — Medium-wide: solemn stillness around the table. An absurdly loud SLURP
tears through the silence, followed by a sharp CRUNCH, both coming from the back of
the room. Every head whips around toward the far wall in one motion, robes swirling.
3.0s HARD CUT
3.0s to 6.0s — Two-shot at the far wall: the two Time Travelers lean side by side
against the stone beside the arched doorway, lit half by warm lamplight, half by the
cool blue glow of the tumbler. The man takes another long unhurried pull on the spiral
straw, eyebrows raised at the crowd. The woman digs into the holographic chips bag,
puts one chip in her mouth and crunches loudly, holding eye contact with the room.
6.0s HARD CUT
6.0s to 9.0s — Close on the Leader: eyes wide with disbelief, then narrowing. He jabs
the scroll toward the strangers and demands, voice cracking with indignation:
"Who are you? You're disrupting our sacred vow!"

PERFORMANCE
The whip-around is a single synchronized crowd move — forty heads turning as one, then
total stillness. The Travelers are the exact opposite: loose shoulders, slow blinks,
utterly at home, snacking with deliberate unbothered rhythm. The Leader's indignation
builds through the face first — eyes widen, nostrils flare, brow knots — before the
line explodes out. Pore-level skin realism, living eyes with lamp catch-lights.

PHYSICS
Robes swirl and settle with real cloth weight on the whip-around. The chips bag
crinkles and flexes in the woman's grip. Liquid moves faintly in the glowing tumbler
as the man drinks. Contact shadows ground both Travelers against the wall and floor.

LIGHTING
Clay oil lamps on the left wall remain the primary source — warm 2800K flickering flame
light. Around the two Travelers at the far wall, the tumbler and the thin glowing
jacket seams add a soft cool blue accent glow on their faces and the stone behind them
— the one cold note in a warm room. Deep shadows elsewhere.

AUDIO
One absurdly loud wet SLURP (about 1.5 seconds), then a sharp CRUNCH. The rustle of
forty robes turning at once. In segment 2, the quiet fizz of the tumbler and another
slow crunch. In segment 3 the Leader's line, deep and theatrical, cracking upward with
indignation: "Who are you? You're disrupting our sacred vow!"

STYLE
Photorealistic live-action, cinematic realism, natural fine film grain, real-time speed
throughout.

POSITIVE LOCKS
The chamber, the Leader and the crowd stay identical to their references across all
cuts — head wrap, grey chin streak, dark-red trim band, scroll in the right hand. The
Time Travelers appear only in segment 2, leaning at the far wall beside the doorway,
and stay exactly there. The man holds the glowing tumbler in his right hand; the woman
holds the holographic chips bag with both hands. The blue seam glow on both jackets
stays lit in every frame they appear in. The oil lamps plus the blue tumbler glow are
the only light sources. Every Pharisee wears first-century Judean robes; the Travelers
are the only anachronism in the room.
```

### Post note

Clip 2 covers 0:15–0:24 of the master edit. It cuts directly after Clip 1's throat-clear
— the first frame deliberately matches Clip 1's end state (stiff council, stone-faced
Leader). The Travelers' reveal is a hard cut, not a camera find, so the edit controls
the comedy beat.

---

## Clip 3 — Scene 2b: The Travelers' Replies (0:24–0:35)

### UPLOAD ORDER for this prompt

Identical files and order as Clip 2 — same seven slots:

| Slot | File | Becomes |
|---|---|---|
| 1 | assets/location-assets/conspiration_room_lrs.png | @image1 (the chamber) |
| 2 | assets/character-assets/pharisee_leader_crs.png | @image2 (the Leader) |
| 3 | assets/character-assets/pharisee_conspirators_crs.png | @image3 (crowd palette) |
| 4 | assets/character-assets/tt1_male_crs.png | @image4 (Time Traveler #1) |
| 5 | assets/character-assets/tt2_female_crs.png | @image5 (Time Traveler #2) |
| 6 | assets/prop-assets/tumbler_prs.png | @image6 (juice tumbler) |
| 7 | assets/prop-assets/snack_bag_prs.png | @image7 (chips bag) |

### Prompt

```
SCENE CONTEXT
Night, inside an underground stone conspiracy chamber. More than forty Pharisee men
stand turned toward the far wall, where two strangers in subtly futuristic clothes
lean beside the arched doorway. Challenged to explain themselves, the two answer with
total nonchalance — and the whole council is left exchanging baffled looks.

ACTIVE REFERENCES
@image1 — the underground vaulted stone chamber: two stone columns, long dark wooden
table with benches, clay oil lamps on iron brackets on the left wall, narrow stone
staircase through an arched doorway in the far wall. 100% matches the reference.
@image2 — the Pharisee Leader: late forties, tall head wrap, grey streak in his chin
beard, dark-red trim band along the mantle edges, rolled scroll in his right hand.
100% matches the reference.
@image3 — crowd palette of four distinct Pharisee archetypes: the men filling the room
are variations of these four, same faction dress, different heights, builds and beard
colors. 100% matches the reference.
@image4 — Time Traveler #1: mid-twenties African man, tall and lean, fitted navy sport
jacket with one thin glowing blue seam along the collar edge, white t-shirt, black
jeans, white sneakers. Voice: laid-back, dry, modern and casual — the deadpan half of
the duo. 100% matches the reference.
@image5 — Time Traveler #2: mid-twenties African woman, half a head shorter than the
man, fitted deep burgundy blazer with one thin glowing blue seam along the lapel edge,
black tank top, black jeans. Voice: bright, upbeat, energetic, happily talking through
food. 100% matches the reference.
@image6 — the futuristic juice tumbler with a spiral straw and a soft blue internal
glow, held by Time Traveler #1 in his right hand. 100% matches the reference.
@image7 — the futuristic chips bag with an abstract holographic surface, held by Time
Traveler #2. 100% matches the reference.

LOCATION MAP
Foreground and midground: the two Time Travelers leaning side by side against the far
stone wall, just right of the arched doorway. Background: the packed council of
Pharisees turned toward them around the long wooden table, the Leader at its head with
his scroll. Oil lamps on the left wall are the primary light; the tumbler and the
glowing jacket seams keep a cool blue pool of light on the Travelers. The camera works
from the right side of the room, on the shadow side.

FIRST FRAME / BLOCKING
Standing two-shot of the Time Travelers at the far wall, eye-level, matching the
framing of the previous reveal: the man on the left of frame with the glowing tumbler
in his right hand, the woman on the right of frame holding the chips bag with both
hands, both lit half warm lamplight, half cool blue glow. Beyond them, out of focus,
the turned faces of the council.

FORMAT MODE
Timed multishot, 11 seconds, two segments. Cuts only at the specified point, the
camera does not cut on its own.

OPTICS
Segment 1: 47° FOV standing two-shot on the Travelers, backgrounds softly out of
focus. Segment 2: 63° FOV observational wide on the council. No drift mid-segment.
Natural motion blur.

CAMERA
Handheld at eye level from the right, shadow side of the room, constant subtle 1–2 cm
tremor. Segment 1 holds the two-shot steady through both lines. Segment 2 stands off
the council and lets the confusion play.

ACTION
0.0s to 8.0s — Two-shot: the man lowers the tumbler from his lips, gives the room a
small easy grin and says, dry and unhurried: "Relax, guys! We're here to watch the
show." A beat. The woman leans forward, eyes sparkling with delight, and half-sings:
"You'll see..." — then raises a single chip like a toast, pops it in her mouth, and
bites down with one enormous deliberate CRUNCH, grinning while she chews.
8.0s HARD CUT
8.0s to 11.0s — Wide on the council: forty men in three-quarter profile, all still
turned toward the far wall, exchange slow baffled glances with each other. The Leader
looks down at the scroll in his right hand, then back up at the strangers, mouth half
open — the rebuke dies before it forms.

PERFORMANCE
The man's line lands flat and warm, no effort, as if calming a room of toddlers — one
easy palm-out gesture with his free hand. The woman plays her line as pure showmanship:
the chip raised in a tiny toast, the pause before the bite, the satisfied chew. Comedy
through contrast: the Travelers loose and delighted, the council rigid and lost. The
Leader's bafflement is muscular — brow unknots, jaw slackens, shoulders drop half an
inch. Pore-level skin realism, living eyes with lamp catch-lights.

PHYSICS
The chips bag crinkles and flexes as the woman lifts the chip. The chip snaps cleanly
on the bite. Liquid settles in the glowing tumbler as it lowers. Wool robes shift with
real weight as the council members turn to each other. Contact shadows ground everyone.

LIGHTING
Clay oil lamps on the left wall remain the primary source — warm 2800K flickering
flame light. The tumbler and the thin glowing jacket seams keep the soft cool blue
accent glow on the Travelers' faces and the stone behind them. Deep shadows in the
corners.

AUDIO
The man's line in a laid-back, dry, modern casual voice: "Relax, guys! We're here to
watch the show." A short beat of stunned silence. The woman's line bright and playful,
half-sung: "You'll see..." — then one enormous, room-filling CRUNCH, about 1 second,
followed by her contented chewing. In segment 2, low confused murmurs and the rustle
of robes as forty men trade glances.

STYLE
Photorealistic live-action, cinematic realism, natural fine film grain, real-time
speed throughout.

POSITIVE LOCKS
The Travelers hold the exact positions established in the previous shot — leaning at
the far wall beside the doorway, the man frame-left with the tumbler in his right
hand, the woman frame-right with the chips bag. The blue seam glow on both jackets
stays lit in every frame. The chamber, the Leader and the crowd stay identical to
their references across the cut — head wrap, grey chin streak, dark-red trim band,
scroll in the right hand. The oil lamps plus the blue tumbler glow are the only light
sources. Every Pharisee wears first-century Judean robes; the Travelers are the only
anachronism in the room.
```

### Post note

Clip 3 covers 0:24–0:35 of the master edit and completes Scene 2. Both Traveler lines
live in ONE unbroken two-shot segment so the banter rhythm (line — beat — line — crunch)
is performed in a single take; the only cut is to the council's baffled reaction. These
voice performances are the reference for the Travelers' voices in Clips 4, 6 and 8 — if
a voice drifts badly in later clips, trim a clean line from this clip's audio and attach
it as an @audio reference.

---

## Clip 4 — Scene 3a: The Pundit Commentary (0:35–0:45)

### UPLOAD ORDER for this prompt

Identical files and order as Clips 2 and 3 — same seven slots:

| Slot | File | Becomes |
|---|---|---|
| 1 | assets/location-assets/conspiration_room_lrs.png | @image1 (the chamber) |
| 2 | assets/character-assets/pharisee_leader_crs.png | @image2 (the Leader) |
| 3 | assets/character-assets/pharisee_conspirators_crs.png | @image3 (crowd palette) |
| 4 | assets/character-assets/tt1_male_crs.png | @image4 (Time Traveler #1) |
| 5 | assets/character-assets/tt2_female_crs.png | @image5 (Time Traveler #2) |
| 6 | assets/prop-assets/tumbler_prs.png | @image6 (juice tumbler) |
| 7 | assets/prop-assets/snack_bag_prs.png | @image7 (chips bag) |

### Prompt

```
SCENE CONTEXT
Night, inside an underground stone conspiracy chamber. The two Time Travelers now stand
in the foreground facing the camera like pitch-side sports pundits, delivering
commentary — while behind them, oblivious, more than forty Pharisees argue heatedly
over a scroll spread open on the long wooden table.

ACTIVE REFERENCES
@image1 — the underground vaulted stone chamber: two stone columns, long dark wooden
table with benches, clay oil lamps on iron brackets on the left wall, narrow stone
staircase through an arched doorway in the far wall. 100% matches the reference.
@image2 — the Pharisee Leader: late forties, tall head wrap, grey streak in his chin
beard, dark-red trim band along the mantle edges, arguing over the scroll on the table.
100% matches the reference.
@image3 — crowd palette of four distinct Pharisee archetypes: the men around the table
are variations of these four, same faction dress, different heights, builds and beard
colors. 100% matches the reference.
@image4 — Time Traveler #1: mid-twenties African man, tall and lean, fitted navy sport
jacket with one thin glowing blue seam along the collar edge, white t-shirt, black
jeans, white sneakers, glowing juice tumbler in his right hand. Voice: laid-back and
dry, now putting on a mock sports-announcer cadence. 100% matches the reference.
@image5 — Time Traveler #2: mid-twenties African woman, half a head shorter than the
man, fitted deep burgundy blazer with one thin glowing blue seam along the lapel edge,
black tank top, black jeans, holographic chips bag in her hands. 100% matches the
reference.
@image6 — the futuristic juice tumbler with a spiral straw and a soft blue internal
glow. 100% matches the reference.
@image7 — the futuristic chips bag with an abstract holographic surface. 100% matches
the reference.

LOCATION MAP
Foreground: the two Time Travelers standing shoulder to shoulder, facing the camera
directly, framed from the waist up. Midground: the long wooden table where the Leader
jabs his finger at a scroll spread open on the wood, surrounded by densely packed
arguing Pharisees, all softly out of focus. Background: the far stone wall with the
arched doorway. Oil lamps on the left wall are the primary light; the tumbler and the
jacket seams hold a cool blue glow on the two foreground faces.

FIRST FRAME / BLOCKING
Broadcast-style two-shot: the man frame-left, the woman frame-right, both facing the
camera from the waist up like television pundits at a match, the argument raging out
of focus behind them between their shoulders. The man holds the glowing tumbler in his
right hand; the woman cradles the chips bag.

FORMAT MODE
One continuous shot, 10 seconds. The camera does not cut on its own.

OPTICS
47° FOV two-shot, foreground faces sharp, background argument softly out of focus but
readable. No drift. Natural motion blur.

CAMERA
Locked-off tripod frame at chest height, perfectly steady — a television broadcast
frame, deliberately opposite to the handheld chaos behind them. Focus stays on the two
foreground faces for the full shot.

ACTION
0.0s to 10.0s — One take: the man leans half a step toward the camera, raises his free
hand in a broad announcer's sweep toward the argument behind him, and delivers in a
mock sports-commentary cadence: "And here's the play of the day — the plot gets filed
with the one man legally required to protect Paul. Bold strategy!" As he speaks, the
woman nods along sagely, points a single chip toward the table behind them like an
analyst marking a replay, then eats the chip with a crisp crunch. Behind them the
whole time: the Leader jabs at the scroll on the table, men lean in from both sides
gesturing over each other, one throws up his hands — a full silent-movie argument in
soft focus.

PERFORMANCE
The man performs the line with announcer showmanship on a deadpan face — eyebrows
doing the work, voice riding an exaggerated commentary melody. The woman is the color
commentator: sage nods, the chip-point held for a beat like a telestrator pen. Neither
ever looks back at the argument; they know the game by heart. The background argument
is played with full committed energy — jabbing fingers, shaking heads, gripped beards.
Pore-level skin realism, living eyes with warm lamp catch-lights and a cool blue edge.

PHYSICS
The chip snaps cleanly. The tumbler swings slightly with the man's announcer gesture,
liquid shifting inside. Behind them, wool robes swing with the argument's gestures and
the scroll slides slightly on the wood as hands strike the table. Contact shadows
ground everyone.

LIGHTING
Clay oil lamps on the left wall remain the primary source — warm 2800K flickering
flame light modeling the background argument. The tumbler and the thin glowing jacket
seams wash the two foreground faces with a soft cool blue fill — the broadcast-desk
look inside the conspiracy room. Deep shadows in the corners.

AUDIO
The man's line in a mock sports-announcer cadence over his laid-back dry voice: "And
here's the play of the day — the plot gets filed with the one man legally required to
protect Paul. Bold strategy!" Underneath: muffled overlapping arguing in a period
tongue, robes rustling, one palm slapping the table. One crisp chip crunch from the
woman right after the line lands.

STYLE
Photorealistic live-action, cinematic realism, natural fine film grain, real-time
speed throughout.

POSITIVE LOCKS
The two Travelers hold their broadcast positions facing the camera for the entire
shot — the man frame-left with the tumbler in his right hand, the woman frame-right
with the chips bag. The blue seam glow on both jackets stays lit for the full take.
The Leader keeps his tall head wrap, grey chin streak and dark-red trim band; the
argument stays behind the Travelers, between their shoulders, in soft focus for the
entire shot. Every Pharisee wears first-century Judean robes; the Travelers are the
only anachronism in the room. The oil lamps plus the blue glow are the only light
sources.
```

### Post note

Clip 4 covers 0:35–0:45 of the master edit. The style joke is in the camera grammar:
the conspiracy coverage so far is handheld, but the moment the Travelers take over,
the frame goes locked-off and steady like a TV broadcast. The sports-commentary music
is added in the edit.

---

## Clip 5 — Scene 3b: The Commander's Sushi Cutaway (0:45–0:51)

### UPLOAD ORDER for this prompt

| Slot | File | Becomes |
|---|---|---|
| 1 | assets/location-assets/roman_office_lrs.png | @image1 (the office) |
| 2 | assets/character-assets/roman_soldier_crs.png | @image2 (the Commander) |
| 3 | assets/prop-assets/ancient_scroll_digital_tablet_prs.png | @image3 (tablet-scroll) |

### Prompt

```
SCENE CONTEXT
Day, inside a Roman fortress office. The Roman Commander sits alone at a sleek modern
executive desk eating sushi with chopsticks. He picks up a glowing tablet-scroll
report, reads it for a moment with complete disinterest, sets it down, and goes back
to his lunch.

ACTIVE REFERENCES
@image1 — the Roman fortress office: smooth stone walls, two stone columns, a large red
legion banner with a golden eagle on the far wall, a wooden weapon rack with spears and
two shields on the left wall, tall narrow windows high on the far wall, and in the
center a sleek modern executive desk in dark wood and steel with a black leather
ergonomic office chair. 100% matches the reference.
@image2 — the Roman Commander: mid-forties, sturdy build, short greying hair, bare
head, lorica segmentata plate armor worn casually with red tunic sleeves visible,
leather strip skirt, unarmed. Off-duty bureaucrat energy. 100% matches the reference.
@image3 — the tablet-scroll hybrid: two dark polished wooden rollers with brass caps,
and stretched between them a thin flexible pale-blue glowing screen showing faint
glyphs. It lies on the desk as a delivered report. 100% matches the reference.

LOCATION MAP
Foreground: the front edge of the modern executive desk. Midground: the Commander
seated in the black leather office chair behind the desk; on the desktop, a lacquered
black plate of assorted sushi rolls and nigiri with chopsticks, the glowing
tablet-scroll lying beside it, and the small modern desk lamp. Background: the far
stone wall with the red legion banner and the high narrow windows. Flat grey daylight
falls from the high windows.

FIRST FRAME / BLOCKING
Static formal medium shot, straight-on and perfectly centered on the Commander seated
behind his desk, symmetrical like an official portrait: sushi plate to his left on the
desktop, glowing tablet-scroll to his right, desk lamp at the edge of frame. He is
mid-bite, chopsticks raised.

FORMAT MODE
One continuous shot, 6 seconds. The camera does not cut on its own.

OPTICS
47° FOV medium shot at desk height, everything in crisp focus — flat, formal,
bureaucratic framing. No drift. Natural motion blur.

CAMERA
Locked-off tripod, dead still for the full 6 seconds, centered symmetry — the visual
language of official portraiture and dull administration.

ACTION
0.0s to 6.0s — One take: the Commander places a piece of sushi in his mouth with his
chopsticks and chews slowly. His eyes slide sideways to the glowing tablet-scroll on
the desk. Still chewing, he lifts it with one hand, unrolls it a few centimeters, and
reads. His face stays completely flat — one slow blink, one small exhale through the
nose. He rolls the screen back in, lays the tablet-scroll exactly where it was, and
picks up the next piece of sushi. Life goes on.

PERFORMANCE
Total deadpan carried by micro-behavior: the sideways eye-slide before the head ever
moves, the unhurried chewing all the way through the read, the tiny nasal exhale as
the entire verdict on the matter. His posture stays comfortable and slouched half an
inch below military bearing. Pore-level skin realism, living eyes with flat window
catch-lights.

PHYSICS
The chopsticks flex faintly under the grip. The tablet-scroll's flexible screen curls
and uncurls smoothly around its wooden rollers as he opens and closes it, its pale-blue
glow shifting on his fingers. The office chair yields slightly as he leans back.
Contact shadows ground the plate, the tablet-scroll and the lamp on the desktop.

LIGHTING
Flat overcast 5600K daylight from the high narrow windows — even, neutral, grey-blue
and bureaucratic, with soft shadows. The tablet-scroll's pale-blue screen adds a faint
cool glow on his hand while it is open. The mood is a waiting room, not a fortress.

AUDIO
Quiet room tone with distant muffled fortress sounds. The soft clack of chopsticks on
lacquer, unhurried chewing, the faint smooth rustle of the screen unrolling, one small
bored exhale through the nose. He says nothing.

STYLE
Photorealistic live-action, cinematic realism, natural fine film grain, real-time
speed throughout.

POSITIVE LOCKS
The Commander stays seated behind the desk for the whole shot, bare-headed, red tunic
sleeves visible under the armor, unarmed. The desk holds exactly the sushi plate with
chopsticks, the tablet-scroll and the desk lamp. The room stays first-century Roman
except the desk, the office chair and the desk lamp — those three modern objects and
the sushi are the only anachronisms. The tablet-scroll returns to its original spot on
the desk. Flat grey daylight from the high windows remains the only light source.
```

### Post note

Clip 5 covers 0:45–0:51 of the master edit — the wordless boredom IS the joke, so
protect the silence: no music sting on the cut in the edit until the lounge track
fades in underneath. This is also the cheapest clip in the project (one character,
one room, no dialogue) — ideal as the FIRST test generation to validate the prompt
pattern before spending credits on crowd clips.

---

## Clip 6 — Scene 3c: Hungry Pharisees + "Where's Paul?" (0:51–1:00)

### UPLOAD ORDER for this prompt

Identical files and order as Clips 2, 3 and 4 — same seven slots:

| Slot | File | Becomes |
|---|---|---|
| 1 | assets/location-assets/conspiration_room_lrs.png | @image1 (the chamber) |
| 2 | assets/character-assets/pharisee_leader_crs.png | @image2 (the Leader) |
| 3 | assets/character-assets/pharisee_conspirators_crs.png | @image3 (crowd palette) |
| 4 | assets/character-assets/tt1_male_crs.png | @image4 (Time Traveler #1) |
| 5 | assets/character-assets/tt2_female_crs.png | @image5 (Time Traveler #2) |
| 6 | assets/prop-assets/tumbler_prs.png | @image6 (juice tumbler) |
| 7 | assets/prop-assets/snack_bag_prs.png | @image7 (chips bag) |

### Prompt

```
SCENE CONTEXT
Night, inside an underground stone conspiracy chamber. The plotting has decayed: the
Pharisees around the long wooden table are visibly hungry and frustrated, their
argument running out of fuel. In the foreground, the two Time Travelers still face the
camera like sports pundits, and the woman gleefully hands the story off: "Meanwhile...
where's Paul?"

ACTIVE REFERENCES
@image1 — the underground vaulted stone chamber: two stone columns, long dark wooden
table with benches, clay oil lamps on iron brackets on the left wall, narrow stone
staircase through an arched doorway in the far wall. 100% matches the reference.
@image2 — the Pharisee Leader: late forties, tall head wrap, grey streak in his chin
beard, dark-red trim band along the mantle edges. 100% matches the reference.
@image3 — crowd palette of four distinct Pharisee archetypes: the men around the table
are variations of these four, same faction dress, different heights, builds and beard
colors. 100% matches the reference.
@image4 — Time Traveler #1: mid-twenties African man, tall and lean, fitted navy sport
jacket with one thin glowing blue seam along the collar edge, white t-shirt, black
jeans, white sneakers, glowing juice tumbler in his right hand. 100% matches the
reference.
@image5 — Time Traveler #2: mid-twenties African woman, half a head shorter than the
man, fitted deep burgundy blazer with one thin glowing blue seam along the lapel edge,
black tank top, black jeans, holographic chips bag in her hands. Voice: bright, upbeat,
energetic, happily talking through food. 100% matches the reference.
@image6 — the futuristic juice tumbler with a spiral straw and a soft blue internal
glow. 100% matches the reference.
@image7 — the futuristic chips bag with an abstract holographic surface. 100% matches
the reference.

LOCATION MAP
Segment 1 plays inside the crowd at the long wooden table in the midground of the
chamber. Segment 2 returns to the broadcast setup: the two Time Travelers foreground,
facing the camera from the waist up, the weary council out of focus behind them at the
table. Oil lamps on the left wall are the primary light; the tumbler and jacket seams
hold the cool blue glow on the two foreground faces.

FIRST FRAME / BLOCKING
Handheld medium shot inside the crowd at the table: the Leader stands with both palms
flat on the scroll, head bowed, jaw grinding. Around him the argument has gone limp —
men sag on the benches, shoulders down, faces drawn.

FORMAT MODE
Timed multishot, 9 seconds, two segments. Cuts only at the specified point, the camera
does not cut on its own.

OPTICS
Segment 1: 47° FOV handheld medium inside the crowd. Segment 2: 47° FOV locked-off
broadcast two-shot on the Travelers, background softly out of focus. No drift
mid-segment. Natural motion blur.

CAMERA
Segment 1: handheld at eye level among the men, constant subtle 1–2 cm tremor, drifting
2 km/h across the weary faces. Segment 2: locked-off tripod frame at chest height,
perfectly steady — the broadcast frame.

ACTION
0.0s to 4.0s — Inside the crowd: one gaunt Pharisee rubs his stomach in slow circles
through his robes. Another slumps back against a stone column and slides down it a
hand's width. A third stares into the middle distance and swallows hard as a loud
crisp CRUNCH echoes from somewhere off-screen. The Leader grinds his jaw, both palms
flat on the scroll, plotting on an empty tank.
4.0s HARD CUT
4.0s to 9.0s — Broadcast two-shot: the woman pops a chip in her mouth, chews once,
beams at the camera and delivers, bright and delighted: "Oh, this is going to be a
classic! Meanwhile... where's Paul?" On "where's Paul?" she leans slightly into the
lens, eyebrows up, and the man tilts his glowing tumbler toward the camera like a
toast to the audience.

PERFORMANCE
Segment 1 is played dead straight — real hunger, real fatigue: hollow stares, slow
blinks, the stomach rub absent-minded rather than comic; the comedy is the situation,
never mugging. In segment 2 the woman is pure delight, a fan who knows the next play;
her line rides an upward melody and lands the question with relish. The man stays
deadpan, the tumbler-tilt his only editorial. Pore-level skin realism, living eyes
with warm lamp catch-lights and a cool blue edge on the foreground pair.

PHYSICS
Wool robes crease and drag as men sag onto benches and against the column. The scroll
curls up at its edges under the Leader's palms. The chip snaps, the bag crinkles,
liquid rocks gently in the tilted tumbler. Contact shadows ground every figure.

LIGHTING
Clay oil lamps on the left wall remain the primary source — warm 2800K flickering
flame light, deep shadows in the corners. In segment 2 the tumbler and the thin
glowing jacket seams wash the two foreground faces with the soft cool blue
broadcast-desk fill.

AUDIO
Segment 1: low weary murmurs, a long low stomach gurgle from the gaunt man, robes
shifting on stone, and one loud crisp CRUNCH echoing from off-screen. Segment 2: the
woman's line in her bright upbeat voice, half through a chip: "Oh, this is going to be
a classic! Meanwhile... where's Paul?" — then a soft fizz from the tumbler as it tilts.

STYLE
Photorealistic live-action, cinematic realism, natural fine film grain, real-time
speed throughout.

POSITIVE LOCKS
The chamber, the Leader and the crowd stay identical to their references across the
cut — tall head wrap, grey chin streak, dark-red trim band. The Travelers appear only
in segment 2, in their established broadcast positions: the man frame-left with the
tumbler in his right hand, the woman frame-right with the chips bag. The blue seam
glow on both jackets stays lit in every frame they appear in. Every Pharisee wears
first-century Judean robes; the Travelers are the only anachronism in the room. The
oil lamps plus the blue glow are the only light sources.
```

### Post note

Clip 6 covers 0:51–1:00 of the master edit and closes the chamber block (Scenes 1–3).
The off-screen CRUNCH in segment 1 is the Travelers intruding on the Pharisees' world
even when off camera — sync it in the edit so it reads as the same bag. "Meanwhile...
where's Paul?" is the handoff line: the edit cuts straight from her lean-in to the
palace sunshine of Clip 7 for maximum contrast.
