# Initial Overview

### Purpose Of Tome Questions
At the beginning of each run, I want the player to have a somewhat random starting loadout. (Loadouts consist of a primary spell, a secondary spell, and one or more passive abilities).

### The Implementation

#### Gameplay Effects
To do this, I came up with the idea of pretty much giving the player a "test" at the start of each run where they answer a series of questions. Each answer of these questions will give them a predetermined spell / ability.

#### Juice: Interesting Questions
To have this portion of the game feel engaging and fun enough to keep doing as the player starts new runs, I opted to make the questions have some personality. 

Having the questions be straightforward "What spell do you want?" seemed uninteresting and overall a waste of time. If the player knew what the resulting spell was, why would they ever pick an answer if another answer gave them an ability they liked???

#### The Process
To get these questions, the player walks up to these "*Question Interactions*" (For lack of a better term). When the player interacts with them, a question UI pops up with three possible answers. Each answer corresponds to a predetermined spell / ability.

# Working Through the Solution

## Problems

### Too Many *Question Interactions*...

#### Problem: Time Sink
Masahiro Sakurai explains that in games where failure is frequent, restarts should be quick to maintain user engagement. I agree. If it takes too long from dying to getting back to the main game, I would lose interest very fast.

The process of going from question to question is much too long, and isn't interesting enough to justify how much time it takes away from the main game.

#### Problem: Lackluster Presentation
There is no *big moment* with 3 question interactions. In terms of presentation, it is very difficult to give a specific moment where the player is empowered and they think to themselves "Ok, now the run starts!"

#### Problem: Level Design Complexity
In terms of dressing the level, having to place 3 separate question interactions is more difficult than just placing one. This adds unnecessary complexity to the level design process.

Also, leading the player to three separate question interactions and then the exit of the area is more difficult than leading them to just one question interaction and then the exit.

#### Alternate Idea: All Questions in One Screen
Instead of having the player go to THREE separate question interactions, I could have all three questions appear in a single UI screen. This would cut down on the amount of time it takes to get through the questions significantly.

##### Pros
- This is much faster
- Gives a single point where we can empower the player and say "Ok, now the run starts!" after they finish the questions
- Easier to implement in terms of level design

##### Cons
- UI Design is a little more complex, with the player spending a little more time in the question UI. How do we go from question to question visually?
- Can still feel like it takes too long to get through all the questions. Me personally, I might just click the first option of all 3 questions to get it over with.

#### Alternate Idea: One Question For An Entire Loadout
With loadouts being implemented within the project in the form of data tables, generating new predefined loadouts is very easy.

##### Pros
- This is the fastest option
- Again, gives a single point where we can empower the player and say "Ok, now the run starts!" after they finish the question
- Easiest to implement in terms of level design
- The current question system is a little labor-intensive. 
	- Having to come up with 3 questions with 3 answers each time is a lot of work. Also, the process of making the data objects for the questions is A LOT of work. A single data table with predefined questions, answers, and resulting loadouts is much easier to manage.

##### Cons
- Might feel a little uneventful if the player doesn't spend enough time making the decision about their loadout. "I did all that for one question? This ENTIRE room is for one question???"

### Too Much Content to Generate

#### Problem: Answer Assets are Cumbersome

For the current process of creating the questions, individual assets need to be made for:
- Questions
- The data assets that hold the information for which spell to give the player

This leads to:
- Organization issues
- A larger surface area for possible bugs

#### Problem: Simply Too Many Questions

With the vision I have for the game:
- there are a LOT of spells and abilities that the player can get
- I want there to be enough variety that the player isn't constantly getting the same set of questions over and over

In order to do that, I would need to create a LOT of question assets. This is very time-consuming and tedious.

Given the lack of time remaining for this project and how much content is actually gonna end up being in the final product, this is not a feasible approach.

#### Alternate Idea: Again, One Question For An Entire Loadout

Having a single question for an entire loadout would significantly cut down on the amount of content that needs to be generated.



### In Terms of the Narrative, How Are the Questions Being Relayed to Allister?

In the game, the questions are something Allister is actually answering, not the player directly. This raises the question of how Allister is receiving these questions.

#### Exploration: Through the Dialogue with an Ally

#### Exploration: Through the Question Interactable Itself

##### A REAL Idea: Pre-written Questions Left Behind by the Archmage

The Archmage, who used to work for the Empire long in the past, was conducting research on ways to quickly equip military mages with spells and abilities. To do this, he created these *things* that give out a quick personality test. This test then gives the test-taker a loadout based on their answers to the questions.

###### Okay. Why Did He Bring These Into Avernoth
The Archmage wanted to further his research, so he brought these devices into Avernoth with him. The loadouts given out by these were lacking in power (which explains why the starting tome alone is probably not strong enough to get you through the game), so he continued his research into generating upgradeable tomes with more powerful spells and abilities.

This is the idea we'll go with for now.

##### Another REAL Idea: The Books Start WITH the Questions
So imagine most of the points above.

However, instead of having some magical device that asks the questions, the tome itself has the questions written inside of it. When Allister picks up the tome, he reads the questions and answers them. The tome then magically enchants itself with the spells and abilities based on his answers.

##### Idea: The Question Interactable is Sentient
Straight up, I do NOT not like this idea. We'd have to do a little more characterization of the Question Interactable, and I don't think that fits with our production timeline.

### How Do I Come Up With What the Interactable Is?

#### Purpose: Create Tome w/ Loadout
Narratively, the reason this "question interactable" was originally created was to quickly equip underskilled mages with a loadout of spells and abilities. If we were to draw real-world parallels, it's similar to how the invention of guns vastly improved the effectiveness of soldiers with little training.

It should be noted that this question interactable is giving out a physical object in the tome. This tome contains the spells and abilities that the test-taker has earned through their answers to the questions.

#### Problem: Who is able to use this Magical Device?

We know for sure that whatever this "question interactable" thing is that is giving out the tomes is some kind of magical device.

##### Idea: Only Specific People Know How to Use It
The Archmage created this device for the Empire's military mages. Only people who have been trained in its use are able to operate it and create the tomes.

Pros:
- This allows us to justify why one of Allister's allies would talk to him before he uses the device, explaining how it works.
- This explains why the mage isn't too worried about just leaving the device lying around in Avernoth.

Cons:
- The narrative explanation for this is PIVOTAL, so we need to make sure we get it right.

#### Theming the Item
Things to consider when theming this prop:
- The "Question Interactable" spits out a tome, so it should probably be book themed
- The tome is enchanted, so it need to have clear indications that it is magical in nature
- Since this device is a modified version of the version created by the Archmage for the Empire's military mages, it should probably have some imperial design elements to it.
- Since this device is in Avernoth, it should probably have some design elements that fit in with the rest of the environment.

#### Problem: How is the Book Created?

##### Idea: Magical Creation
The tomes can be created through magical means. The "question interactable" device uses magic to create the tome out of thin air.

Pros:
- Gives us a clear "This is when the run starts" moment when the tome is created
- Can explain how these are used to quickly equip large numbers of mages
- Is easier to implement in terms of VFX
- The prop itself doesn't need to consider a whole bunch of books lying around it

Cons:
- Not sure

##### Idea: Physically-based
The object itself is already placed within a room with a stack of blank tomes. When the player interacts with the device, we can communicate that it enchants one of the blank tomes to create the starting tome.

Pros:
- Gives a clear physical representation of the tomes being created
- Can show the tome being enchanted in a more tangible way

Cons:
- More complex VFX
- The visual effect can really fall flat, as the tome model we have vs the plain books in the game look extremely different. It would be difficult to make the transformation look good.

### What Actually IS the Question Interactable?

#### Idea: A Summoning Circle
Rather than be some simple contraption the player walks up to and interacts with, the question interactable could be a magical summoning circle on the ground. 

The summoning circle can't just be a simple circle on the ground. It needs to have some design elements that make it feel more interesting and complex. Also, it needs to convey to the player that it is a magical device that creates tomes.

##### Possible Design Elements
- Arcane Symbols on the ground
- Piles of books surrounding it
- Floating magical runes above it
- Some type of floating magical crystal above it
- A "control panel" or something along those lines to clearly indicate that this is an interactable device.
	- Maybe have a book stand with an open book on it. This is where the questions are displayed.

##### Gameplay Implementation Details
The first time the player goes through the game, they can go through the entire process of seeing the tome be created.

However, on subsequent runs, the tome can just be there automatically. The player interacts with it to equip it, questions come up, and then the player proceeds.

#### Idea: A Magical Pedestal

Again, it can't just be an uninteresting pedestal on the ground. Instead, it needs to have some design elements that make it feel more interesting and complex. 

##### Possible Design Elements
- Arcane Symbols on the pedestal
- A floating magical crystal above / around it
- Floating magical runes around it
- A lectern with an open book on it. This is where the questions are displayed. The player interacts with this to create a tome on the pedestal, which they then pick up automatically.

#### Idea: A Super Magical Bookshelf

So this idea is a little different. Instead of being a single interactable device, the question interactable could be a magical bookshelf filled with these *special* blank tomes. 

The player walks up to the bookshelf and pulls a book out, which triggers the question UI to appear. After answering the questions, the tome is enchanted and the player automatically picks it up.

> Note: This is relying on the idea that the tomes themselves contain the questions.

##### Maybe Not
- Wouldn't this mean that the player would eventually run out of books to choose from if they kept restarting runs?
- How Do You Make A Bookshelf Look Interesting At First Glance?
- We would need an animation specifically for pulling the book out to prevent the game from looking too cheap.

##### Possible Design Elements

# Coming Up With More Questions

### Idea: Themed Questions
- All answers give the same / similarly themed passive spells
- All answers give 