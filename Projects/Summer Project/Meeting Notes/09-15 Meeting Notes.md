### Meeting Times

| Meeting                                | Possible Times |
| -------------------------------------- | -------------- |
| LD Meeting                             |                |
| Narrative Designer + CD Meeting        |                |
| Sound Meeting                          |                |
| Environmental Artist Meeting           |                |
| 2D Artist + Narrative Designer Meeting |                |
| Animation Meeting                      |                |
| Character Artist Meeting               |                |

### Quick Recap on Last Week's Mana Rework


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

#### Transitioned Most of the Spell Stuff To C++
- Most of the spell functionality was previously implemented in Blueprints.
- Now it's in C++, which makes it easier to maintain and expand upon.

#### Retimed all the Spell Animations
- All of the spell animations have been retimed a little to be a little more bala

### Playtesting Feedback