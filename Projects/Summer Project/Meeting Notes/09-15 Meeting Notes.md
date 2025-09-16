### Meeting Times

| Meeting                                | Possible Times  |
| -------------------------------------- | --------------- |
| LD Meeting                             | Wednesday @ 8pm |
| Narrative Designer + CD Meeting        |                 |
| Sound Meeting                          |                 |
| Environmental Artist Meeting           |                 |
| 2D Artist + Narrative Designer Meeting |                 |
| Animation Meeting                      |                 |
| Character Artist Meeting               |                 |

### Quick Recap on Last Week's Mana Rework
[Big Change, Huge Even - Mana Rework](<./09-08 Meeting Notes.md#Big Change, Huge Even - Mana Rework>)

### Updates Since Last Week

#### Version Numbers
- I've starting using *semantic version numbering* to keep track of the current state of the game.
- Builds will be marked with version numbers.
- Also, in Git / GitHub, you'll see commits *tagged* with version numbers. This is to signify that the commit will be / was used to create a build.
- Currently, the game is on `version 0.1.1`

#### Agility Stat Actually Does Something Now
Here's a quick refresher on the game's 5 character stats:
- Vitality -> Directly affects your max health
- Mana -> Directly affects your max mana
- Intelligence -> Affects your spell damage
- Resilience -> Affects how much damage enemy attacks do to you
- Agility -> *Affects your casting speed*

#### Update on the Spell Ideology
- Over the past week, we've been looking into ways to essentially make the game feel more fluid and fast-paced.
- Pretty much every primary spell will be a sequence of attacks that can be chained together fluidly.
- Pretty much every secondary spell will be a powerful single-cast ability that the primary spells can chain into.
	- The secondary spells should, for the most part, help with AOE damage.
	- As a reference, if you've every played Kingdom Hearts, think of the different finishers you can use in those games.
- So, each individual animation should be pretty quick and responsive. If it isn't then there should be some type of super-armor or something similar to make up for it. 

##### Transitioned Most of the Spell Stuff To C++
- Most of the spell functionality was previously implemented in Blueprints.
- Now it's in C++, which makes it easier to maintain and expand upon.

##### Retimed all the Spell Animations
- All of the spell animations have been retimed a little to be a little more balanced and feel a little better.
- They're all a *teeny* bit slower and they should hold their end poses for a little bit longer before allowing the player to attack again.

##### New Secondary Spell?
- After moving most of the spell stuff to C++, I make a new spell real quick to test out how easy it would be to make spells.

#### Indicating that You Have Enough Mana
Whenever the player earns enough mana to use their secondary spell:
- The spell icon in the bottom right corner will do a little hop animation
- Allister's model will flash cyan a couple times

#### Every projectile has a slight AOE to it
- This is to make it easier to hit enemies with projectiles, especially in groups.

#### Limit Successive Dodges to 2
- The player can only perform a max of 2 dodges before a short cooldown is applied.
- This was to prevent dodge spam

### Playtesting Feedback?


### What Next?
- I'll go over the playtest notes you guys have sent and will try to address any large issues that have come up
- Passively drain mana over time while not comboing enemies?
	- Reinforces aggressive playstyle
- Animation Meeting fr
