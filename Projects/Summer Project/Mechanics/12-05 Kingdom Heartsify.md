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
- Something we see a lot of in Kingdom Hearts 2 is *enemies that become invincible* for a short time before attacking.
	- For example, the basic heartless enemies phase into the ground and will attack the player once the come up. While the enemies are underground, the player focuses on other enemies, which allows the phased enemies to catch the player off guard once they resurface. Alone, they are not much of a threat, but in groups, they can be dangerous.
	- Another example are the heartless enemies with two tails. They'll dive into the ground and become invincible for a short time before surfacing and attacking the player. The difference here is that the enemies are STILL invincible while attacking, which forces the player to dodge or block the attack rather than simply attacking through it. The only opportunity to damage these enemies is by either parrying / blocking the attack or attacking them while they are above ground before they can attack.
- *Some enemies will completely retreat* before attacking, making them virtually unhittable before they complete their attack sequence.
	- For instance, ...
- *Some enemies have certain conditions* that must be met before being damaged.
	- For instance, the big heartless enemies with the big bellies cannot be damaged from the front. The player must either attack them from behind or use a specific move to stagger them before being able to damage them.
- *Some enemies will relocate themselves* to gain a tactical advantage before attacking.
	- For instance, flying enemies will often move to higher ground before attacking the player, forcing the player to start aerial combos to reach them.
	- Other enemies will just move further away from the player to force the player to close the distance before attacking. In theory, this should allow the enemy to set up their attack better before the player comes within range.

### Is This Necessary?
- For every enemy, no. 
- But, for key enemies and bosses, absolutely.
- The more dynamic each enemy is, then the more engaging the combat will feel.
- The game's difficulty will derive from how well the player is able to manage the various enemy attack patterns and respond to them.