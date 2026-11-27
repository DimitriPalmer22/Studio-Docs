The way the cutscenes are currently implemented definitely *works*, but it isn't the best.

- Generic cutscenes are not very flexible, as they require all implementation to be done in parent actor.
- Cutscene components overcrowd whatever actor they lives on.
- Cutscenes are not very flexible, as they can only do bunches of dialogue, then whatever else.
	- If i wanted to do a line of dialogue, look at something, then walk, then do another line of dialogue, that's at least 3 assets (1 for the cutscene component overall, 1 for the first line, and one for the last line).

# New System

## Representing a Cutscene

Each cutscene is treated as it's own unique asset. This way, we can edit the cutscenes without affecting parent actors.

### A simple object BP class?
- Removes the need for placing the cutscene as a component on a parent actor; only needs a reference to the class.
- Unsure if I can use latent nodes here.
- The lack of a world context makes it unbearably difficult to:
	- Get subsystems
	- Use global macros
	- Use specific functions from libraries

### An actor component
- Keeps world context
- Has easy access to room manager / whatever other actor this needs access to.
- Bloats actor component panel with cutscenes.

## Handling Dialogue

Rather than having data tables for:
- Batches of entire dialogue interactions
- Batches of lines for a singular dialogue interaction

Dialogue data is stored within the cutscene itself.

### Why?
- Having too many assets for dialogue quickly became confusing and bloated the project to no end.
- The separation between the cutscene system and dialogue system allowed for little-to-no flexibility when creating cutscenes.

### New Approach

Latent node approach to using dialogue system:
- The nodes themselves just send line(s) information to the dialogue UI (speaker, text, etc.)
- The UI handles other behaviors (opening anim, change speaker anim, etc.)
- The UI sends an event to the subsystem to finish the latent node when the player exits the line(s) / closes the dialogue screen.

#### Open / Close UI Manually

If we want, we can open / close the dialogue UI manually. 
- This allows us to keep queueing lines of dialogue while doing other actions.
---

# First Journal Appearance Cutscene

- The room manager houses the cutscene for the cinematic and the accompanying dialogue.
- The exit portal has the cutscene for inhibiting the player from leaving the room and the accompanying dialogue.

---

# Convert Journal Dialogue

Each `response` and `completion` dialogue has its own corresponding cutscene asset.
- No longer JUST dialogue. 
- We can have the player do actions, look at things, etc. in between lines of dialogue.

Eacn Journal ENTRY (the entire thing) has its own FOLDER. Inside the folder, there is:
- A cutscene for the `response` dialogue (if it has any)
- A cutscene for the `completion` dialogue (if applicable)
- A data table for entry's dialogue 

---

# Convert Room Manager Dialogue

- [ ] Enable the player end
- [ ] Room clear dialogue cutscene
- [ ] Quest Item Spawned cutscene
