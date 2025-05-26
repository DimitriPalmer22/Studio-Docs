
> Note: As we get further into development, the content on this page may become outdated.

# Brief Overview of the Terms

### Dialogue Interaction

A *dialogue interaction* is a list of *"Dialogue Lines"* from one or more characters.
- The dialogue interaction will simply iterate through this list of dialogue lines.
- During these interactions, there is no user input into what is said. These interactions are predefined.

Ideally, the dialogue interactions can be triggered from anywhere in the game that we define. However, only a specific set of dialogue interactions have the chance to play depending on the current conditions in the game.

### Dialogue Line

*Dialogue lines* are a single line of dialogue spoken by one person. They can be more than one sentence or even a sentence fragment.

Dialogue Lines are characterized by:
- *The Dialogue Character*
- The text contained within the line

### Dialogue Character

The character that is speaking the line of dialogue.

Dialogue Characters are defined by:
- *The character portrait* that appears when the corresponding dialogue line is triggered
- *The character name* that appears when the corresponding dialogue line is triggered

# Creating New Dialogue

### Creating a New Dialogue Interaction

1. In the content drawer, navigate to the `Game/Avernoth/Narrative/DialogueInteractions` folder
2. Either find an appropriate folder or create a new folder to put your interaction in
3. In this folder, right-click and search "data asset"
4. In the data asset creation window, search for `DIS_Interaction`. `BP_DIS_Interaction` should come up. Click it
5. Name the new asset with the following format: `DIS_Interaction_InteractionName`
6. Open the new data asset
7. Set the attributes of the Dialogue Interaction
	1. *Add to Interaction pool*: This is a boolean flag to determine if this dialogue interaction should be included in the game's list of available dialogue interactions. If this is set to false, the interaction will not be played during normal gameplay. You should only ever set this to false for dialogue interactions that are not yet ready to be played or are only used for testing purposes.
	2. *Interaction Description*: A brief description of the dialogue interaction. This is NOT used in-game whatsoever. This is only used so that we, the devs, know what the interaction is about without having to read through the entire interaction.
	3. *Lines*. This is the list of dialogue lines that will be iterated through during the interaction. You can add new dialogue lines by clicking the `+` button next to the `Lines` attribute. For each line, expand the line to see its attributes.
		1. *Character*: The dialogue character asset used for this line. Select the appropriate dialogue character asset from the dropdown. If the character you want isn't there, then you need to create a new one.
		2. *Text*: The words that appear on screen when this line is spoken.
	4. *Is Forced*: This is a boolean flag that determines if this dialogue interaction MUST be played if all the flags are true. This is only used for dialogue interactions that we NEED the poka

### Creating a New Dialogue Character

Dialogue characters are stored as assets, so you only have to create one for each character once and then you can reuse it in any dialogue interaction.
