### Saving Dialogue Information Between Runs

This week, I personally have been focusing on implementing some of the game's roguelike / roguelite mechanics. This includes carrying over the dialogue information from run-to-run. This is now fully functional.

> Note: This system relies on loading the user's saved game data to check the dialogue info. 
> 
> The game's save info is only loaded when the user starts a new run from the main menu / dies and presses the restart button. If you start playing a level in-editor, the saved data will not be loaded.

#### Example: Beginning a New Run

In the player's very first run of the game:
- Allister will *always* say "ugh my head" or something BEFORE the screen fades from black.
- Then, when interacting with the portal in the room, Allister will *always* talk to Magnus, who explains the situation.

In subsequent runs:
- There is no dialogue before the screen fades from black. It just fades from black. (we can change this though)
- Then, when interacting with the portal in the room, a random character talks to Allister.

### Dialogue Animations Showcase

The dialogue animations are a thing now. Each animation is composed of two distinct parts:
- The portrait animation: This type of animation affects only the character's portrait image.
- The "text box animation": The name is a little misleading. This type of animation can affect literally any other piece of UI on the dialogue screen. It was just initially used for the text box.

> Note: The animations are split into two distinct parts due to how the UI has been implemented. 

#### What Types of Animation can We Have?

- Most properties on the UI elements can be easily animated. This includes position, scale, rotation, color, opacity, etc.
- So, this means we can have things like:
	- Translations (Jumps, slides, shakes, etc)
	- Scales (pulses, grows, shrinks, etc)
	- Rotations (swings, tilts, spins, etc)
	- Color changes (flashes, tints, fades, etc)
	- Opacity changes (fades, blinks, etc)
	- Combinations of the above (e.g. a shake that also fades out)

#### What Types of Animation Can't We Have?

- As of right now, anything that removes the text should be out of the picture. 
- So, an effect that hides the textbox, or temporarily pauses the text from being displayed, or removes the portrait image, etc.
- Maybe we can incorporate these in the future, but for now, nah
- Also, I'm sure you know, but there are no different expressions for the character sprites. The portraits we have now are the portraits we have now.

#### Example: Test Dialogue Animation

### Font Change

In the meeting with Alecks last week, we were talking about the font used in the game and how it would probably need to be updated to match the crunchy feeling that everything else in the game has.

Chat, how do we feel about using pixelated fonts?