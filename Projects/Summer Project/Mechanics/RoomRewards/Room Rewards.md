# Room Rewards

## Manual Acquisition

Room rewards **should NOT be an automatically acquired thing**.
- When they are automatic, the player seems to rarely notice when they are acquired
- Automatic rewards also rob the player of the choice of getting the upgrade or not.

## Spawning Rewards in Rooms

After completing a room, rewards will spawn in dedicated spots within the level. These spots should:
- Be within view of the exit
- Be in a convenient spot:
	- within close proximity of the exit
	- within close proximity to the player at the time of spawn (might cause complications)
- NOT obstruct the player's path to the exit. The player should be able to leave the room without having to pick up the reward.

The player will walk up to these rewards and **interact** with them.
## Rewards As Data

Rewards should be stored as **pools**, allowing random selection from a variety of available items.

Individual rewards should contain data

---

## Components

### ACTOR: Reward Spawn Point
An actor that is placed in a level to designate where a reward can spawn.

There **SHOULD** be a fallback for when a reward cannot spawn at a given point (like if the spawn point isn't placed in the level).
- In this case, spawn the actor where the player currently is
- If we spawn the actor on the player, DISABLE ALL COLLIDERS. Implement this as a virtual function in the base class so that it can be overridden for specific reward actors that need to have colliders enabled.
### ACTORS: Reward Actors
Actors that are spawned in the level to represent a reward. These actors should have a component that can be interacted with. 
- Have them extend from a base reward actor class.
- Include an interaction component in this base class.

### DATA: Reward Pool
A list of representations of rewards that can be spawned in a room. 