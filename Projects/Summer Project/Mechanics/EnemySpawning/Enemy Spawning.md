# Enemy Spawning

To enhance the game's rogue-like nature, [Avernoth](../../Avernoth/Avernoth.md) will feature a dynamic enemy spawning system.
- This system will ensure that enemies are spawned in a way that keeps the player **engaged and challenged**
- while also maintaining **balance and fairness**.

Levels will ***NOT*** be pre-populated with enemies. Instead, enemy spawning will be reliant upon:
- *The player's current progress throughout the game* - If a level pops up later in the player's run, it ***SHOULD*** feature more enemies than if it were encountered earlier.
- *A pre-configured set of enemy types* - To keep the game balanced, each level will have a set of enemy types that can spawn. This will ensure that the player is not overwhelmed by too many difficult enemies at once.
- *A pre-set number of waves* - Each spawn area in the game will have a pre-set number of waves it can spawn. However, depending on the difficulty, we can scale up the number of waves to spawn in each area.

# Spawn Areas

To facilitate enemy spawning, we will define **spawn areas** within each level. These areas will be used to determine:
- where enemies can spawn 
- how many can spawn at once.

Rather than placing down individual points where enemies can spawn, spawn areas probe the area and determine a set of valid points where enemies can spawn.

This set of points is then used to calculate the optimal spawn point for each enemy based on the player's current position and the other enemies that will be present in the wave.

# Waves

Waves are a batch of enemies that spawn at once within a single spawn area. Waves have several parameters:
- The set of enemies that can spawn in the wave
- The "**budget**" of the wave, which determines how many enemies can spawn at once (each enemy type has a different budget cost)
- The spawn area that the wave will spawn in.
