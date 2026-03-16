# 03-16 Production Plan

## New Tasks

### New Set of Attacks & Addendums

- Dimitri - Code
- Andre - Animations
- Mikel - VFX

#### New Primary Spell

- 4-hit combo string of the *tempest* element

#### New Secondary Spell

- ss

#### New *Addendums*

Rage mode addendum - Increase agility, but reduce intelligence.
Flat stat increase addendums:
- 10% increase to health
- 10% increase to mana
- 10% increase to mana recharge rate
- 5% increase to Int
- 10% increase to Agi
- 10% increase to Res

### In-Run Progression

Dimitri - Code

- Make enemies harder as you go further into the run.

Implementation:
- Each room has a data table row associated w/ it, detailing things like the room's name, room rewards, the area the room belongs to, etc. Then, in each room, set the information on the room manager (will require LDs to get out of their levels at some point)
- Each enemy has a data table associated w/ it, detailing different difficulty parameters. Things like stat overrides and any AI or ability class overrides can go here. Make a component that takes in this data row and then applies it to each of the corresponding aspects.

### Another New Enemy Type

Erin - Char?

A new enemy type that:
- Is not totally humanoid
- Is not a quadruped
- Has simple movements that should be easy to model / rig / animate for

### 
