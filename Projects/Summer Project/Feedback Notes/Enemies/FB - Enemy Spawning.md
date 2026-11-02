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

## *Automated* Room Managers

Use a weight-table approach on a per-spawn basis to determine which enemies should spawn.

Instead of polling the room's floor for valid spawn points, we can just put down a whole bunch of valid points for enemies to spawn.

- Have some parameters like:
	- Enemy amount
	- Difficulty (More difficult enemy variations are weighed more in the spawning table)
	- Define some enemy types that can spawn

## Calculated Wave-Based Enemy Manager

Per room, have an enemy manager (there will be different types)
- Define some valid spawn points
- Have some more parameters like:
	- Discreet wave count (if the enemy manager uses waves)

## Calculated Time-Based Enemy Manager