
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

- [ ] Used for a tutorial sequence at the beginning of the game

- [x] Journal table dialogue reaction.
	- [x] Each journal entry has a corresponding dialogue interaction asset

- [ ] Tutorial component base class?
	- [ ] Must check if the dialogue UI is already open and will hold off until it's closed
	- [ ] Proximity-based component w/ pre-set dialogue interactions (that have their own conditions) for tutorial purposes
	- [ ] Room event-based component w/ enum for which room event should trigger it (enter, start, clear, or exit)
	- [ ] Gameplay event-based component - List of event + dialogue interaction pairs that will trigger when the event fires
	

## Small Change to the Shop
- [ ] Rework the relinquish upgrade to just be a boost to one stat instead of taking away another stat first.

## Levels

LDs have been making new blockouts that *should* be functional (but not the prettiest yet). I need to add them to the game.

- [ ] Add new levels to the game

Rework the level generation system to accommodate for new generation structure.

- [ ] Refactor level generation system (Linked List Approach)
- [ ] Experiment w/ giving the player alternate exit choices (to take on harder rooms)

Mikel has been playing around with some new materials for the walls and floors.

- [ ] Update wall and floor materials EVERYWHERE

## Shield Mechanic
- [ ] Add a new stat: shield
- [ ] Change the damage calculation to use shield first, then health
- [ ] Differentiate events for:
	- [ ] Taking damage to shield
	- [ ] Taking damage to health
	- [ ] Taking damage in general
- [ ] Turn the orb in the top left into a shield meter

## Rewards

### Standard Room Rewards
- [ ] Balance existing stat rewards 
- [ ] Balance percentage chances of each reward type
- [ ] Boost money reward from completing rooms

### Boss Rewards
- [ ] Reward for completing boss room within a certain time
- [ ] Reward for completing boss room without taking health damage

## 