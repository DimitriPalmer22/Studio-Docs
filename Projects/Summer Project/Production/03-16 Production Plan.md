# 03-16 Production Plan

## New Tasks

### New Set of Attacks & Addendums

- Dimitri - Code
- Andre - Animations
- Mikel - VFX

#### New Primary Spell

- Tempest element
- 4-hit combo string

#### New Secondary Spell

- Tempest element
- Spinning attack with an AOE

#### New *Addendums*

Rage mode addendum - Increase agility, but reduce intelligence.
Flat stat increase addendums:
- 10% increase to health
- 10% increase to mana
- 10% increase to mana recharge rate
- 5% increase to Int
- 5% increase to Agi
- 5% increase to Res

### In-Run Progression

Dimitri - Code

- Make enemies harder as you go further into the run. Shield?

Implementation:
- Each room has a data table row associated w/ it, detailing things like the room's name, room rewards, the area the room belongs to, etc. Then, in each room, set the information on the room manager (will require LDs to get out of their levels at some point)
- Each enemy has a data table associated w/ it, detailing different difficulty parameters. Things like stat overrides and any AI or ability class overrides can go here. Make a component that takes in this data row and then applies it to each of the corresponding aspects.

### Another New Enemy Type

Erin - Char?

A new enemy type that:
- Is not totally humanoid
- Is not a quadruped
- Has simple movements that should be easy to model / rig / animate for

A summoner!
- For now, we'll have it summon the basic melee enemy, but we can make it summon a specific enemy type in the future as well.
- It will try to maintain it's distance from the player

### Narrative Stuff

Chelle - Narrative

### LD Stuff

Mikel - Level Design & 3D Modeling
