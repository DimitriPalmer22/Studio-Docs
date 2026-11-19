# FB - Journal

In general, the conveyance of the game's story and the player's progress within it is still *very lacking*.

## Standardize Journal Progress Representation

### The End Room Seal

The end room's seal is currently a 3-layer radial design. Within each layer, there are spaces for each rune (from the journal entries) to be filled in. 

The seal should be used as a representation of the player's progress within the game. The runes only appear after the player has completed the corresponding journal entry. 

Whenever the player returns to the end seal room, the seal should be displayed with the runes that have been collected. This will give the player a visual representation of their progress within the game.

### A UI Representation that Matches the Seal

Currently, completing a journal entry is *VERY* uneventful. There is no visual representation of the player's progress within the game. We can fix this by creating a UI representation that matches the seal in the end room that appears when the player completes a journal entry.

## When to Notify of Current Progress

There should be points in which the player is informed of their progress within the game:

### Collecting a Journal Entry

Collecting a [Journal Entry](../../Avernoth/Mechanics/Journal%20System.md#Journal%20Entry) (after reaching the first end room) should notify the player of their current progress within the game.

### Completing a Journal Quest

### "Depositing" Journal Entries

### Whenever the User Wants

## Tarun's Journal UI

Within the game's world, [Tarun](../../Avernoth/Narrative/Characters/Tarun.md) takes note of the Journal Entries the [Allister](../../Avernoth/Narrative/Characters/Allister.md) encounters. So, the player should be able to view Tarun's Journal at any time.

Currently, the image Alex made for the Journal is not *ideal* for the following reasons:
- Does not fit will onto the screen
- Does not work well for placing the text on (the lines are not straight)
- Not enough space for other elements to be placed on the screen (buttons, tabs, etc.)
- It is difficult to see the text when the **rune** (that appears when the objective is complete) appears.

# Game Plan

## Tarun's Journal UI:
- Completely scrap the UI we have in-place
- Create a new one with:
	- Tabs for each **Chapter** of the game
	- Buttons for going to next / previous entry
	- Better representation for complete entries