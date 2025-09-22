# Meeting Times

| Meeting                                | Possible Times |
| -------------------------------------- | -------------- |
| LD Meeting                             |                |
| Narrative Designer + CD Meeting        |                |
| Sound Meeting                          |                |
| Environmental Artist Meeting           |                |
| 2D Artist + Narrative Designer Meeting |                |
| Animation Meeting                      |                |
| Character Artist Meeting               |                |

# Version Changes

I didn't send out a build lol.

#### 0.2.0

#### 0.3.0

#### The Build: 0.3.0
As usual, playtest the build when you get the chance and please provide feedback. It could be as simple as "this is confusing" or "this doesn't feel good."

#### What Didn't Get Fixed Yet?
- Death screen font is still hard to read
- The questions at the start of the game still don't have the interesting text that has been written already.

# Upcoming Changes

### More Passive Spells!

#### Reapproach How we Think About Passive Spells
- Right now, there is support for the player to have *up to 3 passive spells* at a time.
- But, honestly I've been having a hard time thinking about constantly rewarding the player throughout the run.
- So, I though about this: What if we let the player have *unlimited* passive spells? This'll help with that whole power fantasy aspect you see in a lot of rogue-likes.

#### Establish a Design Language for Passive Icons
- We should have a consistent design language for the icons of passive spells.
- We can start by parameterizing the passive spells:
	- What event do they respond to (i.e when the player takes damage, when clearing a room, when doing a perfect dodge, etc.)
	- What does the passive do (i.e increase a specific stat, heal the player, etc.)
- Furthermore, specific stats would need consistent iconography (i.e a heart for health, a shield for resilience, etc.)
- From there, 

#### Passive Spells that Do Things
- The passive spells in the game right now are primarily stat boosts that happen as a result of some event in the game.
- But, I think we can do more interesting things with passive spells such as:
	- Firing a projectile
	- Temporary invincibility
	- Healing over time
	- Etc.