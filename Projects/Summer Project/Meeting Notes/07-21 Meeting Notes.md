# 07-21 Meeting Notes

### Meeting Times

> I am unavailable on Saturday.

| Meeting                                | Possible Times |
| -------------------------------------- | -------------- |
| Narrative Designer + CD Meeting        |                |
| 2D Artist + Narrative Designer Meeting |                |
| Environmental Artist Meeting           |                |
| LD Meeting                             |                |
| Sound Meeting                          |                |
| Character Artist Meeting               |                |
| Animation Meeting                      |                |

### Play the Game in the Meeting

#### Changes Since the Last Meeting

##### Main Menu
- Brian updated the main menu concept to have a book that opens and flips pages
- He also changed the main menu fonts

##### Tome Creation & Tome Upgrades
- After the first dialogue interaction in the starting room, the player is greeted by the tome creation screen
	- The tome creation screen is very ugly right now, but it is mostly functional
	- The tome creation screen was created in accordance with the GDD, so you should be able to read that to clearly understand what is going on.
	- Each question type is functional EXCEPT the passive ability question (since there aren't any in the game yet).
- At some point during their run, the player encounters the upgrade room
	- I threw in the upgrade room Mikel made a couple weeks ago (and redid the lighting real quick)
	- Functionally, the upgrade room should be almost complete.
		- The dialogue interaction works
		- The upgrade screen appears, although two of the four upgrade types on the GDD are not done yet.
	- The upgrade screen is also very ugly right now, but it is functional.

##### Spells
- Spells can now be set to follow specific points (sockets) on the player, rather than just the player mesh.
	- For example, the fireball spell now follows the player's hand.
- For testing out different animation types for the spells, I threw in a "punch" spell using Mixamo animations real quick
	- It's basically the fireball spell, but it shoots out a fireball as the player punches

##### VFX
If you guys have been keeping up with the team-designer channel, you've most likely seen these already.
- The crystals now have an ambient twinkle VFX around them
	- These are the cyan twinkles that appear specifically around the crystals
	- This is placed on the crystal blueprint, so you don't have to manually place the VFX in the level
- The rooms in general also have ambient magical twinkles that fill the environment
	- These are the white twinkles that are scattered around the level
- The fireball & fire trail VFX have been reworked to be more fire-y
- Last week, I had the screen shaking whenever the player dodged. I removed that and transferred the screen shake to whenever the player gets damaged instead.

##### In-Game HUD
- Last week, I also had Brian create a basic blockout for the in-game HUD.
- It has:
	- Health bar (functional)
	- Mana bar (functional)
	- Area for the player's mana essence (functional, but is purely text for right now)
	- Area for counting the number of keys the player has (NOT functional)
	- A section for the player's passive spells (NOT functional)
	- A section for the player's primary and secondary spells (mostly functional)
		- Depending on the spells the player has equipped, these icons change

##### Animation Things
- Andre made it so Allister's cloak has cloth physics
	- The clipping is a known issue, and we're having Azalee go back and increase the number of polygons in the cloak to reduce the clipping issues
	- She'll also increase the polygon count for the scarf as well so that it has cloth physics too

##### Journal
- Made a simple layout for the journal (that will be revised)
	- Check Chelle's thread for the doc about that if you're interested
	- [Here's the link for convinience](<../Narrative/07-17 First Journal Entry Task.md>)

##### Other Small Changes
- Camera fades in an out when going between rooms (during which the player can't move)
- While the player is locked on to an enemy, the reticle in the center of the screen disappears
- The lock-on point for the enemies has been raised to chest height

#### Things for This Week
