# 06-22 Meeting Notes

# Remaining Features Being Worked On

## Levels

### Standard Levels

We want **AT LEAST** 8 rooms per area of the game (so **AT LEAST** 24 standard rooms total).
So far, we have
- [x] 9 FINISHED Rooms in area 01
- [ ] 4 FINISHED Rooms in area 02, 4 unfinished
- [ ] 1 FINISHED Rooms in area 03, 2 unfinished

Since it's a lot of work to create fully new levels, the plan was to either:
- move rooms from other areas into the area that needs more rooms
- create a new room by modifying an existing room.

### Boss Room For Area 01

Boss fight is being worked on, but still needs:
- Placed "fountains" for the boss fight
- Proper waves set up for the minor enemies
- Some unique animations for the boss fight

### Boss Room For Area 02

- Boss arena still being worked on
- No mechanics have been implemented at all for this.

### Boss Room For Area 03

Boss fight is being worked on, but still needs:
- A proper boss fight arena
- The summoner enemy asset
- Minor enemy waves properly set up

### End Rooms

Layouts for all 3 are pretty much done.
We just need to get the mechanics for those going.

## Narrative

### Standard Journal Entries

Of the 18(?) standard entries we want to have in the game, only 7 are done. Here's a link to the ones that have been written thus far: <https://docs.google.com/document/d/1fPXqUteASUqkibwUp5ObOOwUCh2P4IH8DkB1fv_49i0/edit?usp=sharing>

Just as a reminder, the player needs to collect these to progress through each chapter of the game.

### Experiment Logs

Of the 12(?) experiment logs we want to have in the game, only two have been written. Here's a link to a google spreadsheet to keep track of the experiment logs that have been written, and the ones that still need to be written (it's under the quests tab): <https://docs.google.com/spreadsheets/d/1pjRz5dA8ngFP_Ry3ltzbb2U_9H8KCBFXYC4ikuIb2-Q/edit?usp=sharing>

## Enemies

### Knight Enemy Variations

Daunte has created several variations of the knight enemies so they are more visually interesting, but we have yet to implement them.

### Summoner Enemy

The animators have been working on rigging the summoner enemy, but we still need:
- textures
- animations

#### Summoner Textures

- Default summoner texture
- Texture (recolor) for the "buffer" variant of the summoner
- Texture (recolor) for the boss variant

#### Summoner Animations

At least 3 animations for using an ability.
- The base summoner enemy will use one of these
- The "buffer" enemy variant will also use one of these
- The boss (which has 3 abilities it uses) will use the above two in addition with another one

### Enemy Distributions

Enemies still need to be properly distributed throughout the levels now that we have a new enemy type.
