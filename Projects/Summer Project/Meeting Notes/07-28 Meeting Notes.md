### Meeting Times

| Meeting                                | Possible Times |
| -------------------------------------- | -------------- |
| Sound Meeting                          |                |
| Environmental Artist Meeting           |                |
| Narrative Designer + CD Meeting        |                |
| Character Artist Meeting               |                |
| 2D Artist + Narrative Designer Meeting |                |
| LD Meeting                             |                |
| Animation Meeting                      |                |

### Vertical Slice Deadline Pushed Back a Week

- Last week, I told you guys that the vertical slice deadline was Sunday, August 3rd.
- BUT, a couple things have changed since then, and I have decided that the deadline needs to be pushed back a week. Mainly, I want to give our new team members a chance to get up to speed and contribute to the vertical slice.

### Play The Game in the Meeting

#### Changes from the Last Meeting

###### New Allister Model
- The completed Allister model is now in the game
- Scarf and robe physics are implemented (but are still being worked on)
- The model is fully textured, but the materials used to apply the textures are not final / need to be replaced. Right now, Allister looks a little too shiny

##### Combat Updates
- New spell type: combo spells. 
	- The spell is actually broken up into multiple parts where the player has to keep pressing the spell button to continue the combo. Also, the player slowly moves toward enemies while casting these spells.
	- We were running into an issue where the spells we had before were generally uninteresting to use / were not really that fun to play with. This is for a couple reasons. The main reason why combo spells were added was to make player input much more engaging.
	- A lot of the Primary spells are going to follow this approach, whereas the secondary spells are still going to be the basic single-cast spells we had before.
- There has also been some "juice" added to the game:
	- Camera shake whenever the player gets hit by an enemy attack
	- Hit stop whenever the player hits and enemy or an enemy hits the player
	- Flinch animation whenever the player or enemies are hit by a spell. This animation also interrupts the casting of any spells that are currently being cast.
	- FOV changes slightly while dodging (this may be way too harsh right now)

##### Mana Essence (The currency)
- Before, whenever the player killed an enemy, the money counter would just go up.
- Now, currency is a physical object.
- Whenever the player kills an enemy, they drop mana essence orbs.
- These orbs eventually fly toward the player after spawning
- Also, sometimes when you clear a room, mana essence orbs will spawn in the room and fly toward the player.
- As of right now, the appearance of these orbs is completely placeholder

#### Feedback from the Team

### Out-of-engine Updates

#### Minotaur Model

#### Wraith Model

### 