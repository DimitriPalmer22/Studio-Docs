# Spell Rework (Again)
- "Spells" shouldn't be thought of as individual attacks
- Rather, each spell is a library of related moves the player can perform based on given contexts
- For instance, the flame volley spell grants you:
	- A basic three-hit string for when enemies are a reasonable distance away
	- A closing-distance attack for when enemies are just out of reach
	- An attack for when the player comes out of a dodge

# Player Action Abstraction
- Data assets for actions the player can perform via inputs
- The asset itself is empty. It is simply used to bridge inputs with animations and effects.
- This will allow us to easily swap out or add animations and effects without needing to change input handling code.


# Player Input Processing
- Input handling code will no longer directly trigger animations or effects
- Instead, inputs will add player actions to a list of actions that have been performed.
	- For example, pressing the attack button will add a "Primary Attack" action to the list.
	- A list *could* look like: 1. Primary, 2. Primary, 3. Dodge, 4. Primary
- The player action processing system will then interpret this list and determine what animations and effects to trigger based on the current context.
	- With the above example, the input processor will decide whether to use the basic Primary (the 4th player action), or should it trigger the dodge-attack version of the Primary based on the 3rd player action.
	- This will be defined by the spell library associated with the Primary attack.

### Setting up An Input for A Spell
Each spell input should be set up as:
- A list of player actions (An array of player action data assets)
- Some type of context-aware interpreter that will determine which player action to trigger based on the current context (distance to enemy, player state, etc.)
- The associated animation + logic that will be triggered when the player action is executed. Each of these can be its OWN gameplay ability.

# Enemy Attacks

### Enemy Proactivity
- A big part of why combat feels so stale is because the player is almost never challenged to react to enemy actions.
- Everything in the game feels like it is the player's doing, and enemies are just sitting there waiting to be attacked.
- This leads to a very one-dimensional combat experience where the player just spams attacks until everything dies.
- Instead, we need to focus on a more dynamic combat system where enemies can proactively challenge the player.
- This is largely due to the enemies almost never having an opportunity to act first. Once the player begins to attack an enemy, the enemy is almost always on the defensive.

### How Does Kingdom Hearts 2 Do This?
- Something we see a lot of in Kingdom Hearts 2 is enemies that become invincible for a short time before attacking.
	- For example, the basic heartless enemies phase into the ground and will attack the player once the come up. While the enemies are underground, the player focuses on other enemies, which allows the phased enemies to catch the player off guard once they resurface. Alone, they are not much of a threat, but in groups, they can be dangerous.
	- Another example are the heartless enemies with two tails. They'l