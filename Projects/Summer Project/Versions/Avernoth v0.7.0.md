# Feature Updates

## Interaction Priority System
- [ ] If more than 1 item is currently with selection range, but one of them has higher priority than the other, immediately consider the higher priority option

## Spell C++ Classes
- [x] Data asset for sound info so the attenuation settings can be placed somewhere other than my details panel
	- [ ] This should also fix the concurrent sounds issue
- [ ] Function Library for common spell functions (spawn projectile, spawn impact effect, etc)

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