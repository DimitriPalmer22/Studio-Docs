# Goals

Place this into ClickUp.

## Combat Improvements

### ANOTHER Combat Test Arena

- [ ] Start working on ANOTHER empty arena space for combat
	- Endless combat arena
	- 5 - 10 waves and then a boss fight
	- After each cycle of waves, increase the difficulty of the enemies (apply gameplay effects)

### DONE Rework Shield (Parry) System AGAIN

Currently, the shield mechanic feels a little… confused. I want it to feel like a more essential skill-based mechanic within the game. It is not an alternative to the dodge. It is a useful way for the player to prevent damage and launch a quick counterattack.
- [x] Shield is only usable when the meter is full.
- [x] Make shield increase gradually (with a gameplay effect)
- [x] Shield regen stat is instead used to control how long it takes for shield to refill.
- [x] Remove functionality for restoring shield on room start
- [x] Ensure tutorial still works with the new shield system.
- [ ] Update the shader on the shield UI item to only glow when the shield is available to be used
- [ ] Also, make the glow more intense.

### Reference Gathering For Target Game Experience

- [ ] Gather more style references for combat animations and game feel
- [ ] I want to increase the number of enemies the player is fighting at once without increasing cognitive load too much. Gather more refs for combat in large crowds so I can better understand how to make this work. (KH2, DMC5, Bayonetta, etc.)

### Upgrade Improvements

The upgrades currently feel useless. The player can kill singular enemies too quickly and larger crowds are still insignificant.
- [ ] Understand how to make upgrades feel more impactful. Gather references for upgrades in other games and analyze how they work. (Crowd control vs. single target upgrades, etc.) -> Hades, DMC5, KH2, Bayonetta, etc.
- <https://u.gg/lol/items>
- <https://wiki.leagueoflegends.com/en-us/ARAM>:_Mayhem/Augments#Hide

- [x] Create a new system for implementing addendums
	- Keep boon rarity as an idea maybe?
	- Use addendum slots to filter
	- Implement GE's using curve tables in case we want to use rarities.
	- Lowkey, that's a LOT of work…
	- Instead, have multiple versions of each w/ different values associated w/ them. Map those values to a curve table.
- [ ] Recreate all of the existing addendums using the new system
- [ ] Get rid of ALL old addendum BPs
- [ ] Remove old attributes class.
- [ ] Re-connect addendums to ribbon UI?
- [ ] Max-health related addendums should heal as well.

- [x] Use the rarity to define the level of the gameplay effect being applied so I can use the curve tables to easily define boosts for each rarity. This will make it easier to balance the addendums.
- [x] Parse the description to add the modifier to the description text automatically.
	- [ ] Fall back to "???" if a value cannot be found.
	- [x] Also parse the duration.
- [x] Distinguish between minor and major addendum screens.
	- [x] Can be easily implemented by having two versions of the screen BP: one for each room.
	- [x] The minor screen only has options for stats, while the major one allows for upgrades to the primary, the secondary, and the dodge.

### Stat Rework

The values of stats need to be re-defined in how they are represented. Currently, I use a curve to define how much a stat is worth. This *works*, but the selected values are arbitrary and don't make much sense in terms of how the player perceives them. I want to make the stat values more intuitive and understandable for the player.

For example, an *Intelligence* stat of 3 means the player does 1x damage… Why?

- [x] Re-do stats so they work on a +/-% scale instead of being a multiplier that is applied to the base value. This will make it easier for the player to understand how much of an effect a stat has on their character.
- [x] Reorganize the attributes file so that it is easier to understand and modify. Right now, it is a bit of a mess.
- [x] Use the item spawn chance as a flat percentage boost that is added AFTER reward chance calculation.

- [x] Health Calculation (GE)
- [x] Mana Calculation (GE)
	- [x] Queued mana cost.
- [x] Shield Calculation (GE)
- [x] Damage calculation
- [x] Critical hit chance calculation & damage
- [x] Move speed calculation
- [x] Rooms w/out dialogue
- [x] Currency & shop
- [x] Storing and retrieving stats from data tables
- [x] Remove elemental stats / store them in another attribute class
- [x] Dodge stats
- [x] Shield stats
- [ ] Convert all GEs to use new attributes.
- [x] Separate gameplay effects by feature / function / accompanying ability
- [ ] Fix tome loadout screen 2.
- [ ] Fix tome loadout screen 3.
- [ ] Rebalance all enemy stats
- [x] Remove applied stats when removing tomes
- [ ] Implement combo counter w/ gameplay effects and stack refreshes
- [x] Implement new attribute class for primary attacks & secondary attack stats.

## Difficulty Rework

Now that the stats represent additive modifiers (and not arbitrary values), I can make a more reliable difficulty system that scales with the levels.
- For each type of enemy, make 1 gameplay effect that affects MULTIPLE stats.
- This GE should also have its own curve table, representing the added stats of the enemy at different levels.
- The "levels" represent the different areas of the game.

## Cutscene Infrastructure

- [x] Allow checkboxes for adding / removing cinematic black bars
	- Add & remove function
- [x] Allow checkboxes for blocking / allowing player input
	- Add & remove function
- [ ] Add a function to remove all active cinematic elements. Useful for removing any black bars or allowing player input early.

## Loadout Tweaks

- [ ] Be a little more intentional with how much starting max mana I give to each loadout. It should be in terms of 1x, 1.5x, or 2x the secondary ability's mana cost.
- [ ] 

## Levels

### Brian's New Level

- [x] Take a look at Brian's new level
- [ ] Implement it in the game if it is ready
- [ ] Document the necessary steps to implement a new level in the game.
	- [x] Mark as lighting scenario in levels menu
	- [ ] Add to data table for level information
	- [ ] Add it to the level pool

### Room Rewards

Currently, getting a room reward is insignificant / the player barely notices when it happens.
- [ ] Make the player interact with a room reward in order to receive it.
	- This means health orbs can no longer just be health orbs alone. They must be an object the player walks up to an presses the interact button on. Then, it can burst into orbs.
- [ ] Point the player's camera to it
- [ ] Call attention to it in a tutorial. Don't allow them to leave without picking it up.
- [x] Force reward flag in generated room info. This is so that the player is guaranteed to get a reward in a room for tutorial purposes.
- [x] Create room reward spawn point actor.
- [ ] Place dedicated spots in each room where rewards can spawn. This SHOULD be within view of the room exit.
- [x] No collision fallback
- [x] Remove shield reward
- [x] Force reward entry (to avoid drawing from pool)
- [x] Create spawners for actors.
	- [x] Need to be added to pools…

### Health & Money Orbs Change

Instead of being a whole bunch of tiny orbs that check for collision, let it be one actor that spawns a whole bunch of GPU-managed particles. This should reduce CPU overhead and make it easier to manage the orbs.
- [ ] Create a new visual for the orbs actor.
- [ ] Create a new health orb actor that spawns a bunch of GPU-managed particles.

### Better Levels Infrastructure

Loading in and out of levels is still a little iffy. I need to find a way to make this work more consistently.
- [ ] Centralize all level load and unload logic to the GameModeLevelComponent. Remove this code from the RoomPlayerStart and RoomPlayerEnd.
	- [ ] This can cause complications with loading the FIRST room initially. Make an edge case to work around this.
- [ ] Re-modularize the room managers so that they are more digestible to manage.
	- The overall framework for a room manager should be very barebones, with it only really having functions for entering, starting, and clearing the room (exposing the exit)
	- After starting the room, use a series of IOngoing components to define what needs to be done before the room is cleared. This way, the room manager doesn't need to know about the specifics of what is happening in the room, it just needs to know when the room is cleared.
	- Sub classes can then define what exactly the player needs to do before the room is cleared. (e.g. kill all enemies, collect all items, etc.)

## Overall Progression

…

## Journal Entries

### Journal Entry Text

- [ ] More placeholder journal entry text.
- [ ] Track this in the docs / spreadsheets.

### Journal Entries Are Boring & Confusing

- [ ] Have a small little level sequence when a journal entry is collected
	- When picking up a journal entry, have a little camera cut when picking up the journal entry
	- THEN, while the cut is still active, show the journal entry text on screen.
	- Remove page from screen
	- Then fade screen back to normal.

### Tracking Journal Entries is in a Horrid Place

- Our journal page UI doesn't work for this… It never has.

## End Rooms

### End Room 01

- 

### End Room 02

- 

### End Room 03

- 
