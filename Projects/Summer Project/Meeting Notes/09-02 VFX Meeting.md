# VFX Philosophy

I want there to be more movement on-screen when the player is not doing anything. This would make the game feel more alive and active.

- Make use of the 'heat haze' effect that distorts the screen more.

# Art Style of VFX

- It's all magic
- Over-the-top dramatic VFX
- More stylized PSX look like *Tenebyss*

# What types of Things need VFX?

### Characters & Combat

#### Player

- Player Spells
	- Charge
	- Actually doing the attack
	- Impact
- Any movement ability
	- Dodge
	- Perfect Dodge fr
- Taking damage
- Healing

#### Enemies

- Enemy Attacks
	- Anticipation
	- Actually doing the attack
	- Impact
	- Melee attack trails
- Enemy deaths
- Taking damage
- Healing
- Mana essence orbs

### Environment

#### Visually Interesting

- Crystals
- Cages
#### Interactable Props
- Journal Table
- Room Exit
- Dialogue Portal

#### Ambient VFX

> Different environments should have different ambient VFX. i.e. an outdoors environment should not have the same vfx as the gold glowy things inside the rooms.

- Room sparkle things

#### Light Sources

- Lanterns
- Chandeliers
- Candles
- Torch? (If we're feelin torches)

#### Surface Detail & Things to make things interesting

- simple shapes & circles (that move) throughout the environment to add detail


# Design Language

For each "Thing" that requires VFX, how are we gonna go about consistently representing it using VFX?
- For example, how should *ALL* movement abilities be represented using VFX?

> Note: Creative liberties can be taken to add more flair to the VFX, but the core design language should be consistent with what has been written here.

- Movement abilities (Player or enemies): 
	- long trails
	- dust clouds
	- screen distortion at the point of where they started their movement

- Player spells (Look at the bow spell in Elden Ring & the purple fireball spell in *Tenebyss*)
	- Upon release - a release of energy
	- The projectile itself should have:
		- Aura
		- Maybe a trail (if appropriate)
	- Upon Impact - a release of energy

- Melee Attacks
	- "Sword trails" that communicate the hitbox of the attack
	- Upon hit - a release of energy
	- Heavier attacks should have an additional VFX thing to make them feel more impactful
		- For example, in Tenebyss, the spinning sword attack has an extra layer f 