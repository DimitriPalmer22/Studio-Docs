# 08-04 Meeting Notes

### Meeting Times

> I'm unavailable Saturday night :(

| Meeting                                | Possible Times   |
| -------------------------------------- | ---------------- |
| LD Meeting                             | Tuesday @ 8pm    |
| Narrative Designer + CD Meeting        | Wednesday @ 11am |
| Sound Meeting                          | Thursday @ 11am  |
| Environmental Artist Meeting           | Thursday @ 5pm   |
| 2D Artist + Narrative Designer Meeting | Friday @ 11am    |
| Animation Meeting                      | TBA              |
| Character Artist Meeting               | Uhh…             |

### Play the Game in the Meeting

#### Changes to the Game

> This week, I've tried to keep you guys a little more updated than usual by sending more videos in the Discord. You guys can check those out if you want.

##### Music and SFX

- A whole new wave of SFX has been added
- I also made a music track and put it in as the background music
- [More Info Here](<../Audio/07-31 Audio Update Notes.md>)

##### There is Now a Very Basic Death Screen

- When you run out of health, it shows up. yup.

##### The Shop

- The shop is a room that spawns at least once per area
- Here, the player can interact with a talking magical gargoyle
- This opens the shop menu where they can exchange mana essence (the currency) for different items

##### Camera Feedback Change

- Idk if some of you guys saw, but last week, after the meeting, I made a video showing the camera swaying whenever Allister does an attack
- After some feedback, I've taken that out and replaced it with a camera shake whenever the player's spell hits an enemy

##### Room Clear Notification

- People were having trouble telling when they have defeated all the enemies in the room.
- So, there is now a (very ugly) room clear notification that appears at the top of the screen
- Also, a sound plays, too
- However, I want an even stronger in-world indication that the player has cleared the room.
	- Any thoughts?
	- Maybe VFX?

##### Enemies

- Considering that both of the 3D character artist are out of town, we're *probably* going to have to stick with the placeholder enemies we have for right now and refine them
- So, I've removed the health bar above their heads (that was there purely for testing purposes)
- The enemies (and Allister) now flash red whenever they take damage.
	- I though about having the color of the flash indicate how much health they had left (yellow = medium health, red = almost dead), but idk how I feel about it
- Also, I've replaced their material, so they're no longer green

##### Imported New Models

###### Rae's Models

###### Kiana's Models

##### Updated Allister Materials

- Allister's materials have been updated. He is now using the master material that pretty much the rest of the game is using.
- Now, his material supports using the Alpha in his textures as an Alpha mask, so we can selectively clip out parts of his model (this can be done for other models too)
- As a result, his hair looks like hair now.
- Also, I think his scarf is a little skinner around the neck too
- Also, the old material was glossy and made it harder to read the detail on his model. This material should be a little better in that regard.

##### Updated Spell Combos

- The combo system we have as of right now is very modular, and pretty much allows us to combine different hits to make different and unique combo chains
- This way, we can reuse some animations but still increase the output of the number of spells
- *This is where I show off the one spell that's a little wacky*
- *Show off Combo02 as well*

##### Dashes

- Dash animations have been revised
- There's this sick twirl that Andre made, you guys should give him applause or something

##### Journal Table

- Here, Allister can read journal entries left behind by the Archmage who created Avernoth.
- Whenever Allister enters a room, these have a chance to spawn
- As of right now, it's a little boring visually, but it'll get there

##### New Portraits

- A couple new portraits have been added to the game.
- Some of these are pretty much done.

##### VFX

- Fireball impact VFX
- Trails behind the crystals in the Crystal Barrage Spell

##### Andre Animations

- *Show this off in-call*

##### Nerdy Stuff

- I enabled Screen-Space global illumination, so your performance might be a teeny tiny bit worse, but I doubt it's too bad.
- I really only added this to get some more dynamic lighting in the game, but it doesn't make that much of a difference

#### Feedback from the Group

- For the next room VFX, have something shooting up from the circle
- Send a video of the colors changing when people are hits

### What Gets Showcased in the Video We Send in the Server?

- In terms of things being "complete" or "presentable", people are only going to see what we show them, so we can strategically show only what we want to show people.
- If anyone asks "ayo who worked on this," I won't hesitate to say names, so lmk if you don't want me to do that for you specifically.

### Tasks For This Week

#### Programmers

- [x] Dimitri Palmer

- Enemy AI Stuff
- Implement more spells
- Implement passive spells
- General polish

#### Designers

##### Level Design

- [ ] Leonardo Santa-Zapata
- [ ] Aiden Richmond

- Review the lighting Aiden did
- For any levels that have NOT been added to the pool of levels, make sure they are prepared properly to be added to the pool of levels
- With the props that have ALREADY been made and are in-engine (including the ones that aren't textured yet), set-dress the levels

##### VFX

- [ ] Mikel Sienra

- More VFX.

##### UI

- [ ] Brian Rosario-Diaz

- I'll give you a list of UI things that need revision and better art

#### Artists

##### Env. Artists

- [ ] Rae Overton
- [ ] Erin Willie
- [ ] Austin Marmie
- [ ] Daunte Smith

- The wood texture
- Texture the existing props
- Make new props

##### Character Artists

- [ ] Azalee Nelson
- [ ] Mia Parent

- N/A

##### 2D Artists

- [ ] Alexandra Kotzeva
- [ ] Alexis Ibanez

- Finish up the remaining portraits
- Highkey, i need a background image

##### Animation

- [ ] Andre Powell
- [ ] James Draper

- Enemy animations

#### Narrative Designer

- [ ] Chelle Radcliffe

- End of floor dialogue
- Questions for the start of the game

#### Audio

- [ ] Matthew Cabrera

- Work on SFX
