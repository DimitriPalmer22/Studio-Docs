
## Spells Screen

This is a screen where the player, at any time, can learn more about the current spells they have equipped. Thematically, Allister is opening his tome and reading the contents, so the UI should probably reflect that.

Preferrably, the layout should stay pretty similar to the rough blockout shown below. The panels *can* be moved a little and resized, and the exit button can be moved somewhere else entirely.

!![](<../../../_Meta/Attachments/SpellScreen.png>)

### Features
- In the left panel, we see a list of all the spells currently equipped. Each item is this list is actually a button. Clicking on one of these buttons will update the right panel to show more information about that spell. Each button features, the spell's icon, name, and the type of spell it is (primary, secondary, or passive). The left panel has a scrollbar just in case the player has enough spells that they don't all fit on the screen at once.
- The right panel shows much more detailed information about the currently selected spell. At the top, we see the spell's icon, name, and type again for easy reference. Below that, we have a small, but interesting bit of flavor text to give the game a little more personality. Next, we have an actual description of the spell and it's unique abilities. Each spell has some added effects that are not immediately obvious, so this description is important for players to understand how to best utilize their spells. Finally, at the bottom, we have a section dedicated to the upgrades to the spell that the player has acquired throughout their current run. NOTE: only primary spells can have these types of upgrades. So, this section will only appear if the currently selected spell is a primary spell.
- Last, there is an exit button toward the bottom of the screen that allows the player to close out of this screen and return to the main game.

## Codex / Journal Screen

This is a screen where the player can read through the various journal entries & experiment logs they have unlocked in their time playing the game (not just the ones found in the current run).

Journal entries and experiment logs are KEY to the player's progression, so we need some place to store them for easy access. In order to escape Avernoth, the player must collect all experiment logs + journal entries in the game.

### Theming

Thematically, Allister himself is not able to pick up these notes and take them with him. Remember, every time he dies, he loses everything he acquired during his current run. So, Tarun, Allister's handy apprentice, transcribes these notes into *HIS* notebook. When we open up this menu, we are looking at TARUN's notebook.

### Journal Entries vs. Experiment Logs

Journal entries are just plain notes that the can read.

Experiment logs are also notes. However, they contain some type of *objective* the player must complete in order to fully recreate the experiment listed on it.

### Progression

At the end of the game, there is a door. The door has a magic seal on it. The magic seal has a series of runes around it. Each rune on this seal corresponds to a rune on each journal entry / experiment log.

By default, journal entries will have a rune on the background of the page(?).

On the other hand, incomplete experiment logs will not have their runes visible on the page at first. Once the player completes the associated objective, the rune will appear on the background of the page to visually mark that the objective has been completed.

### Mockup Features
!![](<../../../_Meta/Attachments/CodexTest.png>)

- In the left panel, there are buttons where the player can select which note the want to view.
- For each button:
	- There is the rune associated with the note. For standard journal entries, this is always going to be visible. For experiment logs, this is only visible once the associated objective has been completed. 
	- The title of the note
	- The type of note it is (experiment log vs. journal entry)
- In the right panel is the note itself.
- For each note:
	- there is the text of the note itself
	- the background of the note contains the rune associated with the note. However, we need to find a way to make this as unintrusive as possible. Maybe make it smaller or move it out the way? The readability of the text takes priority.
