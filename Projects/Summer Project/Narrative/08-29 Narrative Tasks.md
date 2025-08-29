
> Note: This isn't the backlog of things to write. Ngl, that's gonna have to come later. For now, w

### Expressive Emotions in the Dialogue

- I have added the foundation for supporting emotive animations in the game's dialogue sequences.

#### The Task(s)
- I need you to create a list of 3-5 types of emotions that can expressed through animating the images of the characters (by shaking, scaling, stretching, or rotating the sprite)
- Then, you'll create the assets required for these emotions (you are NOT responsible for animating them, unless you want to idk). See [Creating a New Emotion Asset](<#Creating a New Emotion Asset>) for creating new emotion assets.
- Then, you need to go through ALL (I think there are 29) of the existing dialogue interactions that have already been implemented and see where you can add these emotions

#### Creating a New Emotion Asset

- Emotion assets are stored in `Avernoth > Narrative > DialogueEmotions`
- Right click within the folder, create a new `Data Asset`, select the `DIS Emotion` type
![](<../../../_Meta/Attachments/Pasted image 20250829120318.png>)
- Set the `Name` to whatever you want the name of the emotion to be.
- Make sure the two check boxes are enabled
- Set the `Portrait Animation Name` and `Text Box Animation Name` to the same value as the `Name`. 
	- It is important that these are named properly and not misspelled because these are used to actually play the animations of the UI objects
- Boom, that's it