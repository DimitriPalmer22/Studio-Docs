# Enemy Spawning

To enhance the game's rogue-like nature, [Avernoth](../../Avernoth/Avernoth.md) will feature a dynamic enemy spawning system.
- This system will ensure that enemies are spawned in a way that keeps the player **engaged and challenged**
- while also maintaining **balance and fairness**.

Levels will ***NOT*** be pre-populated with enemies. Instead, enemy spawning will be reliant upon:
- *The player's current progress throughout the game* - If a level pops up later in the player's run, it ***SHOULD*** feature more enemies than if it were encountered earlier.
- *A pre-configured set of enemy types* - To keep the game balanced, each level will have a set of enemy types that can spawn. This will ensure that the player is not overwhelmed by too many difficult enemies at once.
- *A pre-set number of waves* - Each spawn area in the game will have a pre-set number of waves it can spawn. However, depending on the difficulty, we can scale up the number of waves to spawn in each area.

#