## Meeting Times

| Meeting                                | Possible Times |
| -------------------------------------- | -------------- |
| LD Meeting                             | Tuesday 8 pm   |
| Narrative Designer + CD Meeting        |                |
| Sound Meeting                          |                |
| Environmental Artist Meeting           | Saturday @ 3pm |
| 2D Artist + Narrative Designer Meeting |                |
| Animation Meeting                      |                |
| Character Artist Meeting               |                |

# Current State of the Game / v0.9.0 Changes

## Upgrades!

### Upgrade Menu UI Overhaul
- The whole book idea was too busy and cluttered.
- The UI has been streamlined to show the three upgrade options in a horizontal list.

### "Relinquish" Upgrade Reword
- Before, the Relinquish upgrade would downgrade 1 stat by a random amount and upgrade another stat by a random amount.
- BUT, that felt bad to the player, because they were losing something and weren't gaining much in return.
- Now, the Relinquish upgrade will downgrade 1 or two random stats by a 1, but will upgrade 1 or more other stats by several notches, improving the utility of this upgrade
- Also, the list of stats that can be upgraded or downgraded is much longer than it was before. 

### Removed "Overwrite" Upgrade / New "Amend" Upgrade
- The overwrite upgrade was useless and confusing.
- It replaced one of either your primary or secondary spells with a new random spell.
- This wasn't really an upgrade, as you wouldn't really get stronger.
- The new "Amend" upgrade improves either your primary or secondary spell in some way with a new unique effect.
- So, this upgrade actually makes you stronger as you play the game.

### Upgrade Animation Implemented
- A placeholder animation plays when the player selects an upgrade from the upgrade menu.

## Passive Spell Pickup

- The passive spell pickup now has a new look (still WIP)
- It is a floating piece of paper with some magical runes floating around it
- This way, it's a little more obvious that this is a passive spell pickup, rather than some abstract thing.

## Burn Status Effect

- When hit by the primordial (fire) knights, the player will catch fire

## New Beginning Room WIP

- A new beginning room is currently being worked on

# Goals for v0.10.0:

## Completing A Run / Beating the Game

### Beating the Last "Boss" Room
- After beating the last boss room, a special exit portal appears
- This portal takes the player to a special ending room
- There is a magically sealed door in this room.
- Here, the player is presented with some final dialogue
- However, Allister and his friends realize "yo, we still don't really know how to get Allister out of there. How do we open this door?"
- So, he has to restart the run again to find out how to open the door

### All Journal Entries = True Ending Obtainable
- The journal entries are connected to getting the true ending of the game.
- It is impossible to get all X journal entries in a single run, so now there is a real incentive to do multiple runs.
- Once all journal entries are collected, the door at the end of the run can be interacted with.
- Once the door is open, the screen fades and the credits roll.

## Level Design

### Lighting Adjustments in Most Rooms

- I want the lighting to be, like, completely figured out. 
- An established style for how levels should be lit would be great.
- Most of the levels in the game suffer from one of two lighting-related issues:

#### Too Evenly Lit
- Most levels are lit very evenly, with little contrast between light and shadow.
- This makes the environments seem flat and uninteresting, with nothing to really draw the player's eye.
- Adding more dynamic lighting and shadows would help create a more immersive atmosphere, and immediately makes the levels seem much more finished.
#### Too Dark
- The levels that are dynamically lit often end up being much too dark.
- Yeah, they look cool, but at the expense of playability.
- Finding a good balance between atmosphere and visibility is key here.

### Beginning Room
- Move the exit portal closer to that door on the right side of the room
- Lighting

### Special Rooms:
- The layout of special rooms should be more standardized and consistent across the game.
- The special "thing" of the room (i.e. the shopkeeper, the upgrade station, the passive item pedestal, etc.) should always be near the direct center or back center of the room.
- It might be best if the exit portal was near some doorway that led out of the room. 
- This way, we can clearly indicate the two most important points of the room. 

#### Upgrade Room Needs Revision
- The upgrade room was made BEFORE we had a clear idea of what each area of the game would look like, but was fully set-dressed to be a library / study room.
	- As a result, it only thematically fits in Area 1.
- The upgrade room needs to be reworked to be a little more generic, allowing it to fit in any area of the game.

#### Shop Room Needs Revision as Well
- Same deal as the upgrade room.
- The overall shape needs to be redone, as the upgrade room we have right now has ALWAYS been a placeholder.

#### A Design For the Passive Upgrade Room
- This is a brand new room type that I kinda threw into the game out of nowhere, so there isn't really a set design for it yet.
- Ideally, there is a pedestal in the center of the room with a passive spell on it, and the player walks up to it and interacts with it to get the passive spell.

## VFX

### On Fire VFX
- When the player is on fire, we need a visual effect to indicate that. 
- There currently is one, but it's literally the dialogue portal slapped on top of the character.
- It doesn't need to be flashy, just something to indicate the status effect.
- Should also be unintrusive enough to not totally block the player's view of their character.

### Tempest Knight VFX

#### Pt. 1: Radius of the Area of Effect
- A circular icon should appear on the floor showing the radius of the tempest knight's area of effect attack.
- The enemy's animation telegraphs when the attacks is coming, but it might also be worth having a visual indicator on the floor as well.
	- For the sake of simplicity and ease of implementation, this could probably be a separate VFX

#### Pt. 2: Attack VFX
- The actual attack pulls in the player and damages them if they are in range.
- The VFX for the attack itself should indicate that it's pulling the player in.
- This probably be a swirling wind effect that moves towards the center of the circle or something

### Exit Portal Revamp

#### Different Portal Designs
- Right now, the exit portals all look the same.
- There should be some indication of what the next room is just by looking at the portal.

##### Different Room Types:
- Standard Room (Combat)
- Tome Upgrade Room (Choose an Upgrade from the Menu)
- Passive Upgrade Room (Get a new random passive ability)
- Shop Room
- "Boss" Room

### Magma Stomp VFX
- The trail that goes from the player to the enemies protrudes from the ground a little too much to the point where it obstructs vision
- The burst effect when the attack hits an enemy is also a little too big and obstructive

### Further Refine the Passive Spell Pickup
- Make it look cooler idk

## 2D Art

### More Button Prompts

#### XBOX Controller
- [ ] A Button
- [x] B Button
- [ ] X Button
- [ ] Y Button
- [ ] Start Button (Pause Menu)
- [ ] Back Button (Information Screen)
- [ ] Right shoulder (Lock-on)
- [x] Left Trigger (Alternate Interact)

#### Keyboard n Mouse
- [x] E Key (Interact)
- [ ] Z Key (Alternate interact)
- [x] Q Key (Optional dialogue)
- [ ] X Key (Skip dialogue)
- [ ] Escape Key (Pause Menu / Back)
- [ ] P Key (Pause Menu)
- [ ] Middle mouse button (Lock-on)
- [ ] I Key (Information screen)

### UI Stuff

#### Upgrade Menu Assets

## Animation

### Generic Interact Animation
- Allister now plays an animation whenever the player interacts with something
- But, the animation is just a placeholder right now
- We need a generic interact animation that can be used for anything the player interacts with (journal tables, the shop, upgrade stations, exit portals, etc.)
- The animation could literally be as simple as him holding his hand out

### Upgrade Animation
- An animation plays out when the player selects an upgrade from the upgrade menu
- Right now, the animation is just a placeholder
- We need an animation that shows Allister reacting to getting stronger
	- Not a Dragon Ball Z-level animation, but something that shows he's a little stronger now

### Tempest Knight Attack Animation: Slamming Hammer
- The hammer is a large, two-handed weapon
- The attack animation should be pretty much this, but slower: https://youtu.be/PFDndCXxbUI?si=TaVinizBTvLAEwhl&t=437

### Primordial Knight Attack Animation: Spear Thrust
- The spear is a long, two-handed weapon
- The enemy does a quick thrust with the spear
- A short range burst of fire shoots from the spear as well, inflicting damage to the player 
- The attack animation could look something like this: https://youtu.be/W0j2YzlkT0k?si=eWaW6Ym7BuefY5GF&t=49

## 3D Art

### Continue Working on the Stuff You're Already Working On

### Enemy Weapons

Small Plan:
- Find placeholder weapons to use as size references
- Send them to the artists so they can make the asset
- Animator will use the placeholder to animate with
- Once the asset is done, swap it in