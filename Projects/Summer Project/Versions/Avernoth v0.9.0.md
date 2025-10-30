## Enemies
- [ ] Change to the primordial Knight
	- The axe idea I had prior w/ the lingering fire is kinda booboo and not significantly different from the twilight mist aoe
	- Instead, have a fire spear that has a couple effects:
		- Getting hit by the spear itself does some pretty harsh damage
		- The spear shoots out a long-ish range fire spiral that BURNS the player over time (burn as a separate status effect from twilight mist)
		- Note: getting hit by the physical spear also applies burn
	- Literally that one fire spear from the Elden Ring DLC

## Sauce & Juice
- [x] In-world combo numbers
- [x] Hide & show player UI when teleporting in and out of rooms
- [ ] Let players know that their attacks are being resisted because of elemental stuff

## Dialogue
- [ ] Demonstration with new questions @ start of run
- [ ] Dialogue for entering stat upgrade room.

## Music
- For each existing music track, create 2 versions:
	- [ ] Out-of-battle (calmer, maybe no drums)
	- [ ] In-battle (heavy drum break)
- Note: each of these should have shorter intros so I can just go straight into the song w/out waiting to get to the good part.
- [ ] Have per-area music pools

## Journal Entries
- [x] Develop a way to track the collected journal entries  (If I haven't done this already)
	- [ ] Also, make journal tables not spawn 100% of the time
	- [ ] Pre-generate the table locations instead of randomly spawning them per-room?
- [x] Make the journal entry spawns sequential
- [x] Give each journal entry an area it can possibly spawn in. Then, if the 

## Level Design
- Note: It is possible for the arenas to feel a little too big.
- Note: Spawning all the enemies in one area as opposed to spreading them out around the player might not feel the best.
- Note: The walks at the beginning of levels can be a little long at times. Having to walk like 10+ before getting into combat is not fun
- In that one area 3 level, there needs to be a significant landmark in the direction of the end of the level. It is a little too easy to get turned around.
- Rooms with identifiable elemental themes
	- Enemy element distribution
	- 2 enemy element types per-room
	- Each room can have ambient particles to convey the element
- Ring for keeping the player within a specific space during combat
- Introduce elemental affinities to the challenge rooms
	- Elemental hazards for the challenge rooms 

## Traps & Hazards
- Lightning strike
- Fire something
- Twilight something


## Significant Upgrade Paths

There isn't much in the way of significantly changing the way the player's character plays over the course of a run. Here are some ideas for significant upgrade paths that could be implemented:

### Much more dramatic statistical upgrades
- The current upgrades in the upgrade room are very miniscule in nature because it was originally assumed the player would have many more opportunities to upgrade their stats over the course of a run.
- However, since the upgrade room is the only place the player can upgrade their stats, the upgrades should be much more significant.

#### Rarity-based system

##### Common
- +2 "ticks" to a stat 

##### Rare
- 4 "ticks" distributed between 2 stats
- -1 "ticks" to 1 stat

##### Legendary
- 6 "ticks" distributed between 3 stats

### Unlock the Potential of an Ability
- Each ability could have a significant upgrade that changes the way the ability works slightly, making it MUCH stronger.
- Add a secondary status or something.
- For example, primordial spells can have a burn effect added to them.

#### Implementation

##### Registration
- Each ability Data Asset also contains an array of Upgrade UObject classes that define the significant upgrades for that ability.
- Each ability can only be significantly upgraded like this once
- The UObject class will have it's own reference to the ability, and will apply its logic whenever the ability is used.

##### Storage
- Each ability instance will have a reference to any significant upgrades that have been applied to it (Note: The abilities MUST be instanced per actor instead of execution for this to work).
##### Activation
- When the ability is initialized, the ability will check if it has any significant upgrades applied to it.
- The upgrades class will have a virtual method for applying its logic whenever the ability is used. (Events that hook into initialize and fire)

### Elemental Status Effects
- Each element NEEDS a status effect associated with it.

### Elemental Synergies
- If enemies are already affected by a status effect of one element, hitting them with another element can make the two interact.
- Think of the technical damage from Persona games.


## Amend Upgrade

### Primaries

#### Flame Volley
- [x] Burn effect on direct hit
- [x] Larger AOE effect
- [x] Further range

#### Tempest Slash
- [x] Piercing effect on hit
- [ ] Lightning is an optional impact effect, signaling an AOE effect that does high damage in relation to base damage
- [x] Further range

#### Shadow Ball
- [x] Last hit fires a light projectile that deals much higher damage
- [x] Larger AOE effect
- [x] Further range

#### Magma Stomp
- [x] Burn Effect on Hit
- [ ] ***uhh***
- [x] Further Range

### Secondaries

#### Simple Explosion
- [ ] Larger AOE effect (Simple Explosion)
- [ ] Smaller AOE effect, but burns enemies that are hit

#### Relay
- [ ] Chains to more enemies
- [ ] Extend the range the initial chain is allowed to travel(?)

#### Crystal Barrage
- [ ] More projectiles
- [ ] Faster cast time? Alternate, faster cast animation?

#### Crystal Explosion
- [ ] Wider arc of projectiles
- [ ] Further range (Simple Explosion)

#### Tempest Axe Kick
- [ ] Longer Range?
- [ ] +1 Piercing?