# FB - Journal

In general, the conveyance of the game's story and the player's progress within it is still *very lacking*.

## Standardize Journal Progress Representation

### The End Room Seal

The end room's seal is currently a 3-layer radial design. Within each layer, there are spaces for each rune (from the journal entries) to be filled in.

The seal should be used as a representation of the player's progress within the game. The runes only appear after the player has completed the corresponding journal entry.

Whenever the player returns to the end seal room, the seal should be displayed with the runes that have been collected. This will give the player a visual representation of their progress within the game.

> [!NOTE] Early Seal Layers Explanation
> We should establish early on that the game is divided into 3 chapters, with each chapter corresponding to a layer on the seal. This will help the player understand where they are in the game better. We can have one of the characters explain this, seeming as they are ALL magicians.

### A UI Representation that Matches the Seal

Currently, completing a journal entry is *VERY* uneventful. There is no visual representation of the player's progress within the game. We can fix this by creating a UI representation that matches the seal in the end room that appears when the player completes a journal entry.

This UI representation is purely exegetic, meaning the characters in the game do not acknowledge it. It is purely for the player's benefit.
- We can pretend [Tarun](../../Avernoth/Narrative/Characters/Tarun.md) is keeping track of this within his notebook.

## When to Notify of Current Progress

There should be points in which the player is informed of their progress within the game:

### Collecting a Journal Entry

Collecting a [Journal Entry](../../Avernoth/Mechanics/Journal%20System.md#Journal%20Entry) (after reaching the first end room) should notify the player of their current progress within the game.

I don't know if this should make the Seal UI representation appear.

### Completing a Journal Quest

Completing a Journal Entry (collecting a [Standard Journal Entry](../../Avernoth/Mechanics/Journal%20System.md#Standard%20Journal%20Entry) / completing an [Experiment Log](../../Avernoth/Mechanics/Journal%20System.md#Experiment%20Log)'s objective) should notify the player of their current progress within the game.

This should DEFINITELY make the seal UI representation appear.

### "Depositing" Journal Entries

Interacting with the end room's seal sends the player back to the starting area. Maybe include a notification of the player's current progress within the game when they do this.

### Whenever the User Wants

The player should be able to access this UI representation from the journal menu as well.

## Codex UI

Within the game's world, [Tarun](../../Avernoth/Narrative/Characters/Tarun.md) takes note of the Journal Entries the [Allister](../../Avernoth/Narrative/Characters/Allister.md) encounters. So, the player should be able to view Tarun's Journal at any time.

Currently, the image Alex made for the Journal is not *ideal* for the following reasons:
- Does not fit will onto the screen
- Does not work well for placing the text on (the lines are not straight)
- Not enough space for other elements to be placed on the screen (buttons, tabs, etc.)
- It is difficult to see the text when the **rune** (that appears when the objective is complete) appears.

# Game Plan

## End Room Seal Design

- Solidify the design for the end room's seal.
- This is important because other things depend on it.

## UI Representation of the Seal

- Create a UI screen that appears whenever completing a journal entry.
- The design of this should loosely match the end room's seal.

## Tarun's Journal UI

- Completely scrap the UI we have in-place
- Create a new one with:
	- Tabs for each **Chapter** of the game
	- Buttons for going to next / previous entry
	- Better representation for complete entries
	- The completion symbol should be somewhere off to the side, away from text

# Work Notes

## Codex UI

The two-page system we had before wasn't a bad idea:
- The left page is for navigation
- The right page is for the journal's contents.

### The Left Page

The left page acts as a permanent Table of Contents.

However, we often got hit with "Why does the left page never change? If we are turning the page to the next entry, shouldn't the left page change as well?"
- We can really just say it's a magic book
- Tapping on elements on the left page change the right page's contents, making them fade in and out.

### The Right Page

The right page contains the contents of the journal entry. However, maybe we should just **COMPLTELY** copy the journal entry UI and put it here…

#### Varying Page Layouts for Entries

Having each journal entry follow the EXACT same layout is very boring visually. Also, if these are supposed to be notes of some sort, then we can have the pages look different.

For example, some entries can have:
- a diagram
- a table
- a list of items
- various scribbles around the page

We can set up several possible pre-determined layouts for the journal entries. Within the data for the entry itself, we store which layout to use. This way, we can have a variety of layouts for the journal entries, making them more visually interesting.

> [!NOTE] Update the Journal Entry Collect UI as well
> This idea requires the journal entry collect UI to be updated as well to support this functionality. It should literally be the same as the journal entry UI, just without the left page and bigger to fill more space on the screen.
