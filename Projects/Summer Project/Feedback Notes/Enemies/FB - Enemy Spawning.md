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

Per room, have an enemy manager (there will be different types)
- Use a weight-table approach on a per-spawn basis to determine which enemies should spawn.
- Define some enemy types that can spawn
- Define some valid spawn points
- Have some parameters like:
	- Enemy amount
	- Discreet wave count (if the enemy manager uses waves)
	- Difficulty (More difficult enemy variations are weighed more in the spawning table)