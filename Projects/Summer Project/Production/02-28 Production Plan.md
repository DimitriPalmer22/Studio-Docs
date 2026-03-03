# 02-28 Production Plan

Let's say in about two weeks, I want these things to be in the game:
- A much more finalized and polished player attack system. Something we can show an 8 second clip of an have people asking "wait, what game is this?"
- Lowkey a change in art style / environmental design because our current setup is not as appealing as I think it should be. I want the game to feel more GRAND. I want to be able to show short cinematics of a blockout / level (with appropriate lighting, fog, and effects) and draw people in off of that ALONE.
- Once we start getting more content solidified, we should establish a rhythm for our marketing campaign. What types of things do we show? What *personality* do we want our content to have (is it super-cool, are we edgy, or are we laid back and chill?)? How often do we post? How do we keep engagement up between our main content drops?
- Develop a much cleaner and intentional presentation / UI styling for the game. This includes
	- cinematic bars appearing on-screen
	- revisiting the in-game UI bars
	- revising how the addendums appear on-screen when they activate.
	- the fonts we use for the game
	- overall menu styling
- A more data-oriented way of storing information for levels. This will allow us to more quickly and easily store information about which levels are in the game, where they belong, and what rewards are associated with them. For the most part, this is a Dimitri thing. (this will help remove some of the jank in our design process I swear)
- 

## Better Player Attacks

The player's attacks *can* feel even better than they already do, but we have to figure out:
- why the combat in existing references work
- how to apply those working strategies to our product

We have to *HARD FOCUS* on this before addressing anything else because the [Combat](<../Avernoth/Mechanics/Combat/Combat.md>) should be the main attractor of our game, and this is the base of that.

### Combat Demo Level

![Watch This!](https://www.youtube.com/watch?v=5PJRCz0t7yY&pp=ygUcZ2FtZSBkZXNpZ24gem9vcyBhbmQgbXVzZXVtcw%3D%3D)

In game design, it is common to have showcase levels w/ the main purpose of showing off a specific mechanic. These levels are usually very small, and they are designed to be the best possible representation of the mechanic they are meant to show off.

We should have one of these for combat. It should allow devs to easily change their current spells and change the current enemy they are fighting against.

*THIS WILL BE USED FOR DEVLOG CONTENT*

### Revised Attack Animations

In my initial assessment of how the attacks should feel, I was wrong about how many frames we would need for the animations to feel good. The current animations are *too short* to have any type of *weight* or real *expression* to them.

Furthermore, the current movement setup we have for attacks is a little janky. Yes, it works in moving the player to the enemies, but that is not ideal (or conventional) for games with combat like this. Typically, games with combat like this don't have the player move very much from their attacking position (UNLESS they are doing an attack that has the main purpose of relocating them). Any in-engine movement is supposed to be very minimal, with only small movements that are meant to help attacks connect if they are just barely out of reach.
- It should be noted that in games with LESS movement per attack animation, the individual attack animations are much more AOE focused.

### VFX

Lowkey, i want to try incorporating 2D textures / animations / flipbooks for hit effects rather than pure Niagara particles (no I'm not just copying Tenebyss, but they are a good reference). This will allow us to have more stylized effects and break away a little further from the traditional Unreal Engine look.

### SFX

Some of these sounds are pretty rough…

## Art Style / Environmental Design Update

As of right now, the 3D artists are idle, and I could have them do some major redesigning to the appearance of our current levels (in terms of the kits we use).

After looking at some other references, I realized that our spaces don't feel nearly as *OTHERWORLDLY* as they could. Our current levels feel too much like they can exist an any worldly fantasy setting. I want our levels to feel a little more like they have an air of mystery and danger to them.

[02-28 Production Plan Level Design](<./02-28 Production Plan Level Design.pur>)

### Proper Level Design Pipeline

We cannot be doing this right. As of now, the LDs are just freestyling levels in the editor with the REAL ASSETS.
- There is no iteration.
- There is no room for testing.
- There is no room for feedback.

BLOCKOUTS are our best friends. We should be using Unreal's modeling tools to create blockouts of our levels before using real assets (since I lowkey wanna get new assets anyway). This will allow us to iterate on our level design much faster, and it will allow us to get feedback on the design of the levels before we put in the time and effort to make them look good.

### BACKGROUND & SPACE

The background elements can be obscured by **fog**.

## Small Art Update

### Updated Model For Addendums Object (Anvil Thing)

We need to get rid of the anvil as the object the player interacts with to upgrade their tome. Instead, we will replace it with a special writing desk w/ a pen that has magical ink.

### Revise the Model for the Tome Altar

The shape behind the Tome Altar seems a lot like the symbol for the good guys. We should maybe replace it with the symbol for the bad guys.

## 2D Art & UI Stuff

The 2D art style for the game isn't as cohesive as I would want it to be. Also, there are a couple things that are still placeholder and haven't actually had a real artist's touch yet.

> NOTE: For ANY UI-related things that are full screen images, PLEASE PLEASE PLEASE *use conventional canvas sizes* (like 1920x1080 for 1080p). For any MOCKUPS that you send me (where you're demonstrating where the UI should go on the screen), PLEASE PLEASE PLEASE *use conventional canvas sizes*. Fullscreen elements that are not in a 16:9 aspect ratio cause so much more grief than you would think.

### In-Game UI

### Character Portraits

With the creation of the marketing materials and the overall aesthetic of the game's 3D elements (like props & character models), it is safe to say the character portraits don't exactly match the style / aesthetic of the game anymore.

The style of Allister in the Marketing Materials is a lot more in line with the style and tone of the game, so we should update the portraits to match that style.
- Much more dynamic pose
- More dramatic lighting

- FIND MORE REFS FOR AN IN-GAME PORTRAIT ARTSTYLE
- REMOVE DITHERING FROM CHARACTERS
- EXPLORE THE IDEA OF REMOVING A COUPLE CHARACTERS
- REFS FOR POSES? WHY DON'T OUR EXISTING POSES WORK?
- WE CAN EXPLORE MODIFYING THE EXISTING PORTRAITS WITH MORE 

### Allister Portrait Update

Allister's portrait is going to have to be updated to reflect his overall design change.

### Addendum Screen UI

## Narrative Stuff
