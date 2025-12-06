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
- A list could look like: Primary, Primary, Dodge, Secondary