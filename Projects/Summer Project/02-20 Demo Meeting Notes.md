# LEVEL-SPECIFIC

## Beginning Room
- [ ] Room redesign - Smaller & focus more on tome altar
- [ ] New Tutorial Dialogue implementation

## Combat Tutorial
- [ ] Show correct button inputs for each action (NOT WITHIN THE TEXT BECAUSE THAT IS REDICULOUSLY HARD.) Instead, add separate UI elements on the screen to show the correct button inputs for each action. These UI elements should only be visible during the combat tutorial and should disappear once the player completes the tutorial.

## "Boss Room"
- [ ] Redo boss room mechanically
- [ ] Create crystal boss knight w/ hammer
- [ ] Unique attacks?

## Addendum Rooms (Major & Minor)
- [x] Implement tutorial dialogue
- [ ] Addendum assets from Alecks
- [ ] The addendum "anvil" should have stronger VFX that disable once the player uses it.
- [ ] (Ehh) Make addendum screens visually distinct

## Standard Combat Rooms
- [ ] Redistribute the enemy types in the rooms.

# Combat Stuff
## Enemies
### Animation
- [ ] Sync groups for blend space movement animations

### VFX
- [ ] Hammer cracking the floor.
- [ ] Finish the attack telegraphing for the knight enemies.
- [ ] Add the sword VFX back to the sword lol

### SFX
- [ ] Enemy ambient groans
- [ ] Hurt sounds
- [ ] Death sounds
- [ ] Enemy attack sounds

### Enemy AI
- [x] Simplify enemy AI to just be like "attack the player if they're within range" & "if the player is not within range, get closer to the player"
- [ ] Twilight knight is not rotating correctly on its second attack, causing him to dash backwards 
- [ ] Re-add Hammer knight pull

## Allister

- [ ] Cloth physics optimization

### VFX 
- [ ] VFX that stays on his hands as he casts spells. Like he's holding a ball of fire in his hands before he releases the attack.

### SFX
- [x] Attack whooshes
- [ ] Flame volley explosion sounds
- [ ] Crystal explosion sounds

## Bug fixing & Other Stuff

# UI
- [ ] Controller support for menus

### Spell Screen 
- [ ] Implement UI

### Journal Screen
- [ ] Implement UI

### Settings Screen
- [ ] Get this working

# Other Stuff

- [ ] Health and mana essence orb pickups can get an updated look (maybe a different material)

# Things to Test in Playtest

### General
- [ ] Performance

### Dialogue
- [ ] ANY placeholder dialogue at all. It is better off removed than still in placeholder form.
- [ ] Make sure the correct dialogue is triggered at the correct times.
- [ ] Are there any instances where the dialogue camera gets stuck?
- [ ] Make sure correct dialogue is triggered when
	- Starting the very first run
	- Entering the combat tutorial
	- Journal table spawns and stuff.

### Menus & UI
- [ ] Are there any menus that seem poorly explained or confusing to navigate?
- [ ] Are there any instances where the UI gets stuck or doesn't work correctly?
- [ ] Do any of the menus need animations?

### Enemies
- [ ] Are the enemies aggressive enough / are they too aggressive?
- [ ] Do any specific attacks cause performance issues?
- [ ] Do any of the attack animations seem janky?