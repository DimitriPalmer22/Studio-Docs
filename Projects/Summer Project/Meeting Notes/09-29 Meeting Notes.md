# Meeting Times

| Meeting                                | Possible Times |
| -------------------------------------- | -------------- |
| LD Meeting                             |                |
| Narrative Designer + CD Meeting        |                |
| Sound Meeting                          |                |
| Environmental Artist Meeting           |                |
| 2D Artist + Narrative Designer Meeting |                |
| Animation Meeting                      |                |
| Character Artist Meeting               |                |

# The Game

## Current State of the Game
Week by week, the game is getting more and more complete. As of right now, a lot of the main components of the game are taking shape, but some things still need to be iterated on.

Right now, you can *sorta* do a full playthrough of the game:
- Start at the beginning area & Choose your spells based on the questions you get
- Go through rooms and fight enemies
- Get upgrades from the upgrade room
- Buy stuff from the shop room
- Eventually reach a "boos room" (that only has 1 enemy in it lol)
- Keep doing that until you reach the "End of the game" room (which is currently just a placeholder room)

The "Skeleton" of the game is taking shape, but we need to flesh it out with meaningful content.

## Goals for v0.5.0:

For v0.5.0, we're focusing on:
- *Presentation & Polish* - Remove a lot of that 'testing' feel from the game
- *Game Essence* - Understand what would make the game fun to play and iterate on that 

### Outside of Combat

#### Beginning Area

##### Iterate again on the design of the beginning area
The beginning area
- is the very first area of the game players see
- is gonna be the area where players see when they restart a run

So, the visual design and functionality of the room is very important and should be refined further. Maybe we could even split it up into multiple rooms?

##### Beginning Questions
When the player starts the game, they get 3 questions:
- One for their primary spell
- One for their secondary spell
- One for 1 or more passive spells

- However, the current questions we have are still placeholder (boring text)
- Chelle made a couple questions a while ago, but they've never been implemented into the game. We should probably do that.
- Outside of that, we should probably make some more questions to add more variety to the game.

- Furthermore, the UI for those beginning questions is still placeholder. We should probably iterate on that.

#### Economy & Currency

- I want the player to be rewarded for playing well (not taking damage / clearing rooms quickly)
- I want the player to also consciously make decisions about how they're spending their money (the shop or the upgrade room)
	- This is another one of those risk / reward things
	- Do they increase their power in the upgrade room or increase their survivability in the shop?
- Right now, the economy is still pretty unbalanced.

- [ ] Determine how much money you get for clearing a room (based on performance)
- [ ] Determine how much money you get for killing enemies
- [ ] Adjust the prices in the shop
- [ ] Adjust the prices in the upgrade room

#### Upgrade Room

##### Visual Design of the Upgrade Room Needs Iteration
- Right now, the upgrade room is *very* similar functionally to a standard shop in a video game: go in -> spend money -> come out.
- We at the very least need to *distinguish it visually from the shop room* so that players don't get confused
- There isn't much in the room that thematically tells the player "hey, this is the upgrade room where we **improve your tome**"

- Also do the same lighting adjustments that are present in other levels

##### Reward the Player for Playing Well + Risk/Reward
The shop has 3 tiers of upgrades, each with different prices. Here's the though process behind that decision:

- I want the player to be guaranteed an upgrade every time they enter the upgrade room
- The better you play, the more money you make.

##### Upgrades Need to be More Interesting

#### Shop

##### We Need Better Shop Items

#### Telling the Player Where to Go Next

- One thing I *DO NOT LIKE* about our game is how our exit portals are currently used to tell the player where to go (they don't)
- In other roguelike games like The Binding of Isaac or Enter the Gungeon:
	- the rooms have doors
	- So, as soon as the player enters a room, they immediately know where they'll have to go next once they complete the room.
	- In our game, the player does NOT know where they need to go ahead of time.
	- So, if they're looking the other direction when the exit portal pops up, they might not even see it right away.

- We need some *visual indication of where the exit portal is* BEFORE it turns on and lights up.
	- Having a dimmer version of the circle on the floor might not even be enough ngl
	- Maybe we should have doorways in our game and place to portals next to those doorways?

#### Clearing a Floor

##### Make the Big Rooms Feel More Special
- ...yeah

##### Some Type of Statistical Upgrade @ the End of Each Floor
- Right now we have ways to give the player spells, but no consistent way to consistently increase the player's stats as they progress
- We need a way to upgrade the player's stats when they clear the floor
	- More questions?
	- A menu?
	- Some type of special thing spawns in that you interact with???

### In Combat & Combat-Related Things

#### Balancing Primary & Secondary Spells
- One thing I want to avoid is the player mindlessly pressing the primary spell button over and over again until they beat the game
- So, we need to make sure that the secondary spells are powerful and fun enough to use that the player actually wants to use them

##### New Mechanic Idea?
- I want the player to get used to chaining their primary attacks into secondary attacks
- So, let's say the player's primary attack sequence is 4 hits.
- My new mechanic idea is that if the player uses their secondary spell right after their 4th primary attack, the secondary spell will be more powerful (maybe even have an added effect or something).
- This way, the secondary attacks retain their utility if used by themselves
- Players now have a *risk / reward factor* for deciding when to use their secondary spell
	- Do they use it right away for a quick burst of damage?
	- Or do they wait until the end of their primary attack combo for a more powerful effect and risk potentially dropping their combo somehow?

#### Melee Enemies
- I'll focus on creating variations of enemies w/ melee attack animations

#### Make the Enemies Feel More Fair
- One reason why the enemies feel so unfair is that they can hit you from off-screen
	- I'll make so that they're less aggressive when off-screen
- Also, they're not smart enough to realize that the player is currently being attacked by several other enemies at once.
	- I'll try to make it so that only a couple enemies are aggressively attacking the player at once. The other enemies will be less aggressive until some of the other enemies are defeated.

# Environmental Artists

## The Brick


## Other Props

### Rune Icons Lol

Create stylized versions of these: https://www.flaticon.com/free-icons/rune

![](<../../../_Meta/Attachments/Pasted image 20250929191650.png>)



### Better Archway Model