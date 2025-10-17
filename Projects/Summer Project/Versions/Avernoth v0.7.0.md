# Feature Updates

## Interaction Priority System
- [ ] If more than 1 item is currently with selection range, but one of them has higher priority than the other, immediately consider the higher priority option

## Spell C++ Classes
- [x] Data asset for sound info so the attenuation settings can be placed somewhere other than my details panel
	- [ ] This should also fix the concurrent sounds issue
- [x] Function Library for common spell functions (spawn projectile, spawn impact effect, etc)

## Knockback (NECESSARY)
Right now, the player is constantly backpedaling because they don't have a way to generate space between themselves and enemies. Adding knockback will help with this.
- [x] Combine flinch and knockback into one system
	- [x] Knockback duration is based on the length of the flinch animation
	- [x] Create a UObject class to pass flinch data around
	- [x] Face the direction of the knockback
- [x] Prevent movement input while being knocked back
- [ ] Projectile Spells apply knockback based on how far they have traveled (tie to the damage falloff curve)

## Enemy AI Improvements

- [ ] Enemy AI struct in C++ for better organization
- [ ] C++ library for common enemy functions
### Key Concept: GOAP & Action Queuing

#### What is an Action?

An "Action" can be represented by a UObject class that contains functions for:
- What to do when entering the state
- What to do while in the state (tick)
- What to do when exiting the state
- When the action is considered "complete"
	- Success?
	- Fail?

#### Action Queue
- Each enemy has an action queue as well as a "current action"
- This way, we can queue up a series of actions for the enemy to perform for an overall goal.
- Some events will clear the action queue (like being stunned or knocked back)
- Some actions will pause the action cue / current action until completion (like successfully dodging an attack)

#### Interrupt Events
- Each action has a set of gameplay event tags that can interrupt the task and potentially the entire queue (use a struct for this: tag + whether it clears the queue or just the current action)

### Key Concept: Revenge Meter & Revenge Counter
With stun locks and knockback, it can be very easy to virtually render an enemy as useless by trapping them in a combo. Enemies should be given at least one opportunity to engage with the player (given they are not immediately killed)

#### Revenge Meter
- As enemies take damage, they build up a "Revenge Meter"
- When the meter fills up, the enemy activates a "*Revenge Counter*"
- This is a hidden value, so the player doesn't know how close they are to triggering it

#### Revenge Counter
- Depending on the enemy type, the counter will be different. It could be one ability or it could be multiple abilities that activate at once.
- A visual effect NEEDS to accompany the activation of the counter so the player knows something is happening.

##### Revenge Counter Type: Invincibility / Super Armor
Generally, they should either make the enemy briefly invincible or have super armor to eliminate flinching. This way, they can attempt to engage with the player.

##### Revenge Counter Type: Movement
Move the enemy toward their desired combat range. For melee enemies, this is closer toward the player. For ranged enemies, this is farther away from the player.

##### Revenge Counter Type: Attack
Perform a specific attack animation. This should probably be paired with super armor or invincibility. 

### Key Concept: Aggression 

"Aggression" is a hidden value that determines how likely an enemy is to perform an action. It is used like a currency that is spent to perform actions.

![](<../../../_Meta/Attachments/Pasted image 20251016033545.png>)

## Rethink Passive Effects Again
- Simple Passive effects that you can just add on
- Passive effects that specifically augment something (only 1 per-slot)
	- For example, you can only have 1 Primary Spell Augment passive effect at a time. Same for secondaries.
	- This way, we can add some unique effects that really change how a spell works

## Enemy Status Effects
- Shield
- Enraged or something (attack faster & move faster)
- Sturdy or something (no flinch)

## Floor End Rooms
- Distribute rewards to player
	- Questions?
	- Shop opportunity?
	- Tome stuff?
- Plot stuff
- Healing items
- Room with a really big portal at the end of it

### Boss Rewards
- [ ] Reward for completing boss room within a certain time
- [ ] Reward for completing boss room without taking health damage
- [ ] Tutorialize this somehow

## Small Change to the Shop
- [ ] Rework the relinquish upgrade to just be a boost to one stat instead of taking away another stat first.

## At Least Two Attack Things From The Doc

Choose at least two powers from that one document we made and implement them functionally

# Notes: Good Enemy AI?

## Case Study: Hades
- Enemies telegraph their attacks clearly
- Each individual enemy has a very small moveset
- Each move is also very manageable on its own / the player can easily react to it, dodge it, counter, etc.

### Swarming the Player
- The real difficulty comes in once multiple enemies are on screen at once and the player has to prioritize threats and manage space effectively
- Hades' hardest moments comes from when the game feels the most chaotic.
- The player is AWARE of all the things that can hit them, but they are bombarded with so many decisions that they have to make in a short amount of time that they inevitably make mistakes.
- For instance, that one room in the first floor where the crystal has super armor and spawns a whole bunch of mini crystals is very difficult because the player has to manage both the super armored crystal (which requires them to dodge and attack carefully) while also managing the mini crystals that swarm them. 
	- If they prioritize the smaller crystals, the fight will never end, as the super armored crystal will just keep spawning more.
	- If they prioritize the super armored crystal, they risk getting overwhelmed by the smaller crystals.

### The more significant enemies
- For the vast majority of enemies, the time to kill is extremely quick. 
- Also, once trapped in a melee combo, enemies are virtually useless.
- However, some enemies pose more of a threat
#### Armored Enemies
- One of the most common ways Hades ramps up the difficulty of specific enemies is by adding armor to them.
- Armor makes it so that the enemies no longer flinch, and it also increases their health pool, which essentially eliminates the two issues listed above.
- Once an enemy loses their armor, they lose these benefits, so the player has to focus on breaking their armor first.

#### 