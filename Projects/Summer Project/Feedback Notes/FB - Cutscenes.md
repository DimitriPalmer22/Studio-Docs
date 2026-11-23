The way the cutscenes are currently implemented definitely *works*, but it isn't the best.

- Generic cutscenes are not very flexible, as they require all implementation to be done in parent actor.
- Cutscene components overcrowd whatever actor they lives on.
- Cutscenes are not very flexible, as they can only do bunches of dialogue, then whatever else.
	- If i wanted to do a line of dialogue, look at something, then walk, then do another line of dialogue, that's at least 3 assets (1 for the cutscene component overall, 1 for the first line, and one for the last line).

# New System

## Representing a Cutscene

Each cutscene is treated as it's own unique asset. This way, we can edit the cutscenes without 

## Handling dialogue.
