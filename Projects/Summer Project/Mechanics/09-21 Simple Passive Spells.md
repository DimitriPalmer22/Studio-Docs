# Side Note: The Difference Between Vitality and Resilience

- In practice, vitality (max health) and resilience (defense) often overlap in their effects on a character's survivability.
- However, the character's max health can be seen as a more static attribute that should only be changed relatively permanently (As should the max mana stat).
- Resilience, on the other hand, can be viewed as a more dynamic attribute that can be influenced by temporary buffs, debuffs, and situational factors.

# Parameterizing the Spells

## List of Stats that Passives *Can* Affect
- (Int) Intelligence
- (Res) Resilience
- (Agi) Agility

- Mana regen
- Currency Multiplier
- Room reward change multiplier

- Additional dodges
- Dodge Distance Multiplier

- Critical hit chance
- Critical hit multiplier

## List of Gameplay Events to React to
- Entering a new room
- Exiting a room

- Starting the spawner / "Starting" a room
- New wave start
- Final wave start
- Finishing a Spawner / "Clearing" a room

- Killing an enemy
- Taking damage

# Types of Stat Boosts

## One-Shot, Duration-based Stat Boosts

- Activated by a gameplay event
- Applies a stat boost to a specific stat (using a gameplay effect)
- Ability is considered active for the duration of the effect

| Name | Stat | Event | Duration | Cooldown |
| ---- | ---- | ----- | -------- | -------- |
|      | Int  |       |          |          |
|      | Res  |       |          |          |
|      | Agi  |       |          |          |
|      |      |       |          |          |
|      |      |       |          |          |

## Stacking Semi-Permanent Stat Boosts
- Activated by a gameplay event
- An integer for max stack capacity
- Can either be deactivated by another gameplay event or expire after a duration
- Cooldown is optional

| Name | Stat | Event | Max Stacks | Duration | Cooldown |
| ---- | ---- | ----- | ---------- | -------- | -------- |
|      |      |       |            |          |          |

## Automatic Spell Cast on Event
- Activated by a gameplay event
- Casts a specific spell when the event occurs
- Considered active on a case-by case basis.
- Should not be able to be reactivated while already active or on cooldown


| Name | Event | Description |
| ---- | ----- | ----------- |
|      |       |             |
