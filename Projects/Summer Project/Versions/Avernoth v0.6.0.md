
# v0.6.0

## Dialogue Pacing

Right now, dialogue portals spawn completely randomly. I want there to be at least some semblance of pacing to it. Ex: the chance of getting a dialogue portal is largely determined on how long it's been since the last dialogue portal spawned.

- [ ] Stat for how many rooms since last dialogue portal
- [ ] Control the pacing of the dialogue more consistently
	- [ ] Curve for chance of dialogue portal spawning based on rooms since last dialogue portal
	- [ ] Bool flag for always getting a dialogue portal on the room manager (should be used for boss room BP)
- [ ] New bool flag on dialogue interactions for overriding the chance to spawn (ALWAYS Spawn)
	- [ ] Used for a tutorial sequence at the beginning of the game

## Small Change to the Shop
- [ ] Rework the relinquish upgrade to just be a boost to one stat instead of taking away another stat first.

## Levels

LDs have been making new blockouts that *should* be functional (but not the prettiest yet). I need to add them to the game.

- [ ] Add new levels to the game

Rework the level generation system to accommodate for new generation structure.

- [ ] Refactor level generation system (Linked List Approach)
- [ ] Experiment w/ giving the player alternate exit choices (to take on harder rooms)

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