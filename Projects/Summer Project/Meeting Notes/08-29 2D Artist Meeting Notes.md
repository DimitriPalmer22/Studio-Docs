# UI Elements that Need to be Updated

### Reticle
The reticle works a lot like the reticle in Kingdom Hearts. The player has two targeting modes:
- Free targeting mode: The player can move the camera around freely. The targeting reticle will automatically move to the enemy that is closest to the center of the screen.
- Lock-on targeting mode: The player can lock onto a specific enemy. The reticle will stay on that enemy until the player unlocks or the enemy is defeated.
There should be two distinct reticle designs for each mode.

### New Dialogue Text Box
I was thinking a scroll design for the dialogue text box. The left and right sides of the text box would be rolled up.

![](<../../../_Meta/Attachments/Pasted image 20250829111450.png>)

### Room Clear Text Box
Something that looks similar to the scroll text box (mentioned above) would be pretty fire. 

![](<../../../_Meta/Attachments/Pasted image 20250829112110.png>)

### Upgrade Room Background PNG

- This should probably be dithered & pixelation to match the rest of the new UI elements

![](<../../../_Meta/Attachments/Pasted image 20250829112508.png>)

### Transmutation Circle Image for Upgrade Book

![](<../../../_Meta/Attachments/Pasted image 20250829114345.png>)

- Separate the transmutation circle into multiple PNGs for each layer of the circle
- Then, in-engine, we'll animate each layer of the circle to rotate at different speeds to give it a really magical look

### New Font

- We need a new pixelated font to fit the design language
- The one font we have for the upgrade screen is cool, but it needs to be pixelated

### Buttons

![](<../../../_Meta/Attachments/Pasted image 20250829114734.png>)

- We need new assets for clickable UI buttons in the game. As of right now, it's just the "room clear" asset being slapped all over the place
- We can do something in a style similar to the new health bar asset.

### Feedback on New Animations

- The scale-up when characters are entering is a little too harsh
	- We reduced it in-call
- Any vertical animations should probably be down or should at least hide the fact that the bottom of the characters is cut off