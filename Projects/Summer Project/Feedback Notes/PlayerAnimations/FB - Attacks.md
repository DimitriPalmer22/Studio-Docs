# Primary Attacks

## General

- [ ] Combo index (which tempest slash attack to use) is not resetting after animation is finishing…

## Flame Volley
- [ ] Re-do flame volley hitboxes
- [ ] Re-do the portions of the animation for flame volley
- [ ] Re-time flame volley animations again (anim rate for anim sections)
- [ ] Make flame volley finisher fireball bigger visually 

## Tempest Slash

- [x] Attack wind-ups still feel needlessly slow and clunky
- [x] Add multiple hitboxes in a hit group.
	- [x] Tempest 01
	- [x] Tempest Far
- [ ] Not enough forward movement throughout the whole animation for hits 1 and 2
- [ ] The far attack does close distance consistently


## Shadow Ball

- [ ] Change the element of the shadow ball attack (once it's safe to).

# Secondary Attacks

- [ ] Implement the ability for the split abilities to be held.
	- [ ] In ThirdPersonCharacter, add / remove tag
	- [ ] In ThirdPersonCharacter, make it so that holding the button ADDs the tag,
	- [ ] Then, make it so that releasing the button REMOVES the tag.
	- [ ] Then, in the UHoldMontageAbilityBase class, respond to the event when the tag is removed instead of added
		- Ngl, this is going to be deprecated anyway so...
	- [x] In montage base, detect when tag is present / removed. (only is the montage portion detects when the button is being held)
	- [x] In tag holder, set up the tag for the secondary being held
	- [ ] Drain mana while charging.
		- [ ] If mana drain isn't fully complete, don't release the ability

## Crystal Explosion
- [ ] Implement as a held split ability

## Relay
- [ ] Implement as a held split ability
- [ ] Charge time is WAYYYYY to long.

