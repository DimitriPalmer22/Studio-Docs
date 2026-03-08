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

Right now, we can control