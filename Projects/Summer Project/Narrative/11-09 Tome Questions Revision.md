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
The Archmage wanted to further his research, so he brought these devices into Avernoth with him. The l

##### Idea: The Question Interactable is Sentient
Straight up, I do NOT not like this idea. We'd have to do a little more characterization of the Question Interactable, and I don't think that fits with our production timeline.

### What Actually IS the Question Interactable?