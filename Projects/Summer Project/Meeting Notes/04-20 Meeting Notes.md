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

### Polish Con
