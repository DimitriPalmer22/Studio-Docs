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

## Why?
Having too many assets for dialogue quickly became confusing and bloated the project to no end.