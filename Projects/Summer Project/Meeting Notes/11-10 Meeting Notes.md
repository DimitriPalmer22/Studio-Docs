### Meeting Times

| Meeting                         | Possible Times |
| ------------------------------- | -------------- |
| LD Meeting                      | Tuesday @ 8pm  |
| Narrative Designer + CD Meeting | Tuesday @ 11am |
| Sound Meeting                   | -              |
| Environmental Artist Meeting    | Saturday @ 3pm |
| 2D Artist Meeting               | Sunday @ 3pm   |
| Animation Meeting               | -              |
| Character Artist Meeting        | -              |

## Current State of the Game / v0.10.0 Changes

v0.9.0 and v0.10.0 were both pretty small updates (partially due to time constraints and availability issues).

### Very Silly Lightning Bug Fixed 
- There was a bug where light wasn't being properly baked onto our props. This has been fixed.
- Literally, we just had to increase the lightmap resolution on the props because by default, Unreal sets it to 4 when it should be like 32 or 64 for most objects.

[The Fix is discussed a little more here.](<./11-08 Environmental Art Meeting Notes.md>) I've already gone over it with the environmental artists.

- With that squared away, the lighting in some levels has been updated.
- The post-processing has been tweaked very slightly.

### The Ending Room: The game loop is more complete now
- Before, there was no way to even get to the "ending room" of the game, as the final boss level was not fully set up.
- As of right now, the final boss level has 1 enemy wave set up, allowing you to complete the room and reach the ending room.
- In the ending room, you'll see a magically sealed door. 
- However, if you've collected each of the journal entries, the door will be unlocked and you'll be able to proceed to the ending sequence. 
- If you haven't collected all of the journal entries, the door will remain locked, a portal appears that'll bring you back to the start of the run.

### Back-end Save Data Stuff
- A couple of small, back-end changes were made to how save data is handled.
- At some point in the future, I'm gonna be implementing a feature where you'll be able to save your run progress, exit the game, and load back into where you left off.

### Save Data has been Enabled In-Player
- Before, every time you played the game, your progress would reset.
- So, you would see tutorials you've already seen, and you would have to recollect journal entries you've already collected.
- Now, your progress is saved between play sessions.
- If you ever want to reset your save data, open the console (during play mode) and type `Av.SaveGame.ClearPersistent`
- Then exit play mode and start a new play session.

### Armory Props
- We got a whole new set of armory props from the environmental artists.
- So, continue set-dressing

### Important Dialogue Laid Out
- Some of the dialogue in our game is *plot-significant*
- I have created all the assets required for most of this dialogue.
- So, you'll see dialogue prompts pop up with placeholder text.
- We're still working on getting the final dialogue written.

## Goals for v0.11.0: