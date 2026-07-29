# Asset Manifest — Acts 23 Humorous Video Clip (90 Seconds)

Registry of all finalized elements. Video prompts reference elements by **Tag** and must restate the **Critical details** in words — reference images drop small details.

## How referencing works (upload protocol)

Seedance never reads filenames — an `@tag` in a prompt binds to an **uploaded reference**, not to a file on disk:

- **Load-order binding (default):** uploads are ordered slots — first image = `@image1`, second = `@image2`, etc. The prompt's ACTIVE REFERENCES block defines what each slot is.
- **Named binding:** if the interface lets you name uploads, name them with the manifest tag (e.g. `@paul`) and use that tag in the prompt.

Therefore every scene prompt in this project ships with an **UPLOAD ORDER** list, e.g.:

```
UPLOAD ORDER for this prompt:
1. assets/character-assets/paul_crs_3.png        → @image1 (Paul)
2. assets/location-assets/herods_palace_lrs.png  → @image2 (palace)
```

Upload exactly those files in exactly that order, and the prompt text stays consistent regardless of what the files are called. The tags in this manifest are project-side bookkeeping: they identify which file to upload and which critical details to restate in the prompt text.

## Characters

| Element | Tag | File | Critical details | Status |
|---------|-----|------|------------------|--------|
| Time Traveler #1 (male, "The Observer") | @tt1_male | assets/character-assets/tt1_male_crs.png | razor hair part on LEFT temple, mole on left cheekbone, fitted navy sport jacket with one thin glowing blue seam along the collar edge, white crew-neck tee, slim black jeans, white leather sneakers, slim black smartwatch with blue accent on left wrist | final |
| Time Traveler #2 (female, "The Snack Enthusiast") | @tt2_female | assets/character-assets/tt2_female_crs.png | beauty mark under RIGHT eye, fitted deep burgundy blazer with one thin glowing blue seam along the lapel edge, black tank top, slim black jeans, black leather sneakers, small silver earpiece in right ear, half a head shorter than @tt1_male | final |
| Paul ("The Confident Prisoner") | @paul | assets/character-assets/paul_crs_3.png | CLEAN well-kept cream/off-white linen robes (the cleanliness is the joke — never ragged), simple leather sandals, early fifties, dignified bearing | final |
| Pharisee Leader ("The Intense Conspirator") | @pharisee_leader | assets/character-assets/pharisee_leader_crs.png | tall head wrap, grey streak in chin beard, dark-red trim band along the mantle edges, corner tassels (tzitzit) with a blue thread, dark earth-tone woolen robes | final |
| Roman Commander (Claudius Lysias, "The Disinterested Bureaucrat") | @roman_soldier | assets/character-assets/roman_soldier_crs.png | NO helmet, red tunic sleeves visible under lorica segmentata plate armor, leather pteruges skirt, unarmed (no sword/spear/shield), off-duty relaxed stance, mid-forties, short greying hair | final |
| Angel ("The Heavenly Caddy") | @angel | assets/character-assets/angel_crs.png | folded wings reaching mid-calf, clean flowing white robes in a simple modern cut, cream sash, simple sandals, NO halo, NO baked-in glow (radiance comes from scene lighting) | final |
| The 40+ Pharisees crowd ("The Hungry Mob") | @pharisee_conspirators | assets/character-assets/pharisee_conspirators_crs.png | group sheet of 4 distinct archetypes (different heights, builds, beard colors) used as a crowd palette; consistent faction dress — same robe style, head wraps, tassels | final |

## Locations

| Element | Tag | File | Critical details | Status |
|---------|-----|------|------------------|--------|
| Conspiracy Chamber | @conspiration_room | assets/location-assets/conspiration_room_lrs.png | narrow stone staircase through arched doorway in the far wall (Scene 2 time-traveler reveal stages near it), two stone columns, long central wooden table with benches, clay oil lamps on iron brackets as the ONLY light — warm orange/brown, room small enough that 40 men overfill it | final |
| Roman Commander's Office | @roman_office | assets/location-assets/roman_office_lrs.png | exactly three modern objects — executive desk, black ergonomic office chair, metal desk lamp — everything else period Roman: red legion banner with golden eagle on far wall, weapon rack with spears/shields on left wall, high narrow windows, grey-blue neutral daylight, marble floor | final |
| Herod's Palace — Paul's quarters + garden terrace | @herods_palace | assets/location-assets/herods_palace_lrs.png | kline lounge couch with silk cushions on the left, marble columns with cream silk drapes on the right, three wide archways in far wall opening onto flat lawn with trimmed hedges and stone fountain (the golf stage), golden late-afternoon light from the terrace side, zero modern objects | final |
| Night Road out of Jerusalem (Great Escort) | @night_road_jerusalem_out | assets/location-assets/night_road_jerusalem_out_lrs.png | massive arched stone gate background right with open wooden doors and one torch bracket each side, packed-earth road running diagonally from gate past camera (the column's marching path), flat rocky verge with two boulders in left foreground (time travelers' spectator spot), cool blue moonlight + warm torch pools at the gate | final |

## Props

| Element | Tag | File | Critical details | Status |
|---------|-----|------|------------------|--------|
| Futuristic Juice Tumbler | @tumbler | assets/prop-assets/tumbler_prs.png | spiral straw, blue internal glow | final |
| Futuristic Chips Bag | @snack_bag | assets/prop-assets/snack_bag_prs.png | abstract holographic packaging, NO readable text | final |
| Hunger-Strike Pictogram Banner | @hunger_protest_banner | assets/prop-assets/hunger_protest_banner_prs.png | pictogram design only, NO text anywhere on the banner | final |
| Tablet-Scroll Hybrid | @ancient_scroll_digital_tablet | assets/prop-assets/ancient_scroll_digital_tablet_prs.png | two dark polished wooden rollers with brass caps top and bottom, thin flexible pale-blue glowing screen with faint unreadable glyphs stretched between them, parchment-like backing on the reverse | final |
| Ancient Golf Club + Ball | @golf_club_and_ball | assets/prop-assets/golf_club_and_ball_prs.png | driver-style silhouette scaled for a standing adult swing (~1.1 m), polished dark wooden shaft with visible grain, hammered bronze club head with hammer-mark texture, leather-wrapped grip with visible stitching, plain white regulation golf ball with dimples | final |

## Inline-only elements (deliberately NOT registered — describe directly in video prompts)

Sushi plate · palace food tray · goblet · Paul's loose/broken chains · escort column soldiers, horses and carried torches (Scene 5) · golf ball flight effects.
