# 03-08 Production Plan

## Carry-over Tasks from Last Week / Last Sprint

- LDs: De-square levels
- Erin: Finish texturing the writing desk
- Daunte: Finish pedestal model (texture)

- Get the new tome altar in the game.
- Get the writing desk proxy in the game.
- Place the new pedestal in the game.

- Update the existing UI

- Model & texture new enemy

## New Tasks

### Current Enemy Improvements

### Better Dialogue Incorporation

The dialogue has been neglected for the most part and is only every really updated for large milestones. At this rate, the dialogue and narrative are going to feel a lot more tacked-on than I would like.

#### Cleaner Implementation of Save Data

For testing purposes, (Dialogue-related) save data needs to be much more manageable. Right now, the only ways to manipulate save data are through actually playing the game or by using in-game commands. So, we should implement save data as data table rows.

- An "empty" save-data table row.
- Other table rows to represent different states of the game (like having certain bosses defeated, certain dialogue options chosen, etc.)

#### Have the Camera Face Allister During Dialogue

Our *framing* during dialogue is generally pretty bad. There is no intention behind what the character is looking at during dialogue, and it just feels kind of awkward. As of right now, there is no reason the dialogue can't just take up the entire screen.

Right now, during dialogue, we *can* control where the camera faces (e.g. facing toward an enemy during the combat tutorial). However, for the most part, the camera just faces forward during dialogue. It would be a lot better if we could have the camera face Allister during dialogue since he's the one doing most of the talking and is the main character of the game.

#### Journal System

The crux of the game's narrative is the meta-progression (the things that carry over between runs). In our case, the only implementation of this is the journal entries, which are collected by Allister and recorded by Tarun.

However, if we're just collecting the journal entries, then the player would have little reason to read anything. However, since the journal entries have objectives that the player needs to actively complete, the player is incentivized to read the journal entries and the dialogue surrounding them to know what they need to do to complete them.
