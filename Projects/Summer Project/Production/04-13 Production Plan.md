# 04-13 Production Plan

### Enemy AI

The game's enemy AI is bogus. I have spent the past week trying to improve it, and it is still bogus. I fear the system I set up for using GOAP is far to over-engineered for what exactly I am trying to achieve in this game.

At this point, my implementation is really just a unique version of a state tree. If that is the case, I should just use a state tree for the Enemy AI.

### Enemy Designs

We have basic enemies, but we have nothing to re-order the hierarchy of priorities for the player during combat.
