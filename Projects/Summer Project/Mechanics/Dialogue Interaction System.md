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
- Character-unique text sounds

# Where Are Dialogue Interactions Found?

We need the ability to trigger dialogue interactions whenever.

### Dialogue Interaction Triggers

Dialogue interaction triggers are defined by:
- Which level they are found in
- What type of trigger is it?
	- Run start trigger
	- Room clear trigger
	- Room enter trigger

# How Do We Determine Which Dialogue Interaction Play

### Flags

We'll use *flags* / tags / values that tell us more about each line of dialogue. Each dialogue interaction is defined by a series of flags that apply to all dialogue interactions, as well as unique tags that only apply to certain dialogue lines.

In order for a line to be considered to be played, all of the flags must be true.

To break it down further, dialogue interactions will have flags like:
- PlaysInAreas: the list of areas of the game the interaction can be played in (1, 2, 3). If the player is not in one of the valid areas, then this interaction will not play.
- PlaysInInteractionTypes: the list of interaction types the interaction can be played in (run start, room clear, room enter). If the dialogue interaction trigger is not one of the valid types, then this interaction will not play.
- UniqueTags: A list of unique boolean flags that MUST be true in order for this interaction to play (Killed first boss, has died yet, etc.)
