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

Each spawn area has a `Box Component` that defines the area in which enemies can spawn. This box can be resized to fit the desired area for enemy spawning.

### Configuring the Spawn Area's Waves

Each spawn area should be configured with the following properties: