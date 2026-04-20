# 04-20 Meeting Notes

## Updates to the Game

### Wraith Behavior Rework

Each of the wraiths now have different attacks:

- **The primordial (fire) wraith** - fires a wall of fire that damages the player if they step in it, restricting their movement. They don't move, but will rotate toward the player.
- **The twilight (shadow) wraith** - fires a projectile in a straight line toward the player. They cannot move, but will rotate toward the player.
- **The tempest (lightning) wraith** - summons a lightning strike on the player's location. A big bright circle appears on the ground where the lightning strike is going to hit, and indicates how much time the player has to get out of the way before the lightning strike hits.

This helped a good amount with making the combat a lot more engaging.

### Minigame Stuff

We currently have 3 types of minigames for the experiment logs:
- A pattern memorization minigame where you have to memorize a pattern and then interact with those items in the correct order.
- A hold-and-release minigame where you have to hold a button to fill a bar, and then release it when the bar is *nearly* full.
- A button mashing minigame where you have to repeatedly mash a button to fill a bar before a timer runs out. The bar depletes at a constant rate when you're not pressing the button.

These are just generic minigames that can then be slapped onto different quests with different themes and aesthetics.

For example, here are some of the existing minigames in the game's code:

#### Button Mashing - Cauldron Minigame

- The player has to collect various items in the room
- Once they have all the required items, they can then interact with a cauldron in the room to add them to the cauldron
- Then, a button mashing minigame triggers to stir the cauldron and mix the ingredients together. The player has to fill the bar before the timer runs out to successfully mix the ingredients.

#### Button Mashing - Channeling Mana from a Tome

- The player walks up to a pre-existing tome that's just laying around one of the levels.
- They can interact with it to channel energy from it
- A button mashing minigame triggers, where the player has to repeatedly mash a button to draw the energy out of the tome and into themselves. If they fill the bar before the timer runs out, they successfully draw the energy out and complete the quest.

#### Pattern Memorization - Brazier Puzzle

- There are a set of braziers laid out in a room.
- When the player approaches the braziers and interacts with (*some item around the braziers*), fire sparks from the braziers in the specific order that they need to be interacted with.
- The player must interact with the braziers in the correct order to complete the quest.

#### Hold & Release - Imbuing a Weapon with Magic

## Plans Going Forward

### Polish Content Accessible in Demo

- Combat feels the best it has felt in a while due to enemy improvements.
- Overall presentation of information & cutscenes feels good.
- However, some aspects of the game can still be improved.

In about a week and a half, we'll be funneling more people to the demo, so we should probably polish up the content that's currently accessible in the demo to make sure it's as good as it can be. This includes:

#### Revise Enemy Wave Setups

Now that the enemies have been changed, we need to change up the enemy wave setups in the demo to make them more engaging and fun with the new enemy behaviors. A big part of our enemy designs are based around the enemies working together, so keep that in mind.

Some waves have too many of one type of enemy (especially fire wraiths. Use those sparingly). Some waves have ONLY melee enemies or ONLY ranged enemies, which is not ideal. We want to have a good mix of different types of enemies in each wave to make them more engaging and fun.

> Note: Also consider how much space the player has to operate in for each wave. Some enemies block off space or require you to move around ALOT to fight them, so we should consider that when designing the waves. Maybe some rooms just aren't cut out for specific enemies.

#### Game Balancing

The game is difficult, even for me. We need to do some balancing to make sure the game is challenging, but also fair and fun. This includes:
- Distribution of enemies per-wave (too few vs. too many)
- Enemy health and damage values
- Player health and damage values
- Health pickup distribution
- Shop currency distribution
- etc.

#### 
