### Meeting Times

| Meeting                                | Possible Times  |
| -------------------------------------- | --------------- |
| Sound Meeting                          | Tuesday @ 11 am |
| Environmental Artist Meeting           | Friday @ 4 pm   |
| Narrative Designer + CD Meeting        | Friday @ 11 am  |
| Character Artist Meeting               | TBA             |
| 2D Artist + Narrative Designer Meeting | TBA             |
| LD Meeting                             | Tuesday @ 8pm   |
| Animation Meeting                      | TBA             |

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

##### Narrative Stuff
- The portraits of the enemies have been updated in-engine with more updated versions
- *SHOW THE PORTRAITS SO FAR*
- no more android guy :(
- A couple more dialogue interactions have been added, so you'll see those pop up from time to time.
- Dialogue portal transition screen
	- This is VERY placeholder for right now, and I highkey need someone to go in and make this look better
	- As of right now, its a simple level with a camera in it, so it can be easily modified later.

##### UI Updated
- The placeholder UI we had before has been updated a little bit with Alexis's old UI concepts from WAYYY long ago.

#### Feedback from the Team

- FOV change while dodging is a little too harsh right now
- Allister Model Stuff
	- With the art style, the texturing was supposed to do a lot of the heavy lifting, but it's kinda hard to read the detail on Allister right now
	- For characters that are farther away from the player, you should artificially increase the contrast on some things to make details easier to read.
- Change the positions of the sockets where the fire spells spawn. They are a little too far from Allister
- Show some rune effects or something whenever the player is casting a spell
- Death lol

### Out-of-engine Updates

#### Minotaur Model (IN-PROGRESS)

- *SHOW THE MODEL?*
- I just realized that I forgot to ask Mia to send pictures in the Discord, so you guys will just have to believe me when I say the model is getting close to completion.

#### Wraith Model Proxy (IN-PROGRESS)

- *SHOW THE MODEL*

### Goals & Tasks

Just to reiterate, we are working towards a "vertical slice" type of deal, where we show off a portion of the game that is largely representative of how we want the final product to look and feel.

We're definitely getting there, but there is still a lot of work to do.

#### Programmer
- The shop system
- Enemy AI revision
- Journal things

#### VFX
- The rest of the trails (I know some have been worked on, but I haven't seen them yet)
- Impact VFX
- Some other "juicy" stuff I have to talk to Mikel about for conveying information to the player

#### Audio & Audio Implementation
- Right now, the game is still pretty silent
- I know some sounds have been worked on and created, but now we've gotta start actually putting them in the game
- Same with the music

#### Prop Art
- I was looking through the prop list and realized most of the props that need to be textured are wood-based, but we don't have a wood texture yet. It would probably be a bad idea to start on those without establishing a look for the wood first.
	- 
