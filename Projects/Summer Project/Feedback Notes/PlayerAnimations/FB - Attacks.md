# Primary Attacks

## General

- [ ] Combo index (which tempest slash attack to use) is not resetting after animation is finishing…

## Flame Volley
- [x] Re-do flame volley hitboxes(?)
- [x] Re-do the portions of the animation for flame volley
- [x] Re-time flame volley animations again (anim rate for anim sections)
- [ ] Make flame volley finisher fireball bigger visually 
- [ ] FLAME VOLLEY FAR WAS THE ONE THAT CHANGED.

## Tempest Slash

- [x] Attack wind-ups still feel needlessly slow and clunky
- [x] Add multiple hitboxes in a hit group.
	- [x] Tempest 01
	- [x] Tempest Far
- [ ] Not enough forward movement throughout the whole animation for hits 1 and 2
- [ ] The far attack does close distance consistently
- [ ] AOE-based attacks should:
	- [ ] Have a bigger hitbox
	- [ ] Go closer to enemies


## Shadow Ball

- [ ] Change the element of the shadow ball attack (once it's safe to).

# Secondary Attacks

- [x] Implement the ability for the split abilities to be held.
	- [x] In ThirdPersonCharacter, add / remove tag
	- [x] In ThirdPersonCharacter, make it so that holding the button ADDs the tag,
	- [x] Then, make it so that releasing the button REMOVES the tag.
	- [ ] Then, in the UHoldMontageAbilityBase class, respond to the event when the tag is removed instead of added
		- Ngl, this is going to be deprecated anyway so...
	- [x] In montage base, detect when tag is present / removed. (only is the montage portion detects when the button is being held)
	- [x] In tag holder, set up the tag for the secondary being held
	- [x] Drain mana while charging.
		- [x] If mana drain isn't fully complete, don't release the ability
	- [x] Charge start event
	- [x] Charge end event
	- [x] Fully cancel animation when the ability is cancelled (gets hit or mana runs out)
- [x] Remove ability to move during charged attacks.
- [ ] Remove old held ability base class in C++
- [x] Tune the charge time for each ability (currently too long)
- [ ] Gameplay cue when the ability is fully charged

## Crystal Explosion
- [x] Implement as a held split ability
- [x] Spawn crystals
- [x] Fire crystals
- [x] When cancelling the ability (gets hit prematurely or mana runs out), make sure to detach the spawned crystals before destroying them.
- [x] Projectiles only doing 1 damage each

## Relay
- [ ] Implement as a held split ability
- [ ] Charge time is WAYYYYY to long.

