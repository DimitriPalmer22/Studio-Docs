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
- The associated animation + logic that will be triggered when the player action is executed.