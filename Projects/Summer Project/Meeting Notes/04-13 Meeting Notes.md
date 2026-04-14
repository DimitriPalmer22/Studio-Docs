# 04-13 Meeting Notes

## Meeting Times

| Meeting                         | Possible Times |
| ------------------------------- | -------------- |
| LD Meeting                      |                |
| Narrative Designer + CD Meeting |                |
| Sound Meeting                   |                |
| Environmental Artist Meeting    |                |
| 2D Artist                       |                |
| Animation Meeting               |                |
| Character Artist Meeting        |                |

## Updates To The Game

Not much of the work from last week's plans going forward have been completed.

## Plans Going Forward

### Enemy AI and Behavior Rework

Last week, I had to take a look again at the game's combat to see why it still feels lackluster. The main issue is that we have no way to change up the **player's hierarchy of priorities**.

For example, the melee enemies ALL just chase the player and attack once they are within range. Therefore, the enemy that is closest to the player will always pose the highest threat.

### Again, Creating More Minigames for Experiment Logs

This was not completed from the previous weeks, so it is being put on the list of things to do again.
- I've got a couple in the ClickUp that I want to bang out, but I'll be adding more.

## Enemies, Yet Again

![](<../../../_Meta/Attachments/Pasted image 20260413202900.png>)

Given the hierarchy of priorities we are trying to establish, let's redesign the enemy attacks:

### Primordial Wraith

Creates a wall of fire that limits the player's space to move.
- The player will take damage if they step into this wall.
- We can hide (ranged) enemies behind the wall to make them inaccessible until kill the fire wraith creating the fire wall.

### Twilight Wraith

- Keep this guy, but make him shoot a projectile normally like the OLD primordial wraith did.
- Projectile will no longer fire in an arc, straight line only

### Tempest (Lightning) Wraith

- No more tracking projectile. That is booboo.
- Instead, we have it make a lightning strike on the player's location.
- Beneath the player's feet will be a big bright circle that shows where the lightning strike is going to hit, and the player will have a second or two to get out of the way before the lightning strike hits.

### Kamikaze Enemy 

- The one Azalee is supposed to be making.
- Runs towards the player and explodes or something idk.

### Finish Any Other Unfinished Work from Previous Weeks

Ongoing work:
- New Enemy 1
- New Enemy 2
- New character portraits
- New UI assets for journal entry screen
