# 07-21 Meeting Notes

### Meeting Times

> I am unavailable most of Saturday. I am moving back home, and don't really know when I'm getting back. I'll most likely be available after 8 pm, though.

| Meeting                                   | Possible Times                                                                                                                                            |
| ----------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Sound Meeting (FMOD implementation + SDD) | Tuesday @ 11 am                                                                                                                                           |
| Creative meeting w/ Matthew & Andre       | Tuesday @ 2 pm                                                                                                                                            |
| Environmental Artist Meeting              | Wednesday @ 9pm                                                                                                                                           |
| Narrative Designer + CD Meeting           | Thursday @ 11 am                                                                                                                                          |
| Character Artist Meeting                  | Thursday @ 2pm                                                                                                                                            |
| Daunte Orientation                        | Thursday @ 5pm                                                                                                                                            |
| Erin + Austin Orientation                 | Friday @ 1pm                                                                                                                                              |
| 2D Artist + Narrative Designer Meeting    | Sunday @ 11 am                                                                                                                                            |
| LD Meeting                                | Probably any weekday @ 8pm, but I'll ask Mikel for when he's available first. <br>Also, Leo doesn't come back from PR till like the 24th or something so… |
| Animation Meeting                         | ???                                                                                                                                                       |

### Vertical Slice / Presenting the Game

A couple weeks ago, I mentioned that the goal of the next couple weeks of work were aimed toward creating a "vertical slice" of the game: a small polished section of gameplay that showcases the game's mechanics, art style, and overall feel.

!!! *I want us to show the game off in the Shbeeb alumni Discord server once we hit this milestone.* !!!

We can keep our peers up to date w/ what we've been up to over the summer, and we can also get some outside feedback on the game.

- ***The date for this is Sunday, August 3rd***. If anyone is uncomfortable with this date, or thinks we need to push it back, please let me know.
- This date might seem a little soon, but I want most of the group to focus on polishing the content that is already in the game, rather than adding new content.

### Things that Need to Be Polished for VS

#### Designers
- Find placeholder assets for any 2D / UI art that is not in the game currently
	- In-game UI
	- Dialogue boxes for dialogue screen
	- Tome creation screen
	- Power Icons
		- Fireball icon 1
		- Fireball icon 2
		- Crystal Barrage icon
- Make / find placeholder textures & materials for any untextured assets that are currently in the game.
	- In the event that any of the ACTUAL textures are not done, these should look good enough to be presentable.
- Make sure the visuals of all levels in the game are visually consistent
	- Crystal blueprints
	- Particle effects
	- Lighting

#### Sound
- Footstep sounds
- Every spell currently in the game should have some type of sound(s) for it firing
	- These could be made in-house OR they could be royalty-free sounds we find online and can use as placeholders
- The dialogue sounds (like the scribbling sounds)
- UI Sounds

#### 2D Art
- Character portraits
	- It'd be pretty fire if we had at least one pretty complete character portrait by the deadline
	- The rest can be pretty rough / unfinished

#### Environmental Artists
- There was a priority list of textures was sent out a while ago. Try to get as many of those done as possible.

#### Character Artists
- Allister model done
- Allister textures done
- Minotaur model done
- Minotaur textures done

#### Programming Stuff
- Any feature that is in the GDD, but is NOT in the game currently needs to be added

#### VFX
- Make sure all the trail VFX work like the fire trail VFX
- Impact VFX for when the spells hit
- Some type of magic poof VFX for when the enemies die
- Some particles that get drawn toward the player when they get money

#### Enemies
- Enemy attack animations
- Enemy AI refinement

### Play the Game in the Meeting

#### Changes Since the Last Meeting

##### Main Menu
- Brian updated the main menu concept to have a book that opens and flips pages
- He also changed the main menu fonts

##### Tome Creation & Tome Upgrades
- After the first dialogue interaction in the starting room, the player is greeted by the tome creation screen
	- The tome creation screen is very ugly right now, but it is mostly functional
	- The tome creation screen was created in accordance with the GDD, so you should be able to read that to clearly understand what is going on.
	- Each question type is functional EXCEPT the passive ability question (since there aren't any in the game yet).
- At some point during their run, the player encounters the upgrade room
	- I threw in the upgrade room Mikel made a couple weeks ago (and redid the lighting real quick)
	- Functionally, the upgrade room should be almost complete.
		- The dialogue interaction works
		- The upgrade screen appears, although two of the four upgrade types on the GDD are not done yet.
	- The upgrade screen is also very ugly right now, but it is functional.

##### Spells
- Spells can now be set to follow specific points (sockets) on the player, rather than just the player mesh.
	- For example, the fireball spell now follows the player's hand.
- For testing out different animation types for the spells, I threw in a "punch" spell using Mixamo animations real quick
	- It's basically the fireball spell, but it shoots out a fireball as the player punches

##### VFX
If you guys have been keeping up with the team-designer channel, you've most likely seen these already.
- The crystals now have an ambient twinkle VFX around them
	- These are the cyan twinkles that appear specifically around the crystals
	- This is placed on the crystal blueprint, so you don't have to manually place the VFX in the level
- The rooms in general also have ambient magical twinkles that fill the environment
	- These are the white twinkles that are scattered around the level
- The fireball & fire trail VFX have been reworked to be more fire-y
- Last week, I had the screen shaking whenever the player dodged. I removed that and transferred the screen shake to whenever the player gets damaged instead.

##### In-Game HUD
- Last week, I also had Brian create a basic blockout for the in-game HUD.
- It has:
	- Health bar (functional)
	- Mana bar (functional)
	- Area for the player's mana essence (functional, but is purely text for right now)
	- Area for counting the number of keys the player has (NOT functional)
	- A section for the player's passive spells (NOT functional)
	- A section for the player's primary and secondary spells (mostly functional)
		- Depending on the spells the player has equipped, these icons change

##### Animation Things
- Andre made it so Allister's cloak has cloth physics
	- The clipping is a known issue, and we're having Azalee go back and increase the number of polygons in the cloak to reduce the clipping issues
	- She'll also increase the polygon count for the scarf as well so that it has cloth physics too

##### Journal
- Made a simple layout for the journal (that will be revised)
	- Check Chelle's thread for the doc about that if you're interested
	- [Here's the link for convinience](<../Narrative/07-17 First Journal Entry Task.md>)
	- Side note: Chelle and I also briefly talked about this in our meeting on 07-17. I added those notes to the end of the previously mentioned document as well.

##### Other Small Changes
- Camera fades in an out when going between rooms (during which the player can't move)
- While the player is locked on to an enemy, the reticle in the center of the screen disappears
- The lock-on point for the enemies has been raised to chest height

#### Feedback from the Team Looking at the Game

> These are things the group comments on as I play the game on-stream.

- Less floppiness / movement in Allister's cloak when its done
	- Also don't make the cloak go up his butt
- Put in the footstep noise
- Put noises in the game in general
- Put the actual character portraits
- Character portrait background
- Upgrade menu
- Flinch effect / stun effect on the enemies when they're hit
- refine the enemy AI some more
- tie the enemy attack animations the sockets
- better animations for the enemy attacks
- More crystal blueprints cuz we're just using the same one over and over
- Decals in the level EVERYWHERE
- Put in a placeholder for the ending room similar to the starting room. That way its not a green box
### Things for This Week

> This is not a comprehensive list of tasks for EVERYONE.

#### Programmer
- Dialogue portal transition
	- Whenever the player enters a dialogue interaction, the camera goes to a new environment that looks like it is INSIDE the dialogue portal
- Spell animation combo system
	- Some spells allow the player to repeatedly use them and get a string of animations as opposed to just the one animation
- More enemy AI revision
	- More aggressive enemy AI
	- Dodge functionality

#### Animation
- Omnidirectional Dodge (w/ programmer)
- More attack animations
- Flinch

#### Narrative Designer
- First, ask about the progress on the journal entry task Chelle and I talked about
- 2 journal entries + revised dialogue that ISN'T racist to French ppl

#### UI (Brian)
- Pretty up the tome creation screen's UI
	- Establish a solid layout
	- Give a rough idea of what each UI element is supposed to look like (have it fit with the book theme)
- Pretty up the upgrade screen's UI
	- Establish a solid layout
	- Give a rough idea of what each UI element is supposed to look like (have it fit with the book theme)

#### Character Artists
- Allister model progress
- Work on enemy models

#### Small Polish Things (that May or May not Get Done immediately)
- Throw on the spell SFX onto the crystal spell
- Invincibility flash after getting hit
- Invincibility conveyance while the player is dodging
- FOV change while dodging
