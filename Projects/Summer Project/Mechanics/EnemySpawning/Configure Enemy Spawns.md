---
tags:
  - LevelDesign
---
# Configure Enemy Spawns


> [!NOTE] Enemy Spawning System Information
> For general information about the enemy spawning system, see [Enemy Spawning](Enemy%20Spawning.md).

## Folder Organization

All actors related to the enemy spawning system within the level should be placed under `00_Gameplay/Enemies` in the level hierarchy. This includes:
- The enemy manager
- The different spawn areas

![](<../../../../_Meta/Attachments/Pasted image 20261108210354.png>)

## Spawn Areas

Each spawn area holds information about the enemies that can spawn in it, as well as the waves that can spawn in it. 

> [!NOTE] This is Unlike the Old System
> In the old system, spawn areas were not used. Instead, enemies were spawned at specific points in the level. The waves were then configured within the Room Manager's 'Enemy Manager' component. 
> 
> The old system lacked flexibility and made it difficult to manage the spawning of enemies, as well as to create a dynamic and engaging experience for the player.

### Resizing the Spawn Area

Each spawn area has a `Box Component` that defines the area in which enemies can spawn. This box can be moved, rotated, and resized to fit the desired area for enemy spawning.

![](<../../../../_Meta/Attachments/Pasted image 20261108211040.png>)

### Configuring the Spawn Area's Waves

Each spawn area also has a component on it to manage the waves.

After clicking on this component, you'll see a field for `Waves`. Each entry in the `Waves` array represents a new wave that can spawn in this area. Each wave has several properties that can be configured:

![](<../../../../_Meta/Attachments/Pasted image 20261108211320.png>)

#### Budget Generator

> [!Question] What is the budget?
> The budget is a value that determines how many enemies can spawn in a wave. Each enemy type has a budget cost associated with it, and the total budget for the wave will determine how many enemies can spawn at once. For more information, see [Spawn Budgets](Enemy%20Spawning.md#Spawn%20Budgets).


> [!TLDR
> ] Title
> Contents


In this section, we have several options:

The `budget generator type` determines how the budget for the wave is calculated. The options are:
- `Constant Value`
- `Scaled Value` (Default)
##### Constant Value
If using  a constant value, the LD can select a simple number to use as the budget for the wave. This number does not scale based on the player's progress in the game.

##### Scaled Value
If using a scaled value, a new field appears: `Scaling Budget Generator`. The LD need to pick at least one of the options that appears from the drop-down list. The `BP Scaling Budget Generator` is a good choice. It allows the LD to configure:
-  **A base value** - The original number to perform calculations on when generating the budget. This should probably be kept at the default value of 100.
-  **A difficulty modifier** - This is just a multiplier applied on top of the base value. This allows the LD to more easily configure waves that progressively use larger budgets (without needing to touch the base value).
- **Progress Scaling Curve** - A curve that scales the budget based on the player's current progress in the current floor. This should be kept at the default value.

#### Enemy Type Generator