
# v0.6.0

## Dialogue Pacing

- [x] Function in Old Data Asset to Create new, matching data assets
- [x] Function to check if a dialogue interaction is valid
- [x] Gather and store all dialogue interactions
- [x] Make a new, identical UI that works with the new dialogue struct
	- [x] In the new UI, have the UI purely control the dialogue flow

Right now, dialogue portals spawn completely randomly. I want there to be at least some semblance of pacing to it. Ex: the chance of getting a dialogue portal is largely determined on how long it's been since the last dialogue portal spawned.

- [x] Stat for how many rooms since last dialogue portal
- [x] Control the pacing of the dialogue more consistently
	- [x] Curve for chance of dialogue portal spawning based on rooms since last dialogue portal
	- [x] Bool flag for always getting a dialogue portal on the room manager (should be used for boss room BP)
- [x] New bool flag on dialogue interactions for overriding the chance to spawn (ALWAYS Spawn)

- [x] Journal table dialogue reaction.
	- [x] Each journal entry has a corresponding dialogue interaction asset

- [x] Tutorial component base class?
	- [ ] Must check if the dialogue UI is already open and will hold off until it's closed
	- [x] Proximity-based component w/ pre-set dialogue interactions (that have their own conditions) for tutorial purposes
	- [x] Room event-based component w/ enum for which room event should trigger it (enter, start, clear, or exit)
	- [ ] Gameplay event-based component - List of event + dialogue interaction pairs that will trigger when the event fires

- [x] Rich text boxes
- [x] Interact in-battle flag
- [ ] Button prompt for the optional dialogue stuff
- [ ] Small demonstration / tutorial sequence to show off the capabilities of the new system

BUGS:
- [x] Consider how to validate and invalidate tutorials (just use the tags lol)
- [x] Getting a dynamic dialogue interaction while you have an optional one is gonna remove the optional one. Keep this as a feature?
- [x] Can still control player while the animation for the dynamic dialogue is playing
- [x] Interaction queue?


## Levels

LDs have been making new blockouts that *should* be functional (but not the prettiest yet). I need to add them to the game.

- [x] Add new levels to the persistent level
- [ ] Add new level data assets to the game

Mikel has been playing around with some new materials for the walls and floors.

- [x] Update wall materials 
- [x] Update floor materials

Spiffy the levels a little
- [ ] Add cobwebs to the walls
- [ ] Add decals to the game

## Alternate Floor Structure

Keys are something new in the game
- [x] Add a new attribute to the player's attributes for the key
- [x] Key pickup
	- [x] Add to enemy reward pools
- [x] Key shop item
- [x] Make the UI element for keys visible again
- [ ] Event for spending a key
	- [ ] Create a component that listens to the attribute event in the attribute set and fires off whenever a set attribute is changed. Expose the attribute tags to the BP so I can change them in-engine.

Rework the level generation system to accommodate for new generation structure.

- [x] Button to enter alternate room
- [x] Refactor level generation system
- [x] Experiment w/ giving the player alternate exit choices (to take on harder rooms)
- [x] UI to show the player when they can go to an alternate room
- [ ] Tutorial / story stuff for alternate room
- [ ] Rewards for alternate rooms

## Shield Mechanic
- [x] Add a new stat: shield
- [x] Change the damage calculation to use shield first, then health
- [x] Differentiate events for:
	- [x] Taking damage to shield
	- [x] Taking damage to health
	- [x] Taking damage in general
- [x] Turn the orb in the top left into a shield meter
- [x] Shield shop item
- [x] Shield item pickup
- [ ] Shield item tutorial

## Interaction System Improvements
- [x] Alternate interaction button
- [x] In-world button prompt for interaction
- [x] Make the interaction component a scene component so I can use that for positioning on the button prompt

## Rewards

### Standard Room Rewards
- [ ] Balance existing stat rewards 
- [ ] Balance percentage chances of each reward type
- [ ] Boost money reward from completing rooms

### Rarity System For Passive Spells

# Bugs
- [x] Dialogue portal collision still on after turning off
- [ ] Make sure room has been entered before allowing trigger collisions
- [ ] Journal table spawn chance is still 100%
- [ ] Maybe enemies shouldn't spawn health on death. Reserve that to room completion?
- [ ] Enemies drop rewards a little too often
- [ ] Optional portal not disappearing after room exit
- [ ] Boost money amount?
- [ ] Journal tables spawning with no entries
- [x] Pickups (like the stat upgrade pickup) need to auto-destroy on room exit
- [ ] Boss rooms sometimes getting stuck after clearing out all enemies in the room.
- [ ] Rotate character sprites to face the opposite way
- [ ] Some levels don't have the skybox
- [ ] Dialogue portal needs to use the post processing manager instead of its own post processing
- [ ] Double shop menu
- [x] "+-" on currency UI

# Update

## Major Dialogue Update

### Dialgoue UI Update
- Characters bob up and down a little while in the dialogue screen
- ***The dialogue UI now supports rich text***, allowing us to have more control over the appearance of individual words & characters. It's a *teeny* bit wonky right now, so there are some quirks to work through. But, it should be good enough to use for formatting individual words.

### Per-Character Talking Sounds
- Added support for each character having their own "talking" sound effect.
- The game is still using the same old placeholder sound, but every character's sound is pitched differently to give them some uniqueness

### Dialogue Types
There are now three types of dialogue interactions:
- **Static Dialogue Interactions** - These are the dialogue interactions that we've always had. The player walks up to a portal (or some other object that activates dialogue) and presses the interact button to start the dialogue interaction. These are mainly for the shop and upgrade room.
- **Dynamic Dialogue Interactions** - Instead of Allister having to walk up to some object to interact with it, a little dialogue portal appears next to Allister and the dialogue starts automatically. These are mainly for key story beats and tutorial purposes. Anything that we want to make sure the player sees would most likely be a dynamic dialogue interaction. 
- **Optional Dialogue Interactions** - Similar to the dynamic dialogue interactions, a little dialogue portal appears next to Allister. However, the player has the option to ignore it and continue playing. The player would have to press a dedicated button (Q for right now) to start the dialogue interaction. These are mainly for flavor text and lore purposes. The room clear dialogue interactions are an example of optional dialogue interactions.

### Tutorialization
Using the new dynamic dialogue interactions, we can now tutorialize the game a lot better. As of right now, there are a couple scenarios in which tutorial dialogue can pop up:
- The player approaches an object that requires a tutorial (like the journal table)
- The player enters a room
- The player clears all the enemies in a room
- The player exits a room (the dialogue won't start until the player loads into the next room)

### Journal Table Update
- Now, each journal table entry has an accompanying dialogue interaction that plays after the player finishes reading the entry. 
- This should help give the journal table feel more integrated into the world and story of Avernoth. 

### Better Pacing of Room Clear Dialogue
- Before, the change of getting room clear dialogue after clearing a room was completely random.
- Now, the chance of getting room clear dialogue is based on how many rooms it's been since the last time you got room clear dialogue.
- If it's been like 6 rooms since the last time you got a room clear dialogue, then getting one is guaranteed.



# Avernoth Update v0.6.0

## Dialogue Overhaul
- Dialogue portals no longer spawn directly on the exit of the room when clearing a room. This interrupted gameplay too much.
- Now, a tiny little portal appears next to Allister, and the player can *choose* to read the dialogue (there is a button prompt for this) or to ignore it and continue playing.
- *Mandatory* dialogue interactions will play automatically
- Journal tables now have accompanying dialogue after the player reads the journal entry
- The characters bob up and down while the dialogue UI is open
- Each individual character has their own talking sound (Still placeholder tho)

## Levels!!!
- The look of the levels has changed significantly. Mikel made new wall and floor materials that should be updated pretty much everywhere.
- LDs have been making new blockouts that should be functional, but aren't completely set-dressed yet
- Over the past week, I think we've gotten like 4-5 new levels
- They are NOT in the rotation of levels yet, though
- Right now, I'm having the LDs focus on functional blockouts to ensure that gameplay is good while we finish the art for the levels

## "Choosing" Rooms to Go into
- Before, the layout of the game was completely linear and boring. I wanted to give the player more *meaningful choices*
- New item: "keys" (the thematic representation of these keys is still being worked on). You can see your "key" count in the top left corner of the UI next to the money
- At the end of each room, if you have a key, you can choose to spend it to go into an alternate "*challenge room*". These rooms are harder, but they give better rewards.
- Challenge rooms will be modified versions of EXISTING levels that are made more difficult
- As of right now, there are no dedicated challenge rooms, but the functionality of choosing rooms is there and (mostly) working

## Shield Mechanic
- A shield meter has been added to the game.
- That fancy looking orb in the top left is actually used for something now!
- The shield meter fills up when you pick up shield orbs from killing enemies or from buying them in the shop
- The shield will absorb damage before your health does
- The player's defensive stats DO NOT affect damage calculation on the shield.
- When the shield breaks, there is a pretty cool effect to go with it
- Why a shield?: Part of the game's current reward calculation system is tied to how long it has been since the player has taken damage to their *HEALTH*. The shield acts as a buffer to prevent the player from taking damage to their health, which should help them get better rewards.
- Also, I needed something else to put in the shop.

## Interaction System Improvements
- The interaction system has been refined a little bit
- Now, instead of the interact prompt popping up at the bottom of the screen, it appears either on Allister or on the object that you can interact with
- Also, there are button prompts shown for interactions now