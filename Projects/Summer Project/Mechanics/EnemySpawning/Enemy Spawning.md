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

## Configuring Waves

Considering the fact that each spawn area can have its own set of waves, we can configure waves on a per-spawn area basis.
- This means attaching the wave setup to the spawn area's actor itself (via a component)
- Each spawn area can have it's own `index` property, allowing for proper ordering of the different spawn areas. This is not needed for rooms with a single spawn area, however.

Then, we can have one centralized actor that manages the spawning of waves across all spawn areas in the level. This actor can be responsible for:
- Keeping track of which spawn area is currently active.

## Additional Waves

Sometimes, an extra wave (or more) can be automatically spawned after the initial waves are defeated.

This can be used to increase the difficulty of a level or to add more variety to the gameplay.

This happens on a per-spawn area basis.

> [!Question] *How do we determine what enemies spawn?*
> We look at all the other waves within the spawn area and randomly pick one of it's wave of enemies.

> [!Question] *How do we determine the budget of the wave?*
> Get the maximum budget of all the other waves in the spawn area and use that as the budget for the additional wave. This ensures that the additional wave is not too difficult or too easy compared to the other waves.

# Spawn Budgets

To calculate how many of each enemy type can spawn in a wave, we will use a **budget system**. Each enemy type will have a budget cost associated with it, and the total budget for the wave will determine how many enemies can spawn at once.

Calculating the budget for a wave can be done in several ways:
- A constant budget for the wave
- A budget that scales based on the player's current progress in the game

In most instances, we will be using the budget that scales based on the current progress in the game.


#