# Game Structure

## Beginning Room

At the start of each run, the player ***wakes up*** in the same room every time, the "beginning" of [Avernoth](<../Avernoth.md>). This room serves as a consistent place that we, the game developers, can use to:
- Communicate important story beats to the player (through dialogue)
- Start the player's run and get them into the main game loop

### "Waking Up"

Here are the narrative justifications for why we always revert back to the beginning room after each run:
- The very first time [Allister](<../Narrative/Characters/Allister.md>) wakes up in this beginning room, it is immediately after he has been sealed in his [battle with Hidetomo](<../Narrative/Narrative.md#Events Leading Up to the Game>).
- [Magnus](<../Narrative/Characters/Magnus.md>) cast a spell to reset Allister's position to the start of Avernoth whenever he dies, hence the reason why Allister always wakes up in the same room.
- This same spell can also be activated manually, allowing Allister to return to the start of Avernoth whenever he successfully reaches the end of a run.

### [Dialogue](<./Dialogue.md>)

Upon "waking up", Allister's allies communicate with him through a dialogue portal that spawns around his shoulder. We can use this dialogue to process any significant revelations that Allister has acquired throughout his runs, which allows us to move the plot forward and give the player a sense of progression even though they are technically restarting their run every time they die.

### [Tome Altar](<./Tome Altar.md>) (Starting The Run)

At the start of each run, Allister uses must use the Tome Altar (he also can't use the portals within Avernoth without it, which is why they don't appear until he has one). The tome altar grants Allister a [Tome](<../../Mechanics/Tomes.md>), and Allister takes his leave.

## Standard Rooms

### [Combat](<./Combat/Combat.md>)

Each room contains a variety of enemies that are thrown at the player in waves. The player must defeat all the enemies before leaving the room.

### [Journal Entries](<./Journal System.md#>)

Within each standard room is a [Journal Table](<./Journal System.md#Journal Table>). It is the player's main goal to collect these journal entries, as they are the key to escaping [Avernoth](<../Avernoth.md>).
