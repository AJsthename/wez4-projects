# Pro Tips and Guidelines for AI Video Generation Projects

> **Read this first — these are heuristics, not laws.** Every tip below is context-dependent. Before applying any one of them, check whether it actually fits the task in front of you. A tip written for building a script from scratch (e.g. #1, #22) may add nothing to a project that already has a locked, fully-directed script. Borrow the *elements* that help, skip the rest. The rulebook in [CLAUDE.md](CLAUDE.md) governs how and when these get folded into system prompts, skills, and design assets.

---

### **Prompting Hacks**

1.  **Provide Situational Context and Anatomical Behavior for Emotional Scenes:** Instead of writing a basic prompt, describe the character's exact feelings and physical reactions. Be highly specific about facial anatomy, like "jaw clenching," "eye twitching," or "a tear starts running down," to avoid robotic AI responses and get a much more human reaction.
2.  **Prompt Like a Photographer:** Be highly specific about the camera gear and settings used to capture the image. Include details like the lens, aperture (e.g., "stop down two stops from wide open"), grain, film stock, and bokeh, as well as the specific lighting setup. If you aren't familiar with camera gear, you can ask Claude to analyze a movie frame you like and extract the camera and lens details for your prompt.
3.  **Build a System Prompt for Adherence:** Create a comprehensive set of rules to govern your workflow. This should include screen text rules, prompt clarity guidelines (one main idea, one main action, one main camera strategy per shot), reference discipline, and a frame coordinate system (e.g., telling the AI to place a character at "20% on X-axis and 30% on Y-axis").
4.  **Iterate on Your Prompts:** The first batch of generations almost never works perfectly. If you like the first 5 seconds of a 15-second generation but the rest fails, adjust your prompt to tell the model to only change the last 10 seconds and generate again.
5.  **Define Single Shots Second by Second:** When doing a continuous single shot, give yourself maximum control by defining exactly what should happen at each individual second in the prompt.
6.  **Use Multi-Shot for Action and Dialogue:** One prompt generation can actually hold multiple cuts. This is ideal for action or dialogue scenes where you need the lighting and positioning to remain perfectly consistent across different character reactions, allowing you to generate all the cuts at once and splice out the successful phases.
7.  **Use Phonetic Transcripts for Dialogues:** Instead of typing out complex words or names exactly as they are spelled, spell them out exactly how they *sound* so the AI pronounces them correctly.
8.  **Maximize Detail to Minimize Hallucinations:** Detail exactly when to cut, which angle to use, and who to cut to. The more instructions you give the model, the less room it has to hallucinate incorrect movements.
9.  **Use Good Frames from Bad Videos as References:** If a video generation is mostly trash but has one perfect moment, take a screenshot of that exact moment. Upload that screenshot into Claude and instruct it to use it as a reference for lighting and positioning to keep future generations consistent.
10. **Optimize Shot Lists to Save Tokens:** If you are working with a very long shot list, tell Claude to only update what has changed in the specific prompt you are working on rather than re-rendering the whole shot list. This cuts token usage by 80% and saves tons of time.
11. **Sanitize Overloaded Prompts:** If you keep iterating on the same prompt by adding new edits, it will get too long and create conflicting instructions. Tell Claude to optimize, study the context, and sanitize the prompt by removing what it no longer needs.

### **Pre-Production Hacks**

12. **Follow the 60-30-10 Color Rule and Specify "Practical Light":** To make visuals appealing, balance your colors with 60% as the dominant color, 30% secondary, and 10% as the accent color. To fix artificial, plasticky lighting where characters look out of place, strictly prompt for "practical light only" (like the sun, windows, or lamps). 
13. **Start Dialogues With Establishing Shots:** Always begin dialogue scenes with a wide or medium establishing shot showing all characters and the layout of the room. The AI model will understand this layout and will correctly place everyone looking at each other when you move on to tighter cuts.
14. **Give Every Location an "Anchor":** Give the AI a specific object in the room (like a tree or a stack of books) to use as an anchor. You can then easily position your characters or the camera by prompting their location relative to that specific anchor.
15. **Never Generate Locations From the Front:** AI struggles with depth perception on head-on shots. Always use a 3/4 angle tilt or place the camera in a top corner (like a CCTV camera) to create depth.
16. **Split Locations Into Separate Views:** If the AI keeps confusing the front and back views of a location, generate them as completely separate images. Attach both to your prompt and specifically state which view should be used for which cut.
17. **Draw the Scene Before Prompting It:** Ask Claude to draw a top-down diagram or map of your scene to figure out spatial layouts. You can iterate on this map and then turn it into a prompt prefix to get perfect character positioning.
18. **Script Action Scenes Beat by Beat:** Define the exact choreography for every single cut of an action scene, including who is in it, where they are, and what weapons they have. If you get stuck, have Claude design the choreography for you.
19. **Cut Faces Out of Wide Shots for Character Sheets:** If the face on your character sheet looks too plasticky, physically cut out a better-looking face from a wide-shot generation and paste it into the sheet.
20. **Make Detailed Sheets for Tricky Props:** If the AI consistently misinterprets how an object should be held, generate separate prop sheets showing the object from different functional angles (e.g., what a monster claw looks like from the outside vs. the inside).
21. **Track Character States (Script Supervising):** For longer films, rigorously track every character's state, including injuries, clothing damage, and prop inventory. Lock in these different visual states before generating so any team member can grab the correct, consistent asset.

---

## Cinematography & Direction

*The tips below were previously an unsorted "Other Useful Tips" dump. They are regrouped here by discipline. Numbering continues from the pre-production set.*

### **Story & Script Structure**

22. **Follow a Classic Story Structure:** To make your story work, build your script around the same structure used in legendary movies.
    *   **The Setup:** Introduce the main character.
    *   **The Rising Action:** Reveal the core conflict, backstory, and drop the character into a major problem to hook the audience.
    *   **The Climax:** Present the ultimate challenge or a massive plot twist.
    *   **The Resolution:** Resolve the conflict at the end.

### **Character & Asset Preparation**

23. **Format Character Sheets for Maximum Clarity:** Always start your character creation with a specific format. Keep the character on a **plain gray background** and include three specific angles: a front view, a back view, and a separate close-up headshot. This ensures the AI model understands what your hero looks like from every angle.
24. **Avoid Harsh Lighting on Visual Assets:** When choosing a character sheet, ensure the lighting is soft. You must avoid harsh shadows on the face or glare in the hair, as cinematic AI videos require a clean, high-quality image of the character to function properly.

### **Location & Environment Setup**

25. **Control Mood Through Location Prompts:** You can set the exact tone of your scene directly in the prompt for your location. Specify details like warm or cold lighting, the weather, and the time of day, and the model will handle the rest.
26. **Always Use "3/4 Angle" for Locations:** Whenever you generate a location, explicitly write "3/4 angle" into the prompt. This forces the model to add volume and depth, giving it a much better sense of the distance between objects.

### **Camera, Framing & Movement**

27. **Build Tension with "Dutch Angles" and Framing:** If a scene feels too basic, use dynamic camera work like a **Dutch angle** (a tilted camera shot) to build tension and make the audience uncomfortable. Additionally, leaving almost no space between your character and the edge of the frame makes the hero feel trapped, which is a classic director's move for showing a character losing control.
28. **Simulate Realism with Handheld Camera Moves:** Add "handheld camera movement" to your video prompts. This adds subtle walking and breathing motions, creating the illusion that a real human camera operator is holding the gear.
29. **Lock Character Positioning with Wide Shots:** If you are struggling to get your characters positioned correctly in a room, start your scene with a wide establishing shot. This forces the AI to map out the room and place everyone exactly where they need to be, keeping their positions locked for the rest of the sequence.
30. **Create Drama with Speed Ramps:** To make crucial moments more dramatic (like a football flying toward a goal), instruct the AI to use a **speed ramp**. This dips the footage into slow-motion and snaps it back to full speed, creating a cinematic "frozen in time" effect.

### **Transitions & Editing**

31. **Use Match Cuts for Seamless Scene Transitions:** To make a smooth transition between clips in the same scene, attach the final frame of your previous generation to your next prompt. This allows the AI to kick off the new scene from the exact same physical position.
32. **Master the Whip Pan Transition:** To hold the viewer's attention between scenes, use a **whip pan** (a fast sideways swing of the camera). When prompting for this, give the AI a duration and label your subjects (A, B, C, etc.). Crucially, a whip pan must end on the exact same type of shot that it started on (e.g., if it starts on a medium shot, it cannot end on a close-up).
33. **Add Pauses After Flashbacks:** A crucial directing rule: never jump straight into dialogue immediately following a flashback. Always stitch in a one to two-second pause to allow the character to process the memory before they begin speaking.

### **Model-Specific Behavior (Seedance)**

34. **Lock in Visuals to Lock in Voices:** The Seedance AI automatically generates a unique voice for a character based on their appearance in the character sheet. By consistently referencing the exact same character sheet, you inherently lock in their voice to ensure it stays consistent throughout the film.
35. **Ditch Negative Prompts:** When using Seedance, do not use negative prompts (e.g., telling the AI "he's not crying"). The model does not understand them and will often do the exact opposite. Instead, tell it exactly what you want it to do, such as prompting for "an anxious look".
36. **Generate Clean Plates — Diegetic SFX Only, No Baked-in Music or Text:** Seedance tends to add a musical score on its own even when you never asked for one, and any baked-in music or on-screen text makes the finished clip nearly impossible to edit, re-cut, or re-score. In every *video* prompt, restrict the audio to basic environmental and action sound effects (plus the needed spoken lines) and lock out music, songs, captions, and subtitles — phrase it positively, e.g. "diegetic sound only, no music, no on-screen text." Add the music bed, titles, and subtitles afterward in the edit, where they stay fully controllable and removable. (Applies to **video generation prompts only** — image/asset prompts have no audio and need no captions.)
