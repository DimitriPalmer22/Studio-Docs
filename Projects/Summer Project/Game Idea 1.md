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
	- If you want to significantly change / upgrade your tome, you have to find a new one.

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
- Each use of these spells should feel grand and powerful (using VFX and sound design to make them feel impactful).

##### Transformation (OPTIONAL)
- Some tomes have a transformation ability.
- These are not a literal change in form, but more a temporary augment to the player's abilities / stats.
- For example:
	- Tome A gives the player a bright blue aura that increases their damage by 50% for 10 seconds.
- Instead of being time-based cooldowns, these have meters that fill up based on the player's actions. They also deplete partially if the player plays poorly.
	- For example:
		- Tome A's meter fills up when the player hits enemies with their primary spell.
		- Tome B's meter fills up when the player dodges enemy attacks.

##### Passive Abilities
- Each tome has a number of passive ability slots
- Some tomes come with most / all of these slots pre-filled, but some slots may remain empty so the player can acquire more throughout their run.
- These passive abilities can be anything from stat boosts to effects that trigger under specific circumstances.

#### Progressing Through the Run / Getting Stronger
- After completing a floor, the player has to answer another question. Depending on their response, they get a different set of random base-stat boosts.
- At the end of each floor, the player has a couple options. They can choose to:
	- *Relinquish* (name pending)
		- Thematically, tomes can't really change unless you give something up. Generally, there is a ceiling to how strong a tome can be.
		- The player can choose to:
			- sacrifice one of their passive abilities
			- sacrifice one of their ultimate spell
			- sacrifice their transformation spell
			- purposely decrease one of their tome's stats
		- As a result, this increases the player's base stats.
			- Depending on what you sacrifice, the player will get a different amount of base stats.
		- This way, the player can keep their current tome and still get stronger if they really like it.
		- Also, once the player does decide to change tomes, they still retain the stats they gained from relinquishing their tome.
	- *Overwrite* (name pending)
		- Thematically / lore-wise, you are replacing a page in your tome with a new one, allowing you to change your tome. However, you need some sort of special item (which breaks upon use) to do this.
		- Increase the stats of the tome overall.
		- One of the spells of the tome (of the ones it currently has) gets replaced with a new spell (that is usually more powerful)
	- *Empower* (name pending)
		- This option is only available if the player does well for this floor / completes this floor quickly
		- Thematically, a special person who is very good at magic comes and empowers the player's tome. However, they are being chased by something, so they leave the floor after enough time has passed.
		- Special shop that allows the player to buy a new spell / ability for their tome.
		- Can also buy special upgrades for their tome.
		- No sacrifice btw.
		- Use currency to determine how powerful the new spell is
### Starting a Run
- Every time you start a run, you are given a series of random questions from a very LARGE pool of possible questions (Use data assets or something for this)
	- These questions have a LARGE list of possible responses
	- Each response does something random (well, not entirely random. The response will have a general mood, and based on that mood, the effect will be different)
	- This serves as our initial character building, which we go into the rest of the run with.
	- Note: The player's answers to the questions will be stored in a page at the front / back of the ***Tome*** for the duration of the run.
	- **IDEA**: For long-term progression, we can unlock more questions at the start of our runs AND a wider selection of questions / responses.
		- For example, when booting the game for the very first time, the player gets a sequence of 3 random questions from a list of like 10 total.
		- As we get further through the game and defeat more bosses, we unlock more questions to choose from / more answers to choose from / a longer sequence of questions.
		- The questions / responses you unlock are tied to in-game achievements.
		- The number of questions in the beginning sequence is tied to how far you've made it in your runs / how many times you made it very far.

### Incentive to Keep Going
- Given that some powers / abilities have time-based mechanics, there needs to be a way to prevent the player from waiting in safe spaces for the cooldowns to finish.
- *Idea*: Stop the timers while the rooms / areas are not active?
- *Idea*: Have a time-based incentive at the end of the floor
	- For example, the player has to defeat a boss at the end of the floor within a certain time limit.
	- If they don't, they get a penalty (maybe a curse or something)
- *Idea*: Have a curse that makes the player take damage if they stay in a room for too long.
- *Idea*: Like Persona's Reaper, spawn a strong enemy if the player stays in an empty room for too long.
	- This enemy is a very powerful mini-boss that can only be defeated with late-game stats and abilities.

### Structure of the Game

#### What is an "Area"?
- ***Areas*** are like the floors in a roguelike. They are themed areas that the player must traverse to reach the final boss.
	- Think the floors in *Hades*, *Enter the Gungeon*, *The Binding of Isaac*, etc.
- Each area is broken up into a series of "rooms". Each room is a small space that contains a series of enemies, traps, and other obstacles.
	- The player must defeat all the enemies in a room to progress to the next room.
	- Rooms can also contain treasure chests, shops, and other points of interest.
- Generally, no area's layout is predefined. Instead, the areas are procedurally generated.
	- This means that the areas are randomly generated each time the player plays the game.
	- This allows for a high degree of replayability and keeps the game fresh and exciting.
- The individual rooms are pre-defined, but the order in which the player encounters them is random.
	- Much like the rooms in *Enter the Gungeon*, the rooms are randomly chosen from a pool of rooms.
- Each area has a specific theme, which is reflected in the enemies, traps, and other obstacles the player encounters.
	- For example, one area might be themed around fire, while another might be themed around ice.
	- The enemies in each area will also reflect this theme.

#### Level Design Methodology
- The game is designed to be procedurally generated, but the individual rooms are pre-defined.
- This means that there are a series of rooms that are designed to be used in the game, but the order in which they are encountered is random.
- As a result, there does not need to be much continuity between the rooms.
	- What I mean is, the rooms do not need to be designed to flow into each other using the same assets.
	- In fact, we can play into the rooms not making much sense together because of some magical reason.
- The rooms can be designed to be completely different from each other, as long as they are fun to play in and look good.
- Also, given our wide range of level designers, we can have a wide range of styles and themes for the rooms.
- Also, given with our lack of artists, we can focus on getting a wide range of small and simple props. We'll use those to set-dress the rooms and make them feel distinct.
	- Try to stay away from having large props that take a long time to make and only appear in one or two rooms.
- First and foremost, the rooms NEED to facilitate combat.
	- The rooms need to be designed to allow for the player to move around freely and dodge enemy attacks.
	- The player should rarely ever feel like the room is too small or cramped due to props or architecture getting in the way.
- ROOMS THAT ARE NOT USED FOR COMBAT (like shops) ARE ALLOWED TO BE SMALLER / MORE DENSE WITH PROPS
	- The player should feel like they are in a safe space when they enter these rooms.
	- The player should not feel like they are in danger of being attacked by enemies in these rooms.
	- These spaces should also be used to deliver some type of environmental storytelling
- Each level designer can work asynchronously on their rooms while regularly checking in with each other / the CD to make sure the rooms are cohesive and fit within the overall theme of the game.

#### Area 1
- Theme: Area with gray brick & magic crystals
#### Area 2
- Theme:
#### Area 3
- Theme:
#### Final Boss Area
- Boss area is the only predetermined area in the game.
- Instead of having a series of rooms the player must fight through, the final boss consists of a couple utility rooms and then the boss arena room.

## 1. Three Creative Pillars

| Pillar               | Core Question                                                        | Outcome                                                                                                                                                                                        |
| -------------------- | -------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Emotional Spine**  | What core feeling do we want players to experience every 10 minutes? | Every choice they make is important. <br><br>Choices lead to a sense of power (not overwhelming or underwhelming.).<br><br>The constant focus on combat gives the player a rush of adrenaline. |
| **Interactive Hook** | Which single mechanic will define the loop and reinforce the spine?  |                                                                                                                                                                                                |
| **Narrative Thread** | What story beat anchors player choice to world reaction?             |                                                                                                                                                                                                |
