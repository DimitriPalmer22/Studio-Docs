# 02-28 Production Plan

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
