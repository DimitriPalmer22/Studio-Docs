# 07-14 Meeting Notes

### Meeting Times
- Narrative Designer + CD Meeting
	- Friday @ 11 am
- 2D Artist + Narrative Designer Meeting
	- Sunday @ 11 am
- Environmental Artist Meeting
	- Possibly After 2 on Wednesday???
	- Possibly Friday @ 4???
	- NOT Saturday @ night???
- LD Meeting
	- Wednesday @ 8pm
- Sound Meeting
	- 3pm on Friday
- Character Artist Meeting
	- 6pm Thursday
- Animator
	- TBD

### Playing the Game in the Meeting
- If you want to play the game with the closest experience the player will have, open the the `MainMenuConcept` level and play from there.

- Main menu
	- Brian sent a video a couple days ago
	- I threw in the most recent track from the music channel in there just because it's music from us and not some royalty-free stuff
	- Any comments about how you guys feel about it?
- We load into a hub level. Again, this is a placeholder level for now. It will be removed.
- Then, we load into the ACTUAL starting level.
	- I decorated it a little bit with real assets and lighting just to remove that placeholder feel.
	- Real quick, I dropped some of the sketches of the characters as placeholders for the portraits. Right now, they're all cropped unevenly, so they are scaled a little weird.
	- Also, I changed the fonts for the dialogue
- Then, we load into the rest of the gameplay loop.
	- Enemy AI is now partially functional
		- The enemies move toward the player and occasionally strafe, but they're a little DUMB
		- They do a ranged attack once the player is near enough
		- I'm still researching the high-level stuff that makes them more intelligent
		- Also, I'm looking to add more attacks for them in-general
	- Trail VFX!
		- Mikel made a whole bunch of different trail VFX.
		- Only the fire VFX trail is functional right now though because reasons, but they'll be working eventually
		- How do u guys feel about it?
	- Dodge
		- I added a little visual feedback to the dodge mechanic: the screen shakes.
		- We PLAN for the dodge animation to be more dynamic, it'll change based on the direction you're going in. Andre already made the animations, we just have to put them on the player and make them work.

### In-meeting Notes & Feedback

#### Main Menu

- Replace the Avernoth title thing with a LOGO and not placeholder font
- Each option of the main menu can be on a different camera view as well.
	- Think of the menu Naruto Storm games or Dragon Ball Sparking Zero
- For another idea, the different pages of the book on the desk could correspond to the different options of the main menu

#### VFX

- Stretching is visible for the fire trail
	- Ball or cone for the fire power w/ trail behind it
- For the trails in general, the stretching is visible, so it doesn't really matter what the trail is supposed to represent
- Context of the spell really matters with selling visual effect

#### Enemies

- Lower the lock-on point for the enemies
- Enemy attacking, stopping, and relocating
- Prevent enemies from getting stuck together
- Allow the enemies to keep moving while the player is within the enemy's attack range
- First, we might wanna iron out the new idea for the player's attacking mechanics before we do the enemy AI stuff

#### Dodge

- Dodge screen shake
	- Screen shaking feels negative, so we should move it to when the player takes damage
	- Add a trail like in Hades

#### The Great Debate: What Should the Insignia Be?

![](<../../../_Meta/Attachments/Pasted image 20250714230857.png>)

- We needed to choose an insignia for the Musarun Empire
- Ay, me personally, I like 1
- The team voted 3, though