One of the main issues I had with Relapse is how unplanned things felt. There was never a point where I felt like I could look 2 weeks in the future and would know what exactly everyone would be working on and what the game would look like. As a result, several issues kept appearing:
- Scope creep
- Established ideas kept changing because of new content
- Content kept getting added to the game right before deadlines, which led to a lack of polish for some things.

I want to avoid this with the new game. I want to have a clear idea of what the game will look like, how it will play, and what the scope is. This way, at the start of each week, I can plan out everything that needs to be done in the near future.

ChatGPT prompt for developing a proper production structure / pipeline:
## Prompt
I am currently leading a team of game developers, and the game we are currently making is in the early stages of development. I want to make sure that we have a solid production structure in place to ensure that the game is developed efficiently and effectively. It should be noted that our team has no dedicated producer.

I have an idea for how I can properly structure the tasks and workflow of the team. The idea is as follows:

- The game is divided into *features*. Each *feature* is a major part of the game that needs to be developed. Features do not necessarily need to be mechanics; they can also be things like *art* or *sound*.
- Each *feature* of the game is clearly defined and outlined by the team lead. This *outline* contains a clear text description as well as photos / videos of what the feature should look like. These outlines are then sent to the team members who will be working on the feature.
- The *outline* for each feature contains a list of related tasks that need to be completed in order to finish the feature. These tasks are then assigned to the team members who will be working on the feature.
- Each *task* has a *minimum acceptable standard (MAS)* that goes with it. This is basically an explanation of what the bare minimum is that needs to be done in order for the task to be considered complete. This is important because:
	- it allows the team members to know exactly what is expected of them
	- helps to avoid scope creep
	- allows us to be comfortable with what we have and avoid goldplating
- Each *task* has a *due date* that is set by the team lead. This due date is based on the overall timeline of the game and the deadlines that we have set for ourselves.

What can be improved about this structure? What are some things that I should consider when implementing this structure? What are some potential pitfalls that I should be aware of?

# Feature Outline Structure

## Feature: FEATURE_NAME
### Description
This is an example description of what the feature is. Here, we describe:
- A general overview of the feature (short summary)
- Why the feature is important. What is the context of the feature within the game's overall design?
- How does the player interact with this feature? Is it a mechanic they directly interact with? Is it an art asset that they see up close? Things like this help contextualize the feature for the developers.

### Tasks

> Note: Some tasks depend on others. It might be a good idea to make some type of dependency graph or use a topological sort of some kind to understand which things need to be done asynchronously or sequentially.

#### Task_NAME

##### Task Description
This is an example description of what the task is. Here, we describe:
- A general overview of the task (short summary)
- Why is this task important? How does this task fit into the context of the feature?
- How do other tasks relate to this task? Are there any dependencies? Is it a prerequisite for other tasks? Does somebody else need this done first in order to do their task?
- What is the expected outcome of this task? What does it need to look like when it is done?

##### Task Quality Standards
This is an example description of what the quality standard is for this task. Here, we describe:
- Level 1 - Minimum Acceptable Standard (MAS): What is the bare minimum that needs to be done in order for this task to be considered complete? This is something we are *comfortable* putting into the game, but definitely needs some type of improvement or iteration. Things at this level should only stay in the game if time becomes a concern.
- Level 2 - Preferred Standard: What is the preferred standard for this task? This is something we are *happy* putting into the game. Things at this level should be polished and ready to go. This is the standard we should be aiming for.
- Level 3: Anything at this point should be considered goldplating. This is something we are *proud* to put into the game. This is something that we should be aiming for, but if we don't have time, it is okay to leave it out.
