
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

## Small Change to the Shop
- [ ] Rework the relinquish upgrade to just be a boost to one stat instead of taking away another stat first.

## Levels

LDs have been making new blockouts that *should* be functional (but not the prettiest yet). I need to add them to the game.

- [x] Add new levels to the persistent level
- [ ] Add new level data assets to the game

Mikel has been playing around with some new materials for the walls and floors.

- [x] Update wall materials 
- [ ] Update floor materials

Spiffy the levels a little
- [ ] Add cobwebs to the walls
- [ ] Add decals to the game

## Alternate Floor Structure

Keys are something new in the game
- [ ] Add a new attribute to the player's attributes for the key
- [ ] Make the UI element for keys visible again
- [ ] Event for spending a key

Rework the level generation system to accommodate for new generation structure.

- [ ] Refactor level generation system (Linked List Approach)
- [ ] Experiment w/ giving the player alternate exit choices (to take on harder rooms)

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

## Rewards

### Standard Room Rewards
- [ ] Balance existing stat rewards 
- [ ] Balance percentage chances of each reward type
- [ ] Boost money reward from completing rooms

### Boss Rewards
- [ ] Reward for completing boss room within a certain time
- [ ] Reward for completing boss room without taking health damage

### Rarity System For Passive Spells

## At Least Two Attack Things From The Doc

Choose at least two powers from that one document we made and implement them functionally

## Work Some More On Enemy AI

# Bugs
- [ ] Dialogue portal collision still on after turning off
- [ ] Journal table spawn chance is still 100%
- [ ] Maybe enemies shouldn't spawn health on death. Reserve that to room completion?
- [ ] Enemies drop rewards a little too often
- [ ] Optional portal not disappearing after room exit
- [ ] Boost money amount?
- [ ] Journal tables spawning with no entries

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
