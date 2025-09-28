# v0.4.0
- [-] Enhance the UI to show the player's stats while in-game?
- [x] Mana regen proportional to how much damage you deal (based on a curve)
- [x] Make that one upgrade work

- [x] Critical hits (using new stat)
- [x] Event for critical hits

- [x] Combo Counter
- [x] Low-poly spheres for various things

- [x] Room rewards component
- [x] Expand upon room rewards
	- [x] Health reward
- [x] Make enemies dropping $ chance-based

- [-] Display debug text for spell names
- [x] Info screen for the currently equipped spells

- [x] Notification subsystem + UI
- [x] Adjust tome API to avoid directly editing the spell array
	- [x] Allow for events when adding / removing spells

## v0.4.1
- [ ] Improve combo counter
- [x] Make spells fire forward, not in the direction of the camera
- [ ] New Questions / Throw in the questions Chelle made rq
- [ ] Fix button conflicts
	- [ ] Find some way to receive UI input while game is paused
- [ ] Fix homing
- [ ] Change font
- [ ] Manual cooldown when finishing a combo?
	- [ ] Keep ability active & change `CanActivate` to consider a cooldown boolean
- [ ] Fix MikelPOC's spawning

## v0.4.2
- [ ] Multiple menus overlapping. Fix it
- [ ] Look into volume mixing
- [ ] Make commands for each player stat


# v0.5.0
- [ ] ENEMIES ffs
- [ ] Tutorial subsystem? + UI + Save Integration
- [ ] Very basic rune ideas / drawings?
- [ ] Only show active spells


# Update Message

# Avernoth v0.4.0

## Spells Screen
- Press I on the keyboard (this button may change in the future idk) to open up the spells screen
- Here you can see a quick overview of your currently equipped spells and their descriptions
- As of right now, its kinda barebones, but it should be functional

## Upgrades
- The empower upgrade now actually works.
- You can get a new passive spell by spending some mana essence
- Note: I know the description of the upgrade says "500 mana essence" while the upgrade actually costs 100. This will be fixed in a future update.

## Critical hits
- Allister has a new stat for critical hit change (default 5%) and a new stat for critical hit damage multiplier (default 1.5x).
- *Most* spells can critically hit, but not all (i.e. the crystal spells)
- Enemies cannot critically hit Allister.

## Combo Counter
- There is now a combo counter on-screen
- It'll definitely look a little different in the future, but for now, it works
- This is useful for any passive spells that depend on your current hit count

## Input Changes
- The game now uses directional input to determine where spells are fired
- So, if you want to switch targets while mid-combo, you can do that by using the movement keys
- Note: I'm still tweaking the values so it may not feel as responsive as it needs to

## Camera Changes
- When not in battle, the camera is pretty much the same
- When in combat, the camera zooms out so you can see much more of the arena 

## Room Rewards & Enemy Drops
- Allister has a new stat: Fortune
- This determines how likely you are to get a reward from a room / how likely an enemy is to drop mana essence
- Before, enemies ALWAYS dropped mana essence. Now they have a chance to
- Before, rooms ALWAYS gave a reward. Now they have a chance to
- Before, rooms would only give mana essence as a reward. Now, they can also drop like 10 health.

