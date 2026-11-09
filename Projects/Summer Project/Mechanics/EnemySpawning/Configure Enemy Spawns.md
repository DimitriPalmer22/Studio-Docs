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