### Aiden's Lighting of Matthew's Level

- Use `MatthewBlock2_POCCopy`
- Add a light in that one corner

### Which Levels Have Been Made, but Aren't in the Pool of Levels?

> Aiden's big outdoor level is gonna be the "Boss Room"

- Aiden big level
- Aiden indoor level
- Brian's new level

> MAKE SURE TO RE-SEND THE DOCS TO PREPARE THE LEVELS TO BE IN THE GAME!!!

### Set-dressing Using the Existing Props

- GO THROUGH ALL YOUR LEVELS AND SET-DRESS USING THE EXISTING PROP ASSETS.
- REPLACE / DELETE ALL THE PLACEHOLDER ASSETS

- All the existing props are in `Avernoth/Art/Common/Props`

- Barrel
- Cauldron
- jarL
- jarS
- potions
	- Potion 1
	- Potion 2
	- Potion 3
- Step stool
- Vial holder
	- Individual vials
	- Just the holder by itself
	- A vial holder filled with vials

![](<../../../_Meta/Attachments/Pasted image 20250805201421.png>)
### Leonardo "Leo" Santa-Zapata

- Texture the uhh…

### UI
- Questions at the start of the game widget blueprints:
	- The entire screen's widget: `WBP_TomeQuestionScreen`
	- The buttons for the answers: `WBP_TomeAnswerButton`
	- Note: The buttons don't a
- Room clear text widget blueprint: `WBP_RoomClear` 
	- This straight up just needs to look better
	- This widget uses the animation window to animate the text appearing on screen. You can play around with this if you want
- Dialogue text widget blueprint `WBP_DialogueText`
	- I reformatted this today in the 2D artist + narrative designer meeting.
	- Really, the main things you need to focus on are making actual UI assets for the text box & name box.
	- Try not to change the format of where the characters are located or where the main text box appears
	- Also, don't change the transparency of the text box too much. We need it to remain transparent so we can see the design of the characters behind it.
- Journal entry widget blueprint `WBP_JournalEntry`

### VFX
- An blue sparkle explosion or light or something for when the player clears the room. This is gonna emit from the the exit platform of the level.
- A VFX for the journal table. Idk sparkles or something.
