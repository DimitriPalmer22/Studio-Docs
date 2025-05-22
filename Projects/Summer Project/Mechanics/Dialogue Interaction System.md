I need some way to represent the dialogue system in-engine so that dialogue can start being implemented properly.
# What is a Dialogue Interaction?

- A dialogue interaction is a list of *"Dialogue Lines"* from one or more characters.
- The dialogue interaction will simply iterate through this list of dialogue lines.
- During these interactions, there is no user input into what is said. These interactions are predefined.

### Dialogue Line

- A single line of dialogue spoken by one person.
	- Can be more than one sentence or even a sentence fragment

Dialogue Lines are characterized by:
- *The Dialogue Character*
- The text contained within the line
- The text speed for that line?
- Any special formatting for that line?

### Dialogue Character
- The character that is speaking the line of dialogue.

Dialogue Characters are defined by:
- *The character portrait* that appears when the corresponding dialogue line is triggered
- *The character name* that appears when the corresponding dialogue line is triggered

Ideas:
- Character-unique fonts?

# Where Are Dialogue Interactions Found?

In our game, there are "rooms".

BUT, we need the ability to trigger dialogue interactions whenever.

# How Do We Determine Which Dialogue Interaction Play

### Flags

We'll use *flags* / tags / values that tell us more about each line of dialogue. Each dialogue interaction is defined

### Forced Dialogue Lines
