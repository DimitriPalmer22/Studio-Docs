> These playthroughs are meant to guide further development. We analyze real gameplay to determine which features need to be worked on still.

# 11/02/26

## Does This Satisfy The Target Experience

### Rogue-lite Features

### Combat

- Enemy spawns are too far apart in many rooms. There are portions of combat where the player has to chase down an enemy to continue the flow of combat.
- Wraiths need to move…

### Story

## Which Features Are Still Lacking

### Audio

- Music too low
- Non-music audio should fade when going from one room to the next

#### Player Combat

Dodge
- No dodge sound
- Perfect dodge sound is missing

Shield
- Need: Shield activation sound
- Need: Shield success sound

Flame volley
- Needs a sound for hitting enemies
- Fire sound is kind of terrible

Crystal Explosion
- Charge finished sound(?) is ear piercing

Secondaries
- Charge start sound
- Charge finish (successful) sound
- Charge finish (fail) sound

#### Environmental

Room portal open sound
- Need a separate sound for finishing the last enemy in a room
- Does not fit the theme (should be more portal-y)
- Too loud
- Should not play in starting room

Room portal remains open sound
- Room clear portal sound does not stop playing when going to the next room?

Room portal interact sound
- Sound not synced to when Allister is going to the next room. (use event in animation?)

Dialogue
- Typing sound too loud
- No confirmation sound for text
- Dialogue portal start sound too loud

Orbs
- Orbs need a collection sound

#### Enemies

Tempest Wraith
- Lightning strike needs a sound

### Where Can Combat Improve

## Is there Any Feature that is Visibly Unfinished?

### Journal / Codex

## Key Takeaways

### I May Need to Rethink The Enemy Wave System as a Whole

- The placement of the ranged enemies often interrupts combat in a way that is not fun. Yes, they force the player to move, but they are also so out-of-the-way that they are annoying to fight.

### Audio Needs to Be a Real Priority

- The game feels most unfinished in the sound department.
- There are too many missing sounds.
- There are many sounds that just don't fit.
- The mixing needs to be addressed.

> Use the sound ledger that was created. Organize sounds by feature.

### The Dialogue System Could Use a Bit More Love

- Going back to the audio, some sounds are still missing.
- The content of the dialogue can be a bit… boring…
	- There is no real introduction to the game's greater plot and world, so everything seems ***irrelevant***.
- Character model is often awkwardly obstructed by textboxes during dialogue. We should frame the player differently during dialogue segments (Maybe a head-on view?)

### Player Combat

- In terms of the flame volley, the crystal explosion, and the default dodges, ***they feel nice***.
- The other attacks should be worked on to feel as impactful and satisfying.
- Again, sounds are missing.
- Some actions (perfectly dodging, shielding, etc.) can feel a bit ***more satisfying***.
- I can experiment a *bit* more with the camera (pull it up and away more?)
- Given the game's combat structure, it is difficult to attack the fire wraiths without taking damage yourself.
	- Instead of giving them a wall that cannot be touched for a duration, make their wall more of an instantaneous bit of damage that is safe immediately after the hitbox is enabled.
	- This would also free us up to allow the fire wraiths to move / even create variations that have different fire wall patterns.

### Levels Need to Be Cleaned Up A Bit

- The player can still be awkwardly caught on random geometry (crystals, books, etc.) in some rooms.
- Lighting bugs can still be found in some levels.
- Some props are awkwardly breaking up the play area.
	- Bookshelves that jut into the play area's walkable space
	- These allow the player to get stuck on them, and they also break up the flow of combat.

### UI Needs a Bit of Love

- The tome selection at the start requires a placeholder UI at least.

### GAME BREAKING BUGS

- Sometimes, the game refuses to load into the next level because `Error: URoomSubsystem::EnableNextRoom - Next room stream is null!`. Find a way to replicate this and prevent it from happening again.
