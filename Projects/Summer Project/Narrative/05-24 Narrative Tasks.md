# 05-24 Narrative Tasks

## Production Recap

So, just as a recap for where the project currently is, we are trying to scale a couple of things down so the project can be completed in a reasonable time frame.

### Some Documents

[This Document (05-11 Meeting Notes)](<../Meeting Notes/05-11 Meeting Notes.md>) goes over a list of features in the game that are still incomplete and the possible pivots for those features.

[This Document (05-18 Meeting Notes)](<../Meeting Notes/05-18 Meeting Notes.md>) goes over plans for *some* of those features (although, this might not be entirely relevant to your work).

[This document (WIP)](<../Production/Pivots.md>) goes over the specific implementation details for each of the design pivots that we have discussed so far (again, at this point, the document might not be entirely relevant to your work).

### TL;DR (for Narrative Stuff)

We might need to scale down & redistribute the number of [Experiment Logs](<../Avernoth/Mechanics/Journal System.md#Experiment Log>) ([Click here for more](<../Meeting Notes/05-11 Meeting Notes.md#Overarching Progress / Completing the Game>))
- Each one of these requires a unique experiment that the player has to recreate, which is a lot of work to design and implement.
- Each minigame requires some type of UI element or something to indicate the player's progress in the experiment
- Each log also requires written text that matches the experiment.

The questions at the beginning of the game are getting scrapped ([Click here for more](<../Meeting Notes/05-11 Meeting Notes.md#Questions the Start of the Game>) or [Click here for even more](<../Production/Pivots.md#Tome Altar>)).
- The amount of content we have in the game doesn't really justify this
- We don't have enough of them implemented at this point to really get a feel for how we want them to be (not just style-wise, but how they affect gameplay).

In terms of the game's general dialogue, we might need to reduce the amount of non-essential dialogue in the game ([Click here for more](<../Meeting Notes/05-11 Meeting Notes.md#Narrative & Dialogue>))
- A lot of the dialogue in the game is meant to add flavor and make the world feel more lived-in, but it doesn't really add much to the core gameplay experience. So, we might need to cut down on some of the non-essential dialogue to free up time for other things.

Boss fights are going to be a thing ([Click here to read more](<../Meeting Notes/05-11 Meeting Notes.md#Boss Levels & Boss Fights>)).
- Our "boss rooms" are very lackluster
- Rather than get unique enemy assets for these rooms, we can lean harder into having unique mechanics / objectives for the boss rooms
- These *are* going to need at least a little dialogue from the characters.

## Task

I'm still feeling out how many logs each chapter should have and what they should be. So, in the meantime, you can work on this.

Write / implement the following text for ***TWO*** experiment logs:
- The text of the experiment log itself.
- (If necessary) Text for immediately after the player picks up the log.
- Text for after the player completes the experiment log's quest.

Experiment Log 1:
- Note: This *is* the first experiment log in the game.
- Find an unused tome somewhere and channel the energy from it. (Spam E minigame).
- After picking up this log, this *unused tome* can be found on any of the journal tables in the game.
- When the player interacts with the tome, they will have to spam the E key to channel the energy from the tome into themselves.
- I *do* have placeholder text for after the player picks up the log, but it can be rewritten if you think of something better.

Experiment Log 2:
- 
