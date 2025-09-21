# Side Note: The Difference Between Vitality and Resilience

- In practice, vitality (max health) and resilience (defense) often overlap in their effects on a character's survivability.
- However, the character's max health can be seen as a more static attribute that should only be changed relatively permanently (As should the max mana stat).
- Resilience, on the other hand, can be viewed as a more dynamic attribute that can be influenced by temporary buffs, debuffs, and situational factors.

# Parameterizing the Spells

## List of Stats that Passives *Can* Affect
### Character Stats
- Current Health
- Current Mana

- (Int) Intelligence
- (Res) Resilience
- (Agi) Agility
- Mana regen (on spell hit)
### Reward Stats
- Currency Multiplier
- Room reward chance multiplier

### Dodging Stats
- Additional dodges
- Dodge Distance Multiplier

### Critical Hit Stats
- Critical hit chance
- Critical hit multiplier

### Slot-Specific Spell Boosts
- Primary Attack Power
- Primary Attack Cast Speed
- Secondary Attack Power
- Secondary Attack Cast Speed

## List of Gameplay Events to React to
### Area/Floor-Based
- Starting an area/floor
- Clearing an area/floor

### Room-Basad
- Entering a new room
- "Starting" a room
- "Clearing" a room
- Exiting a room

### Spawner-Based
- Starting the spawner
- New wave start
- Final wave start
- Finishing a Spawner

### Combat-Based
- Killing an enemy
- Taking damage

- Starting a dodge
- Ending a dodge
- Using all successive dodges
- Performing a perfect dodge

- Started a combo
- Finished all hits in a combo

- Landing a critical hit

- Full health
- 50% health or less
- 25% health or less
- Dead (with extra lives)

# Types of Stat Boosts

## One-Shot, Duration-based Stat Boosts

- Activated by a gameplay event
- Applies a stat boost to a specific stat (using a gameplay effect)
- Ability is considered active for the duration of the effect

| Stat | Event | Duration | Cooldown |
| ---- | ----- | -------- | -------- |
| Int  |       |          |          |
| Res  |       |          |          |
| Agi  |       |          |          |

### Apply Effect Whenever Starting a Spawner

| Stat  | Event        | Duration | Cooldown |
| ----- | ------------ | -------- | -------- |
| cMana | SpawnerStart | N/A      | N/A      |
|       | SpawnerStart |          |          |
|       | SpawnerStart |          |          |

### Reward for Clearing a Room


### Rewards for Perfect Dodging


### Follow-ups for Successive Dodges

 
## Stacking Semi-Permanent Stat Boosts
- Activated by a gameplay event
- An integer for max stack capacity
- Can either be deactivated by another gameplay event or expire after a duration
- Cooldown is optional

### Cumulative Rewards for No-Damage Rooms
As you go through rooms w/out taking damage, you gain stacks of a stat boost. Taking damage removes all stacks.

| Stat | Event      | End Event | Stacks | Cooldown |
| ---- | ---------- | --------- | ------ | -------- |
| Int  | Room Clear | Damaged   | 5      | N/A      |
| Agi  | Room Clear | Damaged   | 5      | N/A      |
| Res  | Room Clear | Damaged   | 5      | N/A      |
|      |            |           |        |          |
| $x   |            |           |        |          |
| Rew% |            |           |        |          |
|      |            |           |        |          |
|      |            |           |        |          |

### Active in Room Until Taking Damage
Only allow 1 stack. Taking damage removes the stack. Starting a new room applies the ability.

### Active in Area/Floor Until Taking Damage
As you start a new floor / get granted the ability, you gain the ability. Taking damage removes it.

### Increment on Wave Until Taking Damage
As you start a new wave, you gain a stack. Taking damage removes all stacks. Clearing the spawner also removes all stacks.

### Increment on Kill Until Taking Damage
As you kill an enemy, you gain a stack. Taking damage removes all stacks.

### Rewards for Full Health


### Rewards for Full Mana


## Automatic Spell Cast on Event
- Activated by a gameplay event
- Casts a specific spell when the event occurs
- Considered active on a case-by case basis.
- Should not be able to be reactivated while already active or on cooldown


| Event | Description |
| ----- | ----------- |
|       |             |
