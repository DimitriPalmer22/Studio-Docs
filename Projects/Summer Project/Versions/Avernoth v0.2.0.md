- [ ] Enhance the UI to show the player's stats while in-game
- [ ] Mana regen proportional to how much damage you deal (based on a curve)
- [ ] Make that one upgrade work
- [ ] Make commands for each player stat


### Rethinking Secondary Spells

Instead of having them be spells that stand completely on their own, we should make them combo better with the primary spell combo chains.

Basically, each secondary can be used for two things:
- Extending your primary combo chain to create a fluid onslaught of attacks (Like the finishers in the Kingdom Hearts series). The secondary should fluidly chain into and out of the primary attack chain.
- A powerful, flashy spell that can be used alone

With that being said, the secondaries can no longer be these long grand sequences that take forever to play out. They need to be quick, flashy, and impactful. They need to be fluid enough to look natural when used alongside the primary attacks.

https://www.youtube.com/watch?v=adFkvrsxQYo


### Revenge Counter

Enemies are still being trapped in combos and we have no real way to have them react to the player attacking them once they get caught in a combo.

We *could* implement a "Revenge Counter" system (like Kingdom Hearts), where if an enemy gets hit by a certain number of attacks in a short period of time, they will break out of the combo and retaliate with a powerful counterattack that has super armor.


### Idea to Enhance Primary Spell

With the way the current system is designed, the primary spell essentially acts as a vehicle which has the sole purpose of charging the player's mana until they can use their secondary spell.

We don't want this. For the sake of variety in gameplay and making the primary spells more viable (maybe even for build-crafting purposes), we could have a "Finisher" system for the primary spells.

Basically, there is a separate bar for the primary spells that is constantly depleting. It fills up whenever the player hits an enemy with a primary spell. Once the bar is full, the player can perform a "Finisher".

This Finisher is just an extra-powerful version of the last hit in the primary spell combo chain. It does extra damage, staggers enemies, and has some extra flashy VFX.

### Refactor the Spell System
- 