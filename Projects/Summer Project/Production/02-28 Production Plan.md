# 02-28 Production Plan

Let's say in about two weeks, I want these things to be in the game:
- A much more finalized and polished player attack system. Something we can show an 8 second clip of an have people asking "wait, what game is this?"

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


## Small Update

### Updated Model For Addendums Object (Anvil Thing)
We need to get rid of the anvil as the object the player interacts with to upgrade their tome. Instead, we will replace it with a special writing desk w/ a pen that has magical ink.

### Revise the Model for the Tome Altar
The shape behind the Tome Altar seems a lot like the symbol for the good guys. We should maybe replace it with the symbol for the bad guys. 