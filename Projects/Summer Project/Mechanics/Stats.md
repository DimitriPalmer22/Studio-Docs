
### What is a Stat

- A stat is a struct that contains the following:
	- Name - a string that identifies the stat
	- Base value - the base value of the stat
		- public get access; private set access
		- Setter clamps the value between the minimum and maximum values
	- Maximum value - the maximum value of the stat
		- A max value below 0 means the stat is not capped
		- Should have a getter for this
	- Minimum value - the minimum value of the stat
	- Description - a string that describes the stat

- Stats should also contain operator overloads that either add a stat to another stat or add a numeric value to the stat

### What Are the Types of Stats

- Character Stats
- Elemental Stats

### Where Are the Stats Found?

- The Player & enemies
- The Tomes

# Character Stats

### What Are the Character Stats?

- Vitality - Determines the maximum health of a character
- Mana - Determines the maximum mana of a character

- Intelligence - Determines the damage done by a spell
- Resilience - Reduces the damage taken from attacks
- Agility - Overall speed & dodge range / invincibility frames
	- In terms of the invincibility frames, think of this like 2k, where the stat doesn't linearly correlate to the expected output. Instead, it acts as a threshold that unlocks different tiers the higher the stat is.
	- For example, 1x agility may give you 10 invincibility frame, while 2x agility may give you 15 invincibility frames, and so on.
- Cast Speed - How quickly a character can cast spells. Also affects cooldown times

# Elemental Stats

### What Are the Elemental Stats

### Where Are the Elemental Stats Found?
