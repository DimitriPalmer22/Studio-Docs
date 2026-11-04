# Problems with the Current System

Having discreet waves implemented for each room poses several problems
- Hard to quickly iterate on different enemy configurations
- Hard to implement scaling difficulty modifiers
- Incorporating new enemy types quickly becomes a hassle
- Manually revising the enemy configurations of each individual room quickly becomes a multi-person job, and we don't really have multiple people anymore.

# Ideas for a Revised System

Implement a style of enemy room configuration like Hades:
- Don't define exactly how many enemies there are per room, where they spawn, and which ones spawn.

Instead, have a more automated approach.

To make the transition a bit easier & allow for more flexibility in the long run, implement an interface, `IEnemyManager`.
- `StartEnemyManager` - Function to start spawning enemies
- `FinishEnemyManager` - Function to stop spawning enemies. Should also call a function to mark the spawner as complete. This should allow us to finish rooms externally.
- `GetAllEnemies` - Function to get all the enemies currently managed by this enemy manager. Should have no side-effects.
- `ManageEnemy` - Function to make an enemy manager start managing a spawned enemy. Should only really be called by those enemy spawner BPs once the enemy is actually spawned successfully.

## *Automated* Room Managers

- Use a weight-table approach on a per-spawn basis to determine which enemies should spawn.
- Instead of polling the room's floor for valid spawn points, we can just put down a whole bunch of valid points for enemies to spawn.
- The room manager uses a variety of factors to determine which spawn points specific enemies should spawn at.
	- Distance from spawn point
	- Etc.

- Have some parameters like:
	- Enemy amount
	- Difficulty (More difficult enemy variations are weighed more in the spawning table)
	- Define some enemy types that can spawn

## Automated Wave-Based Enemy Manager

Per room, have an enemy manager (there will be different types)
- Define some valid spawn points
- Have some more parameters like:
	- Discreet wave count (if the enemy manager uses waves)

## Automated Time-Based Enemy Manager

Allow enemies to "trickle in".

---

# Google AI Overview

> Prompt
> How does hades enemy spawning work?

In *[Hades](https://www.google.com/search?kgmid=%2Fg%2F11fk4qxvvv&q=Hades)*, enemy spawning is split into a few distinct systems depending on the room type: ==standard wave-based encounters, continuous trickle/survival rooms, and special events==. [Link](https://www.google.com/goto?url=CAEScQHrOzAVxiOUWHlVoGR1ol6ctXa2pMsmmO75USLOoPdCmQovjChXx3PlQkYKJZLhUeRb4cX-on-_7TRzcnkW6CF9B48QJCS4qaXxEDtLVb20oS1au4qZM_gi6ZCRYcfCQwEbmTiTF8m22uaSnuhi4FAg)

1. Standard Wave Encounters

- **Waves:** Most normal chambers spawn enemies in discrete waves (typically up to 3 waves).

- **Next Wave Trigger:** The next wave of enemies will not spawn until you completely clear all active enemies in the current wave.

- **Trickle Waves:** In some layouts (especially with large groups of weak enemies like unarmored witches or numbskulls), enemies might not all pop in at the exact same instant; instead, they "trickle" in as spots open up or delays finish.

- **Spawn Boundaries:** Enemies generally spawn just off-screen or within specific geometric circles tied to the shape and size of the chamber. Experienced players use **spawn manipulation** by standing in specific corners of a room to force future waves to spawn tightly grouped together rather than scattered across the map. [Link](https://www.google.com/goto?url=CAESpAEB6zswFRisg7puVWTeMeje4e9dpaQrvEsRkT_BxTueOdX32MnByY2nJ_J_EI-2s-JOINRgJj-PWLGZ2cH8dJ-bGcqT1NHfUJVUlKHUC__-Cw9LLHmwk72BuExSomKzoUUUfb9hsXYQxxVa5_MwGmVqpgo3NmgeKWlJqTaHFPNWQPgmMhWS5cO4PBmJgo3vyeTnknlRxVQZy9LxbU_1PnE7SlvuyQ)
1. Survival Encounters (Tartarus)

- **How it works:** Occasionally in Tartarus, Hades replaces a standard encounter with a 45-second survival test.

- **No Waves:** Instead of waiting for you to clear a wave, enemies spawn continuously and constantly for 45 seconds.

- **Resolution:** You do not have to kill everything; you just have to stay alive. Once the timer hits 45 seconds, Hades automatically clears out all remaining enemies and the room reward appears. [Link](https://www.google.com/goto?url=CAESZwHrOzAVqqRShyvi6_nG5kv2z0BVNGeeiNDI8lVNdBDccoLeN6jWyuNdi3E17gsQAkzlkxInbgf9gVaauMQirFdoRV02w3UJRrcwQMq9XH7Lmbqi3sncKCIBpFK9DazEVONCK-8W_9Y)

1. Special Spawns & Modifiers

- **Trial of the Gods:** Choosing one god over another causes the spurned deity to trap you and summon extra waves of enemies alongside a localized hazard.

- **Thanatos Encounters:** If Thanatos appears in a non-unique chamber, the total enemy count scales up, and you compete against him to see who can get the most kills.

- **Forced Overtime (Pact of Punishment):** Turning on Forced Overtime does *not* make enemies spawn more frequently or change the wave structure; instead, it speeds up individual enemy spawn-in animations and movement speed. [Link](https://www.google.com/goto?url=CAESpAEB6zswFRisg7puVWTeMeje4e9dpaQrvEsRkT_BxTueOdX32MnByY2nJ_J_EI-2s-JOINRgJj-PWLGZ2cH8dJ-bGcqT1NHfUJVUlKHUC__-Cw9LLHmwk72BuExSomKzoUUUfb9hsXYQxxVa5_MwGmVqpgo3NmgeKWlJqTaHFPNWQPgmMhWS5cO4PBmJgo3vyeTnknlRxVQZy9LxbU_1PnE7SlvuyQ)

---

# Enemy Wave Spawner Scratch Notes

## Split Spawning Up Into Multiple Functions
- Full Spawn Function
	1. ***Bool***: Load the actor class 
	2. Bool: Make the actor appear (spawn it)
	3. ***Void***: Do both & broadcast an event

---
# When Using Auto-Spawners, Determine where Enemies Spawn

Automatic spawners do not use the same spawn point logic as the current system. 

Instead, it calculates optimal positions based on how far they are from the player and how many enemies are already in the room.

## An Interface for `IEnemySpawnArea`

This interfaces describes objects that can spawn enemies. It should have functions like: 
- Determine Spawn Location(?)
- Spawn Enemy(?)

This way, we can describe spawn ZONES, areas where enemies can spawn, and not just specific points. This will allow us to have more dynamic spawning behavior.

## Determining a spawn point for an enemy

> To spawn a BATCH of enemies, we can use an Object to hold information about the batch of spawns.

### 1. Create a list of points uniformly distributed across the area

There are different ways we can do this, but the simplest way is to:
- Have a set number of points that we want to generate
- Use the set number of points to determine a grid size (e.g. 10 points = 3x3 grid)
- Randomly generate points within each grid cell, so that they are uniformly distributed across the area

For areas that do not change in size, this can be determined when the room is created.
### 2. Sort the points based on distance

This makes things a bit easier for fallback scenarios (all the points are too close). 

> This same list will be used for ALL enemies that need to spawn (if multiple enemies are spawning at once). Therefore, we do not need to worry about the performance cost of sorting the list multiple times.

### 3. Filter out invalid points

Use criteria like:
- Whether an enemy has just spawned there
- Distance from the player (filter out points that are too close / too far to the player)
- Proximity to other enemies (use some type of score value to determine how "dense" the immediate area is). If it is in proximity to too many other enemies, it should be filtered out.

### 4. Select a Random Point

Use a weighted random system to select a point from the remaining valid points. The weights can be determined by factors such as:
- Distance from the player (closer points are weighted higher / lower depending on enemy type)
- Proximity to other enemies (points that are too close to other enemies are weighted lower)

### 5. Update the point & Surrounding ones

For this instance of batched enemy spawning:
- mark the point as "used" so that it is not used again for this batch of enemies.
- Mark surrounding points as in proximity to an enemy, so that they are weighted lower for future spawns. This will help prevent enemies from spawning too close together.

