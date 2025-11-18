
## Meeting Times

| Meeting                         | Possible Times      |
| ------------------------------- | ------------------- |
| LD Meeting                      | Tuesday @ 8pm       |
| Narrative Designer + CD Meeting | Tuesday @ some time |
| Sound Meeting                   | -                   |
| Environmental Artist Meeting    | Saturday @ 3pm      |
| 2D Artist                       | Sunday @ 3pm        |
| Animation Meeting               | -                   |
| Character Artist Meeting        | -                   |

## Current State of the Game / v0.11.0 Changes

Instead of focusing on the stuff I wrote down last week, I pivoted to working purely on narrative stuff this week (and some other small stuff).

### Tutorial
I started working on a tutorial sequence for the game.
The very first time the player starts a run, they'll get a scripted tutorial that teaches them the basic mechanics of combat.

### MASSIVE Journal Table Rework
The game's journal system has been overhauled. Collecting journal entries is less incidental and now requires a little more effort on behalf of the player.

BEFORE, the player would randomly encounter journal tables while exploring Avernoth. The journal tables were the main thing linked to the player's progression, but it never really felt like the player was actively working toward unlocking or discovering the journal entries. They just showed up fr.

NOW, each journal entry has an "objective" that must be completed in order to unlock the next journal entry and progress through the game. This way, we can ensure:
- the player experiences a variety of content in the game
- the player is actively working toward the main goal of the game

*Do a little demonstration*

### Questions @ the start of the Run Are Still Under Construction...
Since the main way to get spells is through the questions at the beginning, I am waiting until the journal stuff is finished before fully implementing the questions at the start of the run.

### Small Dialogue FX Tweaks
Whenever you start dialogue, there is a small chromatic aberration effect that plays.

### Passive Spell UI Rework

For a while, we just had 3 passive spell icons floating at the side of the screen permanently. This was a problem because:
- It didn't look very good
- It was hard to tell which passive effects were activating and when

Now, we have a bookmark / ribbon-style UI element in the top left corner. As passive spells activate their effects, they appear on the ribbon for a few seconds, then go away. This way, the player can easily see which passive effects are activating and when, without cluttering up the screen.

The asset for the bookmark / ribbon thing is still being worked on, so that may look different in the near-future.

### Updated Set-Dressing
The environmental artists have sent some props for set-dressing and the LDs have set-dressed some of their levels.

## Goals for v0.12.0:

### More Narrative Stuff
Hopefully, all progression-based goals in the game are fully implemented, meaning the game can be fully completed from start to finish.

Dialogue should also be more complete by then.

More question stuff as well.

### Level Design
We'll go over all the existing levels in the game and make sure they are all working and properly set-dressed so that they can be put into the game.