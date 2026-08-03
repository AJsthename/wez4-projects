# Seedance Prompts Pitfalls Audit

Scope: current written Seedance prompt files only.

- `Acts 23/Acts 23 - Seedance Prompts.md`: Clips 1-6 are written; Clips 7-10 are still pending.
- `the_goliath_complex/Goliath Complex - Seedance Prompts.md`: Clips 1-10 are written; Clips 11-95 are still pending.

## Cross-Project Issues

- **Goliath prompts are marked ready but many references are not locally backed.** The Goliath manifest says most `final` tags exist only in the generation platform and are not filed in the repo. Current prompts depend on tags such as `@valley_elah_3qf`, `@israel_camp_3qf`, `@valley_plain_3qf`, `@shield_bearer`, `@goliath_spear`, `@philistine_army`, `@israelite_army`, `@saul_tent_3qf`, `@saul_council`, `@general`, and the funny soldiers. That makes the clips operationally fragile despite the prompt table saying "ready."

- **Acts 23 prompt bodies do not include the clean-plate lock.** The rulebook and pro tips require video prompts to lock `diegetic sound only, no music, no on-screen text`. The Goliath prompts do this consistently; Acts 23 mostly leaves music/text exclusions to post notes or omits them from the actual prompt blocks. Seedance may add unwanted score, captions, title text, or lower-thirds.

- **Both prompt files use negative-control phrasing heavily.** Phrases such as "camera does not cut on its own," "No drift," "no music," and "no on-screen text" appear often. Some are established local conventions, and the music/text line is intentionally required, but the broader Seedance guidance warns that negative phrasing can invert. Where possible, generation instructions should be phrased as positive locks.

- **Several prompts are multi-shot mini-edits rather than simple clips.** This is sometimes intentional, but it raises failure risk when a single generation includes multiple cuts, multiple locations, or different camera grammars. The highest-risk examples are Goliath Clip 6 and Acts 23 Clips 2-4.

## Acts 23

- **Clips 2, 3, 4, and 6 under-spec manifest-critical Traveler identity marks.** The manifest calls out TT#1's left-temple hair part, mole on left cheekbone, smartwatch, and TT#2's right-eye beauty mark, earpiece, and black leather sneakers. The Seedance prompts mention the jackets, glow seams, shirts, jeans, and broad build/height, but mostly omit those small identity locks. This is especially inconsistent because the file's QA caveat explicitly names the mole and beauty mark.

- **Clips 2, 3, 4, and 6 say the Travelers are the only anachronism, while their props are also anachronistic.** The prompts also include the glowing tumbler and holographic chips bag. The intended meaning is probably "the Traveler package is the only anachronistic presence," but the current wording could cause the model to suppress or period-normalize the snack props.

- **Clip 3 has a spatial map contradiction.** The Travelers are described as leaning against the far wall beside the doorway, but the location map says the Travelers occupy the foreground/midground and the council is in the background. Unless the camera has moved to the far wall looking back into the room, this reverses the room geography established in Clip 2.

- **Clip 4 moves the Travelers into a broadcast foreground without a continuity bridge.** Clip 3 locks them at the far wall; Clip 4 starts with them foreground, waist-up, facing camera like pundits, with the council arguing behind them. This can work as a new staged gag, but the prompt does not clearly say they have repositioned from the wall to the table-side foreground.

- **Clip 1 asks close and medium shots to preserve "more than forty men in every segment."** Segment 2 is a portrait-compression close on the Leader, and Segment 3 is a medium on the Leader plus two flanking men. Locking all forty men into every segment may fight the framing and make the model crowd the closeups unnaturally.

- **Clip 2 is tightly packed for 9 seconds.** It needs solemn stillness, loud slurp, crunch, forty-head whip, Traveler reveal, second slurp/crunch, and the Leader's full rebuke. The individual pieces are clear, but the 3-second final closeup may rush the spoken line.

- **Clip 4 has a high dialogue/action density for 10 seconds.** The man's line is long, he gestures toward the argument, the woman performs a chip-point and crunch, and the background argument must stay readable. The prompt may need rerolls to avoid mumbled speech or background chaos overpowering the foreground.

- **Clip 5 introduces sushi and a desk lamp without uploaded prop references.** The manifest marks sushi as inline-only and the office reference includes the desk lamp, so this is not wrong. It is still a generation risk because the prompt requires clean modern sushi, chopsticks, a modern lamp, and a tablet-scroll all on one desktop while only the tablet-scroll is uploaded as its own prop.

- **Acts 23 status table says 10 generations, but only 6 prompts exist.** This is probably deliberate because Clips 7-10 are pending, but the "credit-saving order" mentions crowd-heavy Clips 8 and 9 even though those prompts are not yet written.

## The Goliath Complex

- **The biggest blocker is asset availability, not prompt wording.** The manifest warns that only four images are filed in-repo: `@david`, `@saul`, `@goliath`, and `@avg_soldier`. Yet the written prompts require many more location, prop, crowd, and cameo tags. If the generation platform session loses those tags, the ready prompts cannot be reproduced from the repo.

- **Clip 3 references `@goliath_shield` even though the manifest says the shield has unresolved size failures and v4 is pending.** The row is marked `final`, but the same row says v1/v3 were too small, v2 was far too large, and the accepted v4 spec still needs regeneration/filing. This is internally inconsistent and could poison the most scale-critical reveal.

- **Clip 4 is a solo Goliath shot with weak scale anchoring.** The scale bible warns that solo Goliath shots need an in-frame yardstick. Clip 4 uses only Goliath and his spear, with no `@cast_scale`, `@shield_bearer`, or nearby soldiers. The spear-head-at-shoulder contact helps, but the model can resize the spear with him, so it is a weaker cap than a human yardstick.

- **Clip 6 may be over-ambitious as one continuous 14-second shot.** It starts on Goliath and the Philistine host, then pans/cranes across the whole valley into tight Israelite fear, while changing from 47 degree wide to 29 degree tight and carrying two crowd identities plus two location references. This may blur geography, mix army costumes, or generate an impossible camera move.

- **Clip 6 scale lock uses "ordinary soldier" before establishing an on-screen yardstick.** The later `@philistine_army` line gives a waist-height yardstick, but the `@goliath` reference first says "ordinary soldier's height/shoulder width." The rulebook prefers anchoring multiples to a named visible figure or group.

- **Clip 8 uses `@general`, but the manifest says the general has an unrecorded scale and needs verification against the sheet.** The prompt marks the asset as 100% matching, while the manifest says its description and scale still need validation.

- **Clip 9 says Saul looks to his "generals" plural, but the upload order supplies only singular `@general` plus the council.** The model may duplicate the general, treat counsellors as generals, or drift the group identity.

- **Clip 9 relies on offscreen Goliath voice without a Goliath reference or audio anchor.** Avoiding a visual `@goliath` reference is sensible because he should stay offscreen, but the voice may drift from Clips 4-6 unless an audio reference is used in generation or fixed in post.

- **Clip 10 uses the group-sheet `@saul_council` for one departing counsellor.** The active reference says "a counsellor walking off," but the tag is a three-person group sheet. This risks rendering all three counsellors leaving, or creating a hybrid face rather than a stable individual.

- **Clip 10 mixes an exterior camp plate with an interior tent reference for a brief insert.** The prompt wants Saul glaring from the command-tent entrance up-slope, but `@saul_tent_3qf` is defined as the command-tent interior. This may cause the insert to become an interior throne/tent shot instead of a clean exterior glare from the entrance.

- **Clips 5, 8, and 10 use sequential cuts without exact timecodes.** This can work, but it gives Seedance less timing control than the Acts timed multishot format. Clip 5 has a long Goliath line split across cuts; Clip 8 has dialogue handoff; Clip 10 has five cuts in 15 seconds.

- **Goliath upload order and active-reference order are not always aligned.** Example: Clip 4 upload order lists `@valley_plain_3qf` first, then `@goliath`, then `@goliath_spear`, while active references start with `@goliath`. This is harmless if named `@tag` binding is truly used, but confusing if an operator treats upload order like the Acts `@image1` slot system.

- **The Goliath prompts depend on platform tags but do not list local file paths.** This matches the file's chosen `@tag` protocol, but it makes the document less self-contained than Acts 23. The manifest's archival gap makes this a practical production issue rather than just formatting preference.

## Lower-Priority Consistency Notes

- **Acts 23 production plan is older than the final dialogue/prompt flow.** It still describes an earlier ordering with the Commander appearing near the start and different commentary beats. The final dialogue script and Seedance prompts appear to supersede it, but anyone using the production plan as source truth could reintroduce outdated beats.

- **Acts 23 Clip 5 says the office has exactly three modern objects, then treats sushi as an anachronism too.** This is probably intended because sushi is inline-only food, but the wording "exactly three modern objects" versus "those three modern objects and the sushi are the only anachronisms" is slightly inconsistent.

- **Goliath Clip 7's breakdown location says Saul's command tent, while the prompt is staged outside at the camp/command tent peak.** The source visual supports the outdoor staging, so the prompt is probably right; the breakdown label is just coarse.

- **Prompt files contain many smart punctuation characters.** That is normal for Markdown, but if prompts are copied into a tool that mangles encoding, quotation marks, dashes, and degree symbols should be checked after paste.

