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

## Combat

### Juice
- Chromatic aberration effect whenever you use your secondary. Makes it feel more powerful.
- The trails on Allister's hands are now linked to the current number of hits he has in his combo. The more hits, the longer the trails.
- Chromatic Aberration + vignette

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