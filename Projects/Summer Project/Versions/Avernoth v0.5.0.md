# v0.5.0
- [x] ENEMIES ffs
- [x] Very basic rune ideas / drawings?

# Avernoth v0.5.0
### Melee Enemies
- I made a variant of the knight enemy that has a melee attack animation. 
- I wasn't lying this time I actually did it.

### Boss Room Update
- Boss rooms are now timed
- Every X seconds, a new wave of enemies spawns (regardless of if you've defeated the previous wave)
- If you defeat a wave before the next one spawns, the next wave spawns immediately
- The more waves you defeat before the timer is up, the better reward you get

Boss Room Rewards:
- Tier 1 (Completed No Extra Waves): Passive Spell Pickup & 50 money
- Tier 2 (Completed Some Extra Waves): Passive Spell Pickup & 100 money
- Tier 3 (Completed A lot of Extra Waves): Passive Spell Pickup & Stat Upgrade Pickup & 150 money

### More Rewards for Completing Standard Rooms
- Restore health - 10% chance
- Mana Essence (Money) - 40% chance
- *Stat Upgrade Pickup (New)* - 40% chance
- *New Passive Spell Pickup (New)* - 10% chance

- These rewards have a chance to drop on after you kill the final enemy in the room. The item will spawn on the enemy's body.
- Their chance to drop is based on how many rooms it has been since you last took damage & how fast you completed this room.
- The chances of each item are still being balanced!

### Rune VFX
I made a VFX asset for runes that I threw on:
- the upgrade room (WIP)
- the shop room statue (WIP)
- the things at the beginning of the game that give you the questions (WIP)
- the stat increase pickups
- the passive spell pickups (WIP)

### Cooler Slow-motion Effect when Clearing Rooms
- The slow-motion effect when you clear a room is now more dramatic
- The bloom increases
- Time slows down even more dramatically when clearing a boss room

### Timer in The Top Right Corner
- There's now a timer in the top right corner that shows how long you've been playing this run
- Future mechanics will rely on this timer. For right now, though, it's just for show.
- Timer stops during dialogue, so you don't have to rush through the dialogue to get a good time!

### Test: Using a Secondary @ the End of Your Primary Combo Increases it's Damage
- I wanted to encourage the player to more intentionally combo their primary attacks into their secondary attacks
- So, after you've completed your primary attack chain, if you use your secondary attack quickly, you get a boost to your secondary attack's damage
- You'll know you did it right if you see a VFX asset spinning under the player

### Primary Attack Buff / Enemies Nerfed a Little
- All primary attack spells have been buffed a little bit
- I tried to keep their time-to-kill about the same as each other

[10-03 Item Spawning](<../Mechanics/10-03 Item Spawning.md>)

# Maybe?
- [ ] Only show active spells
- [ ] Tutorial subsystem? + UI + Save Integration


# v0.5.1
- [ ] UI Soft