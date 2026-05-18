# 05-11 Meeting Notes

Development has slowed to a crawl. I was hoping to be done with the game by the end of May. If things keep moving at the same rate they have been, the game will never be finished. So, we have to make a couple changes.

## Unfinished Features

This is a list of the main features in the game that still need serious work before being considered complete. It contains:
- A brief overview of the feature
- The current progress on the feature
- The remaining work that needs to be done for the feature
- Possible pivots to consider if the remaining work seems too daunting or not worth the effort

### Questions the Start of the Game

At the beginning of the game, there is a [**Tome Altar**](<../Avernoth/Mechanics/Tome Altar.md>). When the player interacts with it, they are given a quick, randomized questionnaire. The answers to these questions determine:
- The player's primary spell
- The player's secondary spell
- (Possibly) Some starting [Addendums (Passive Abilities)](<../Avernoth/Mechanics/Addendums.md>)
- The player's starting stats

#### Completed Work

- the mechanic works. We can determine spells and stats and everything through the questions.

#### Incomplete Work

- We still have just one test question. WE NEED MORE.
- In order for this mechanic to feel meaningful, we need to have a good variety of questions that can lead to different combinations of spells and stats.
	- We need to create more questions and make sure they lead to interesting combinations.
- We do also need a good variety of spells and abilities to make this mechanic feel meaningful.
- Related UI specifically for this mechanic.

#### Possible Pivot

Hypothetically, we can completely throw away the whole idea of the questionnaire. Instead, we can have the altar just give the player a random combination of spells and stats without any input from the player.
- This would be much easier to implement, but it would also make the game feel less personalized and less engaging at the beginning of the game.
- It *does* keep the roguelike aspect of the game's beginning, but it does eliminate the fun of having at least some choice in the player's starting setup.

### Normal Levels

#### Completed Work

- Area 1 is is pretty much complete.
- Boss room 1 is complete

#### Incomplete Work

<https://docs.google.com/spreadsheets/d/1vxJl3exbdb2liDQKJrhAyyD7ETsiEauVnJ0WTo2rO4s/edit?usp=sharing>

- Area01_Room05 isn't done yet I don't think
- 3 of Area02 Levels are not done yet
- Area02 boss isn't done yet.
- We only have like 1 or 2 levels done for area03
- Area03 boss room isn't even close to being done.

#### Possible Pivot

A big problem with the later (Area03) levels is that it's kinda difficult to come up with new room designs. Also, it's difficult to create new room types without blowing up the prop list. We also can't expect too many new props / textures either.

So, here's what we can try:
- Lower the number of rooms per area. I wanted 8 per area, but maybe that isn't gonna happen… We can do like 6 or 7 instead per area.
- Move a level from Area01 to Area02 or Area03 (and re-skin it to fit the area's theme)
- Re-use some of the existing rooms as templates for new rooms. This way, we can create new rooms without having to come up with completely new designs from scratch.

### Boss Levels & Boss Fights

At the end of each area is a "boss room". These are supposed to be more unique and interesting than the normal levels.

#### Completed Work

- Area01's boss room is complete

#### Incomplete Work

- Area01's boss (the big knight with two swords) is not done behavior-wise
- Area02's boss room is not done.
- Also, we have no boss for Area02.
- Area03's boss room is not done
- Also, we have no boss for Area03.

#### Possible Pivot

Even though we have a "boss" for Area01, it is completely underwhelming. Also, the chance of us getting new BOSS designs for the other areas is VERY LOW.

So, here's what we can try:
- The enemy designs can literally just be modified, bigger, versions of the existing enemy assets.
	- Area01 - Big knight
	- Area02 - Big wraith
	- Area03 - Big summoner
- Instead of a straight-up fight against a bigger, badder enemy, we should lean more into the mechanics of the boss fights. For instance, a boss could be invulnerable and send out attacks UNTIL they are exposed, and then the player has a small window to attack them before they go back to being invulnerable again. This way, we can create more interesting boss fights without having to create completely new enemy designs.

Destiny as a reference

### Enemies

The game is supposed to have a variety of enemies and enemy combinations to keep combat interesting…

#### Completed Work

- Knight variations complete
- Wraith variations complete

#### Incomplete Work

- Enemies don't feel too different from area to area. The game doesn't scale well in terms of difficulty and variety as you go further into the run.
- Knight variation looks can be updated just a little bit
- Wraith variation looks can also be updated quite a bit
- Summoner enemy (that Erin is working on) is still being worked on, but is close to completion
- The enemy that Azalee was working on probably won't be finished anytime soon…

#### Possible Pivot

- We *could* have Andre work on finishing the model Azalee started. That way, we at least have another enemy in the game.
- To increase enemy variety and combat dynamics a little more, we can have variations of the summoner that buff / heal other enemies.
	- For instance, the "buffer" enemy temporarily increase the defense of specific enemies, almost making them invulnerable until the effect wears off / the "buffer" dies.

### Narrative & Dialogue

Avernoth is supposed to be a story-rich experience in which the characters frequently interact with the player. Dialogue is supposed to accompany most of the game's features to make the game's world feel a little more lived-in.

#### Completed Work

- The code for playing dialogue is pretty much done.
- The dialogue UI is pretty much done.

#### Incomplete Work

- Only 2 / 6 character portraits are done.
- Most of the game's dialogue is placeholder or just not implemented at all. We need to write and implement the actual dialogue for the game.

#### Possible Pivots

- Less dialogue?

### Overarching Progress / Completing the Game

Over the course of multiple runs, collect journal entries. Some journal entries contain experiment logs, which are interactive quests that the player must complete to progress. Collect all entries and complete all logs to fully understand the story and escape Avernoth.

#### Completed Work

- Journal & quest system works
- Some minigames have been implemented for the quests

#### Incomplete Work

- Still need some more minigame variety
- Still need the accompanying quests for each minigame
- All quest entries still need to be written.
- UI for the minigames

- Mechanic for determining which end room you go into is not done
- End rooms not done visually
- End rooms are not done mechanically
- No code implemented for when the player actually manages to collect all journal entries

#### Possible Pivots

- Reduce the number of journal entries required to beat the game.
	- Less quests to come up with / program
	- Less dialogue to write and implement

## Plans Going Forward?

At this point, it seems a little unrealistic to deliver the product I originally planned to deliver within a reasonable time. Therefore, I think it would be best to **re-evaluate the scope of the project** and figure out what the most important features are that we want to have in the game. Some things need to be reduced / cut so that the core elements of the game can shine more.

We are trying to get the game's core elements complete by the end of May / Early June for a release in Early July.
