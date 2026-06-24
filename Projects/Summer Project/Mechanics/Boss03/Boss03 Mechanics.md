# Boss03

![](<./Boss03 Graph.png>)

## Invulnerable Phase

The boss starts out in the **Invulnerable Phase**.

While in the invulnerable phase, the boss:
- will be in an area the player cannot access
- will be completely undamageable (is covered in a shield)
- will periodically buff the other enemies that are currently present (heal them, give them a temporary shield, or boost their damage).

At the same time, 1 (or more waves) of minor enemies will spawn in the arena for the player to fight.
- The number of waves that spawns corresponds to the number of times the boss has entered the invulnerable phase. So, the fight should naturally be more difficult as it goes on.

After the wave(s) are cleared, the boss transitions to the **damage phase**.

## Damage Phase

The damage phase is a timed segment in which the player wants to do as much damage to the boss as possible before it transitions back to the invulnerable phase.
> The player can only do a max of 1/3 of the boss's total health during this phase. If the player does more than that, the boss will transition back to the invulnerable phase early.

At the start of the damage phase, the boss spawns 2 clones of itself. The boss and the 2 clones are then teleported to random (from a list of points) locations in the arena.

Idea: At the same time, a wave of minor enemies will spawn in the arena to distract the player from the boss and its clones. Once the phase is complete, these enemies will die 

If the player hits a clone:
- the player is stunned temporarily, wasting time from the damage phase
- the boss and the clones are then reshuffled to new random locations in the arena.
