- [x] Finish the pull-in ability of the one tempest spell
- [ ] Different knight enemy variations (functionality)
	- [x] Twilight debuff
	- [x] Primordial burn
	- [x] Twilight mist
- [ ] Indication for status effects
	- [ ] Cues
- [ ] Functionality for at least 2 variations of the minotaur enemy
- [x] Setting up the layout of the new beginning of the game
- [x] Focus a little more on the elemental affinities of the enemies and your spells
- [ ] More powers for the player
	- [ ] Primordial Primary
	- [ ] Primordial Secondary
	- [ ] Tempest secondary
- [ ] Rework the passive spell UI
- [ ] Throw in a couple more passive spells
- [x] Potentially a new room type: A room for stat upgrades -> Ensure the player steadily improves over time (not just through the powers they have, but through the stats as well)

#  Avernoth Update v0.8.0

## Audio
- Started using Unreal's Metasounds for most of the game's audio
- New song thrown into the game
- Outside-of-battle music will fade into the in-battle music when combat starts
- NOTE: Instead of using completely separate tracks for in-battle and out-of-battle music, I plan to make calmer versions of the existing tracks to use as out-of-battle music.
- Replaced most of the existing sounds with new, royalty-free sounds
- As of right now, most of the game's audio is unmixed, so some things might be way louder than they need to be!
- Some sounds are just placeholders for now, as they either don't fit the game's aesthetic or are too loud/annoying.
- Some actions still need sound effects added to them.
- The "talking" sound effect for the characters has been replaced with sounds of scribbling.
- Footstep sfx

## Beginning Room + Dialogue

- The beginning of the game has been reworked to be a little more engaging & support the narrative better.
- The room is a *very rough blockout* for now.
- Some of the dialogue portions can probably be removed for the sake of keeping the beginning sequence short.

### Sequence
1. The player's screen is all-black, but a character speaks to Allister as he wakes up.
2. The screen fades from black, we see a dialogue portal. Allister goes up to it, and talks to it to get some more dialogue.
3. After that, Allister exits the current room and enters the next one: the "questions room"
4. Once entering the "questions room", Allister is then presented with a little more dialogue.
5. After that, Allister then walks up to one of the 3 objects in the room that give him a question. However, as he walks up to one of the objects, he is given more dialogue explaining what these objects do.
6. Allister answers all 3 questions.
7. Once he answers all 3 questions, he is then given some more dialogue.
8. Allister walks to the room's exit portal. As he approaches the portal, he is given some more dialogue.
9. Allister then exits the room.
## Combat

### Juice
- Chromatic aberration effect + slight FOV zoom out whenever you use your secondary. Makes secondaries feel more powerful.
- The trails on Allister's hands are now linked to the current number of hits he has in his combo. The more hits, the longer the trails.
- Chromatic Aberration + vignette + more time slow when doing a perfect dodge. It should be easier to tell when you perform one.

### Input
- Separated the targeting scheme when using a mouse vs. controller. The game should feel much more responsive now when using keyboard and mouse.
- When using a mouse, they game will target the enemy closest to the center of the screen. 
- When using a controller, the game will target the enemy closest in the direction the player is moving in.

### Moving Towards Enemies while Attacking is Input-Based
- Before, the player would move towards enemies automatically when attacking them.
- However, I have changed it so that the player has to be holding down the movement input in the direction of the enemy in order to move towards them while attacking.
- So, if you're attacking and not holding down any movement input, the player will pretty much stay in place while attacking.
- This should give the player more control over their movement while attacking.

### Balancing
- Primary attacks are even weaker now, to encourage the player to use their secondary attacks more often.
- Secondary attacks are slightly stronger now.
- It takes a little longer to charge the mana meter
- Perfect dodge detection should be much better for melee attacks

## Interact Animation
- A quick placeholder animation plays whenever the player interacts with something in the world (like a journal table).

## Levels
- The game's rotation of levels has been updated.
- The game has 3 areas in it, and each area now has its own set of levels that can spawn.
- However, levels that DO NOT WORK have been disabled and removed from the rotation for now.