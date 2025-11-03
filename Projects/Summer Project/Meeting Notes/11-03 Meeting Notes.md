## Meeting Times

| Meeting                                | Possible Times |
| -------------------------------------- | -------------- |
| LD Meeting                             |                |
| Narrative Designer + CD Meeting        |                |
| Sound Meeting                          |                |
| Environmental Artist Meeting           |                |
| 2D Artist + Narrative Designer Meeting |                |
| Animation Meeting                      |                |
| Character Artist Meeting               |                |

# Current State of the Game / v0.9.0 Changes


# Goals for v0.10.0:

## Level Design

### Lighting Adjustments

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
- Lighting fs

### Upgrade Room Needs Revision
- The upgrade room was made BEFORE we had a clear idea of what each area of the game would look like, but was fully set-dressed to be a library
- The upgrade ro

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