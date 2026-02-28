# 02-28 Production Plan

Let's say in about two weeks, I want these things to be in the game:
- A much more finalized and polished player attack system. Something we can show an 8 second clip of an have people asking "wait, what game is this?"
- Lowkey a change in art style / environmental design because our current setup is not as appealing as I think it should be. I want the game to feel more GRAND. I want to be able to show short cinematics of a blockout / level (with appropriate lighting, fog, and effects) and draw people in off of that ALONE.

## Better Player Attacks

The player's attacks *can* feel even better than they already do, but we have to figure out:
- why the combat in existing references work
- how to apply those working strategies to our product

We have to *HARD FOCUS* on this before addressing anything else because the [Combat](<../Avernoth/Mechanics/Combat/Combat.md>) should be the main attractor of our game, and this is the base of that.

### Revised Attack Animations

In my initial assessment of how the attacks should feel, I was wrong about how many frames we would need for the animations to feel good. The current animations are *too short* to have any type of *weight* or real *expression* to them.

Furthermore, the current movement setup we have for attacks is a little janky. Yes, it works in moving the player to the enemies, but that is not ideal (or conventional) for games with combat like this. Typically, games with combat like this don't have the player move very much from their attacking position (UNLESS they are doing an attack that has the main purpose of relocating them). Any in-engine movement is supposed to be very minimal, with only small movements that are meant to help attacks connect if they are just barely out of reach.
- It should be noted that in games with LESS movement per attack animation, the individual attack animations are much more AOE focused.

### Visual and Auditory Effects

X

## Art Style / Environmental Design Update

As of right now, the 3D artists are idle, and I could have them do some major redesigning to the appearance of our current levels (in terms of the kits we use).

After looking at some other references, I realized that our spaces don't feel nearly as *OTHERWORLDLY* as they could. Our current levels feel too much like they can exist an any worldly fantasy setting. I want our levels to feel a little more like they have an air of mystery and danger to them. 

### Proper Level Design Pipeline

### BACKGROUND & SPACE

The background elements can be obscured by **fog**.

## Small Art Update

### Updated Model For Addendums Object (Anvil Thing)

We need to get rid of the anvil as the object the player interacts with to upgrade their tome. Instead, we will replace it with a special writing desk w/ a pen that has magical ink.

### Revise the Model for the Tome Altar

The shape behind the Tome Altar seems a lot like the symbol for the good guys. We should maybe replace it with the symbol for the bad guys.
