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

## Production Timeline

### Goal: Make Money
This means we have to sell the game for money.

### Getting The Steam Page Up

#### $100 to get the Steam Page Up
- At some point very very soon, I will ask you guys for some money to get the Steam page up. Any amount would be greatly appreciated.

#### Marketing Materials
!![](<../../../_Meta/Attachments/Pasted image 20251208192836.png>)

### Creating A Playtest-able Build

*By the end of December*, I want to start holding regular playtests of the game (sending them to other people). This is for two reasons:
- Feedback
- Marketing. Allowing people to play the game will create some type of community for it.

### Steam Next Fest / Creating a Full Playable Demo

> Note: In order to be eligible for February's next fest, the game must be set to release fully on or after March 2nd.

- January 5th: Registration Deadline - up-to-date marketing materials (recommended). Steam page up and public. Trailer is also a good idea.
- January 26th: Demo build submitted for review
- February 9th: All required materials due
- February 26th: Next fest starts

#### Next Fest

## v0.14.0 Updates and Goals

### Gameplay Pivot Ideology
- You remember when, at some point, I said this game would be like Kingdom Hearts. Well, it sure didn't feel like it.
- I realized that it's ok for the game to feel more derivative of our inspirations as long as we still have some aspects that make it unique.
- So, the combat ***WILL*** feel more like Kingdom Hearts from now on!

### Combat Tweaks
> Note: Some of these are still being worked on.

#### Player Attack
Our game is only going to have so many buttons to work with. So, we need to make sure that combat feels dynamic in spite of this.

##### Primary Spells
- Before, the primary spells were just a simple string of attacks that the player could perform. *This made gameplay very stale* and unengaging.
- Now, primary spells give you a library of moves to perform based on context (Kinda like Kingdom Hearts)
	- There are / will be different attacks depending on conditions like how far away an enemy is or how many enemies are around you.
- This way, spamming the same attack button will still feel dynamic and engaging.
- There should be several moves to increase the fluidity of combat (like moves that bring enemies closer to you, or moves that let you close distance quickly.)

##### Primary Spell Rework: Flame Volley
- Flame volley's range is EVEN SHORTER
- There is now a move that closes distance to enemies when they are just out of reach.
- There is a now a move that plays when attacking immediately after dodging.

> Note: The other spells are gonna be reworked in a similar manner.

##### Secondary Spells (None of this is implemented yet)
- 

#### Enemy Behavior

##### Why are the enemies so terrible?
- Right now the enemies are not very *proactive*. They just stand there and wait to be attacked.
- This makes combat feel one-dimensional and boring.
- Enemies need a way to guarantee that they can attack the player first, rather than waiting for the player to attack them.
- At no point does it feel like the player needs to strategically approach combat. They just spam attacks until everything dies.

##### Revised Enemy: Primordial (Fire) Knight
- To address the above issue, the Fire Knight enemy has been revised to be more proactive.
- If the player is too close to the knight, the knight will dodge backward.
- If the player does too much damage to the knight in a short span of time, the knight will dodge backward AND THEN do their thrusting attack.
- Also, the beginning of the knight's thrust attack has super-armor, so the player can't just interrupt it with attacks initially.