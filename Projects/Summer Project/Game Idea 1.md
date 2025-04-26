## 0. Jotting down Ideas

- Genre: Fantasy (Magic) Roguelike
- 3D
- 3rd Person, NOT top-down
- The game is supposed to feel like:
	- Difficulty: The player should never feel too powerful in relation to the enemies, even if they are having a really good run. Items / abilities should not carry the player's run. If anything, the player's skill should be the determining factor for how easy the game is.
		- Think Enter the Gungeon / Risk of Rain / *Hades*
	- Combat: Combat is fast-paced and skill-based. The player should feel like they need to frequently move and dodge to avoid enemy attacks. The combat should feel simple enough that the player can pick it up and play, but complex enough that they can learn new things and improve over time.
		- Think *Devil May Cry*
- Visual Style:
	- Stylized Cel-shaded visuals
		- shaded regions should be very very dark to give them a deep contrast to the bright colors of the cel-shaded regions. Maybe even use occlusion masks to give the illusion of depth in places that need it more.
		- For the most part, textures should be very simple. Mainly, they should be flat colors. Then, apply line work to give the illusion of depth and detail.

### Main Mechanics

#### The Tome
- A tome is a magical book that contains a collection of spells and abilities the player can use.
- A core idea I want for the game is that your tome is only so modifiable.
	- If you want to significantly change your tome, you have to find a new one.

##### Stats
- Separate from the player's stats, the tome has its own stats.
- These stats serve as percentage modifiers to the player's stats.
	- For example: +12% to spell damage, +5% to spell cooldown, etc.
- Having the tomes be a separate entity from the player allows us to have a more interesting progression system / makes it easier to randomize them and make them feel distinct.

##### Primary Spell
- Each tome comes with a primary spell.
- This is the main spell the player will be using to fight enemies.
- Should be able to be used with no cost / drawback.

##### Secondary Spell
- Each tome comes with a secondary spell.
- This is an additional spell the player will use in conjunction with the primary spell.
- These can be used at a much less regular interval than the primary spell since they are more powerful.

##### Ultimate Spell (OPTIONAL)
- Some tomes have an ultimate spell.
- These spells are very powerful, and can be used to get the player out of a pinch instantly.
- However, they recharge very slowly / have extreme recharge conditions. For example,
	- Spell A only recharges while under 30% health.
	- Spell B takes 5 minutes to recharge.
	- Spell C only starts to recharge after the player has not taken damage for X rooms.

##### Transformation (OPTIONAL)

##### Passive Abilities

### Starting a Run
- Every time you start a run, you are given a series of random questions from a very LARGE pool of possible questions (Use data assets or something for this)
	- These questions have a LARGE list of possible responses
	- Each response does something random (well, not entirely random. The response will have a general mood, and based on that mood, the effect will be different)
	- This serves as our initial character building, which we go into the rest of the run with.
	- Note: The player's answers to the questions will be stored in a page at the front / back of the ***Tome*** for the duration of the run.
	- **IDEA**: For long-term progrssion, we can unlock more questions at the start of our runs AND a wider selection of questions / responses.
		- For example, when booting the game for the very first time, the player gets a sequence of 3 random questions from a list of like 10 total.
		- As we get further through the game and defeat more bosses, we unlock more questions to choose from / more answers to choose from / a longer sequence of questions.
		- The questions / responses you unlock are tied to in-game achievements.
		- The number of questions in the beginning sequence is tied to how far you've made it in your runs / how many times you made it very far.

### Incentive to Keep Going
- Given that some powers / abilities have time-based mechanics, there needs to be a way to prevent the player from waiting in safe spaces for the cooldowns to finish.
- *Idea*: Stop the timers while the rooms / areas are not active?
- *Idea*: Have a timer that counts down to the next wave of enemies / next room.

## 1. Three Creative Pillars

| Pillar               | Core Question                                                        | Outcome                                                                                                                                                                                        |
| -------------------- | -------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Emotional Spine**  | What core feeling do we want players to experience every 10 minutes? | Every choice they make is important. <br><br>Choices lead to a sense of power (not overwhelming or underwhelming.).<br><br>The constant focus on combat gives the player a rush of adrenaline. |
| **Interactive Hook** | Which single mechanic will define the loop and reinforce the spine?  |                                                                                                                                                                                                |
| **Narrative Thread** | What story beat anchors player choice to world reaction?             |                                                                                                                                                                                                |
