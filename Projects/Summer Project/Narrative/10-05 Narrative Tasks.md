
## You Said you wanted to show me something Paul Made in Regards to the Portal?
yeah ^
# Things That Should Probably Be Addressed Sooner Rather than Later

## Changing the Way we Think About Dialogue
My intention was for this game to have a narrative that was interesting enough to keep players invested in the world and characters while they played the game. Not just because I wanted to make a good game, but because I also wanted to give you a chance to show more of your writing. But, if we want to do that, then we have to make sure we give the narrative as much love as the rest of the game.

I've got a couple concerns with how the dialogue is currently implemented:
- Interrupts the flow of gameplay w/out feeling significant
- A little difficult to follow the story because there hasn't been any real plan on how to intentionally present the story to the player

### Important Dialogue vs. Fluff Dialogue
Not all dialogue is created equal, and we shouldn't try to present all dialogue the same way. I think it'd be beneficial to think of the different types of dialogue in our game in two separate ways:

#### Important Dialogue
- Important dialogue is stuff that the player really needs to know in order to understand the story, the world, or their character. 
- There should be a clear indication to the player that this dialogue is important or at least more significant than other dialogue.
	- Kinda like how in a lot of RPGs, dialogue lines from important quest lines are usually voiced, but lines from side quests or random NPCs are usually not voiced. The player knows to pay more attention when they hear a voice.
- I might even consider making these *UNSKIPPABLE* or something
- For these, it'd probably be best to map out all the important information we want Allister's allies to convey to him
	- For example, entering a new area of Avernoth for the first time, encountering a journal table for the first time, etc.
- Also, the way I see it, *important dialogue interactions* should be delivered as feedback for the player's actions and should acknowledge what the player is doing.
	- Ex: The player encounters a journal table for the first time -> Allister's allies explain the significance of journal tables in Avernoth
	- Ex: The player enters a new area of Avernoth for the first time -> Allister's allies explain the significance of this area in Avernoth
	- Ex: The player enters a "boss room" for the first time -> Allister's allies explain that "the mana here is more dense" or something
- The reasoning behind the feedback idea comes from a video I watched from Masahiro Sakurai, where he explains that action games should always have some type of feedback for button presses. I think the same type of reasoning can be applied in this scenario.

#### Fluff Dialogue

- Fluff dialogue is stuff that adds flavor to the world and characters but isn't strictly necessary for the player to understand the story.
- This is the type of stuff that can be skipped if the player isn't interested in it.
- The dialogue interactions that randomly spawn at the ends of rooms are probably best suited for this type of dialogue.
- Although they should still somewhat follow the principle of acknowledging the player's actions, they don't need to be as strict about it.
	- Ex: The player clears a room -> Allister's allies make a joke about how easy that was OR talk about how it relates to their pasts

### Updating How Allister's Allies can Communicate w/ Him
Right now, dialogue portals spawn in two situations:
- At the end of a room AFTER you clear it
- In pre-determined places like the upgrade room

This is *boring and limited*. It also begs the question, "Why do portals only spawn in these places?" I don't think we have a real reason for it (other than it being easy to implement at the time I was making the dialogue stuff).

#### New Portal Spawn Opportunities

I think it'd be a lot better if we were more *flexible* and *dynamic* with how we allowed Allister's allies to communicate with him.

For example, let's say this is the player's first time encountering a journal table. As Allister approaches it (before even interacting with the table), the player is forced into an *important dialogue interaction* detailing the significance of the journal tables in Avernoth. This way, the player understands why they should care about the journal tables before they even interact with one. 

As for how this would be represented visually, we could probably have a mini portal appear from Allister's tome or on his shoulder or something.

This would effectively help w/ two separate problems:
- Finding a way to *dynamically deliver story content* to the player
- Finding a way to *tutorialize information* within the game's narrative

#### Rethinking the "Room Clear" Portal Spawns

- As it is right now, portals sometimes spawn on the room's exit portal. The player cannot leave the room without interacting with the dialogue portal first. 
- This is kinda annoying because it forces the player to stop and listen to whatever Allister's allies have to say, even if it's not important. This leads to players who don't care skipping all dialogue, which is not what we want.
- Instead, I think giving players the choice to engage with the dialogue portals would be a lot better.
- It might be a good idea to have the portal spawn on Allister's tome or shoulder and have it indicate that the player can interact with it if they want to.

### Avoid Long Unbroken Conversations
- One thing I've seen a little of through playtesting is just how little tolerance players can have for long portions of dialogue
- Considering the fact that this game is targeting an audience that is more invested in the action of the game than the story, I think it's important to keep this in mind
- So, what do we do?

### Give the Story to the Player As They Go
- With just a little bit of movement or action in between these conversations, players seem to be a lot more willing to sit through them.
	- For me personally, It's kinda like being more willing to watch 3 20-minute YouTube videos vs. a single 1-hour YouTube video.
- This is one of the main reasons why I'm inclined to split the starting sequence (Wake up & read dialogue -> answer questions for spells) into more than 1 room. It gives us more opportunities to break up the dialogue into smaller chunks.
- In Hades, if you spawn in and want to immediately start a run 
	- The pool Zagreus wakes up in (where you talk to Hypnos)
	- The little area with Hades
	- The little area next to Zagreus's room (that has Nyx somtimes)
	- The bedroom
	- The training area
	- And THEN the start of the run
- During all of these points, there are opportunities for Zagreus to have conversations with the other characters or even make remarks to himself.
- I'm not saying we need to go this far, but I do think it's worth considering *breaking up the starting sequence into more than 1 room*.

## Questions @ the Start of each Run
I want to rework how the beginning of each run works a little bit due to some feedback I got when I got the designers to play the game.

### The Way It Is Currently
![](<../../../_Meta/Attachments/Pasted image 20251006034311.png>)

- The intro to the game feels very dense right now.
- With the introduction dialogue AND the questions back to back, there is a lot for the player to take in all at once and not much time to breathe.
- Also, the layout of the room doesn't lend itself well to the flow of the sequence. Having to turn around after answering the questions to leave the room is a little awkward.

### The Way I Want it To Be

![](<../../../_Meta/Attachments/Pasted image 20251006035357.png>)

- The player starts their run in the "starting room".
- After the screen fades from black and Allister wakes up, a dialogue portal spawns in front of him.
- The player interacts with the dialogue portal to hear the main portion of the introduction dialogue.
- The player then leaves the room through the exit portal.
- The player enters the "question room". *This is an opportunity for more dialogue.* Something short, though.
- The player approaches the question rune and answers the questions.
- They then leave the room through the exit portal.
- The player enters the first room of the run. Loading in the first room of the run is *another opportunity for more dialogue*. Again, something short.
- Considering that the player has to go through this sequence whenever they restart the game, *we want restarts to be quick*. Get the player back into the game as quick as possible while keeping the narrative within the flow of the game.

## Journal Tables
Right now, the implementation of the journal tables feel... underwhelming. Players walk up to it, read a note, and that's it.

### Allister Should Say Something
- After reading the note, having a forced dialogue interaction would be pretty rad.
- The dialogue interaction should acknowledge the contents of the journal entry.
- It might be best for Allister to monologue here. The allies are supposed to be in the middle of a war or something. It wouldn't make too too much sense for them to actively be reading along with him.

### Giving the Player Something To Work Toward
- Also, a cool little psychological thing I wanna try is giving the player a goal to work toward. Having a popup like *X journal pages found* after reading a journal entry would give players  
- Players might want to learn what happens when all the journal entries are found.

## What Exactly Should We (You lol) Do?

Tackling how we want to approach delivering the narrative to the player should take priority over anything else.

### The Intro Sequence
- The main bit of feedback I got about the initial intro dialogue is that it's way too long.
- When reading it straight up, it looked fine, but having to click through it all at once was a lot.
- I think if you wanted to skip through all the pieces of dialogue

# Things that Are Not a Priority

These are just some things you can keep in mind for later. If you have an idea or suggestion randomly, you can hit me up about it. 

## Area Names?
Every time Allister enters a new area of Avernoth (the areas are separated by the "boss rooms"), a title card appears in the middle of the screen for a few seconds, showing the name of the area. I'm ngl I have absolutely no idea what to do with these.

![](<../../../_Meta/Attachments/Pasted image 20251005224813.png>)

### Area 1

### Area 2

### Area 3


## Tutorial Stuff
I wanna start considering all the brand new concepts and content the player is encountering as they play the game. It's kinda hard for me to do this because I've been working on the game for so long that I forget what it's like to be brand new to it. So, I might need some insight here.

### Intro Room

#### Introduce the Dialogue Portal
- One thing I think would be a nice touch is having the dialogue portal spawn in the intro room a teeny bit after the screen fades from black.
- This draws the player's attention to it and makes sure they don't miss it.
- Maybe the initial room should be pretty simple so the player can focus on the dialogue portal.

#### Getting to the Questions
- Getting the questions should be more of a grand occasion for the player.


#### The Exit Portal
- The exit portal should not be available until after the player answers the questions.
- It should also appear in a position where the player would naturally be facing anyway
- Positioning the exit portal near a landmark that would naturally draw the attention of the player would be a good idea.


### Beyond the Intro Room