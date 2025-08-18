# The Theory and Stuff

### Level Design Feedback

These are a couple things that people (both inside and outside the team) have said about the level design that I think we should consider. We don't have to necessarily change everything in accordance with this feedback, but I think it is worth considering.

#### Feedback From the One Guy in Shbeeb's Server
- The levels don't seem like very interesting places for gameplay
- The player and enemies are just standing in open space firing and dodging
- If we want to get the environment involved:
	- create useful cover for the player and enemies
	- create useful ways for the player to flank

#### Feedback from Me
- Personally, I think

### How Do We Make the Levels More Interesting?
Make sure the game is *fun* to play. The levels need to support this.

1. We should make the levels more interesting in terms of gameplay (think of features and mechanics that do this).
2. Then, use that information to determine how to make the levels more visually interesting. What props and structures do we need to support the gameplay?

#### When Do These Types of Games Feel Fun?

I've found that these games feel the most fun when:
- The player is *forced to engage* with the enemies (no shooting them from outside their range or running past enemies without consequence). You, the player, MUST actively be trying to kill the enemies to progress.
- The player is able to *skillfully* avoid damage and defeat enemies. Risk-reward mechanics are a big part of this.
- The enemies pose enough of a threat to the player that there is *significant risk of death* most of the time
- Despite the difficulty, the player never feels like the game is *unfair*.

The sense of skill expression and high level of difficulty adds a lot of replayability to these types of games. Players will want to keep trying to get better at the game.

#### When Do These Games Feel Unfair?

I've found that the game typically feels unfair when:
- The player is *not given enough information* to make a good decision
- The player has something happen to them that they feel is *outside of their control*

##### What Information Does the Player Need?
- Where are the enemies?
- When are the enemies going to attack?
- When is it safe for the player to attack?
- Where is the most optimal position to engage the enemies?

##### What Can Happen That is "Outside of the Player's Control"?
- Enemies suddenly spawn behind the player without warning
- Enemies suddenly attack the player without warning
- Enemies can attack the player from off-screen with little indication
- The player gets stuck on a piece of the level while moving

#### Making the Levels More Gameplay Interesting

> This section addresses the points mentioned in [When Do These Types of Games Feel Fun?](<#When Do These Types of Games Feel Fun?>) and [When Do These Games Feel Unfair?](<#When Do These Games Feel Unfair?>).

##### The Enemies Need to Pose a Significant Threat to the Player
As of right now, the enemies are far too easy to defeat. This is mostly my fault since the enemy AI is only so complex.

##### Force the Player to Engage with the Enemies
As it is now, when the player first loads into the room, the enemies are already standing around just begging to be shot at.
- This is ***LAME***
- This lets the player start the encounter against the enemies with a clear advantage (they can attack the enemies before the enemies detect them)

Here are some ideas to fix this:
- Wait until the player **gets further into the room** before spawning the enemies.
- **Shrink the size** of the space the player is supposed to engage the enemies from to ensure the enemies detect the player
- Use traps and environmental hazards to restrict the player within the desired area

#### Making the Levels More Visually Interesting
- ;

# Actually Making Levels

When we started this project, you guys told me that you wanted to *make level maps and proper documentation* for these levels so we could go about making levels the right way.

For right now, we'll hold off on making level maps.