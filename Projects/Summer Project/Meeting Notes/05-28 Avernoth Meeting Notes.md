
After a couple weeks of development, to me, it's starting to feel like we're finally getting the ball rolling. Things are starting to take shape and I'm starting to see how this concept can eventually turn into a full-fledged game.

# Where Should the Game Be by the End of the Week?

With that being said, there are still a few things that need to get done before we have a basis for what the game needs to be. Therefore, we need to focus on the following things:

### Goals

- *In-engine implementation of the PS1 / low-poly art style*. We need to see what works, what doesn't work, and what needs iteration. We need to see what the game looks like. This doesn't just mean artwork; this also means level design things as well. I want us to have a good idea of the game's vibe.
- *A very basic demonstration of the gameplay loop*. This means that we need to have the player able to move around, interact with objects, and have some basic combat mechanics. For right now, rather than focusing on how the game *feels*, we'll focus on what exactly is happening in the game.
- *A simple implementation of the game's narrative*. This means that we need to have some basic dialogue interactions in-engine so that we can see how the narrative will flow and how the player will interact with it.

### Level Design

I want at least *1 fully realized level in-engine for POC*. By "fully realized," I mean that the level should have:
- An established modular kit that isn't just placeholder pieces. These should be actual textured models.
- Props placed in the level (that should also be modeled and textured)
- A basic lighting setup that gives the level a good atmosphere. We can worry about lighting optimization later. For now, we just need to see how the lighting looks in-engine.
	- Note: the global illumination setting in the scalability options vastly changes the appearance of the level.

For POC, this one level is going to be the level that Matthew created. This is because it:
- has the most complete modular kit
- has the most props already in-engine
- has the basis a lighting setup that gives it a good atmosphere
	- Still needs more ambient lighting though

### Art

Now that we have a better idea of what exactly needs to be in the game, we can start getting real art assets.

#### Environmental Art

I want enough of the props / modular kit to be modeled & textured so that we can put together a level that doesn't have any placeholder pieces in it. Once we get these, we'll essentially have the basis for the game's art style.

#### Character Art

Ideally, we would have the main character modeled and rigged by the end of the week. But if we can't get that due to it taking too long, I at the very least want the MC's model in-engine so we can get a feel for how he looks with the rest of the game's art.

### Programming

Not all of the game's core mechanics will be implemented by the end of the week. But, I want enough things implemented so that if someone wanted me to describe the game and how it works, I could show them a video of the POC build of the game and walk them through what is happening.

# What Are the Tasks for This Week?

### Level Design

Using Matthew's props and modular kit, make another level. However, try to make the level shaped different from Matthew's level.

##### Why?
- Although I like this modular kit, I still need more confidence that it is suited to creating a wide variety of unique levels.
- Also, I need to make sure all the level designers are comfortable with the process of using these pieces to create levels that suit the game.

### Art

- Go down the list of props. Generate models in accordance with the art style. Then, texture them.
	- Just to clarify, when it comes to making models, the placeholder assets are mainly for basic size and shape references. If the placeholder asset itself doesn't fit with the art style (like with any circular piece), then you should ensure the new model you make fits the art style
- Do the same thing with the modular kit pieces.

For the sake of organization, we'll make a list of the pieces in the ClickUp so that you guys can check them off as you finish them and also assign them to yourselves so everyone know who's working on what.

### Programming

This week, I've already:
- Made very basic spells that look VERY rough but can do damage
- Made dummy enemies that can be damaged and killed

The main things I need to do are:
- Make a system that detects when the player has cleared a room of enemies
- Make a system that plays the correct dialogue interaction based on the current state of the game

One thing I also wanna do, but don't know if I'll have time for is making a system that will load the next level whenever you complete the current one. This will essentially allow us to have a basic gameplay loop that we can iterate on.

# Other Stuff I Wanna Say (Outside the Game Itself)

### In-engine Resolution Scale

Something I noticed whenever someone would share their screen while working in-engine was that the game was really blurry and lowkey headache-inducing. This is NOT the post-processing's fault (at least it shouldn't be).

To fix this, click the three horizontal lines in the top left corner of the viewport, click "screen percentage" and then set the screen percentage to 100%. This is what the game ACTUALLY looks like.
- Warning, this will take more GPU resources, so you may lose a couple frames when working in-engine
- If your computer blows up, don't blame me

![](<../../../_Meta/Attachments/Pasted image 20250528050710.png>)

### Update on the Roles

I don't know if you guys noticed, but during the first couple weeks of development, I was all over the place. I was completely overwhelmed because I was trying to do too many things at once in terms of creative direction, production, and working on the actual game. Because of this, the project was suffering:
- Creative direction was definitely unclear at times
- Production was lacking / people didn't really know what they should be doing
- I couldn't do my individual work on the project as much as I wanted to

So, about a week ago, I decided to rely on the team more and divvy up my responsibilities a little bit better. To be specific, here's what changed:
- I started leaning on the producers, Andre and Leo, a lot more. They've been helping me a lot more with task creation and making important decisions about the short-term direction of the project.
- I've been relying on Chelle more for creative director-type stuff. They're pretty much a co-creative director. I try to run ideas by them to make sure things make sense. In terms of directing and giving feedback, I trust and respect their opinion, and I usually agree with it.

Also, Mikel is the lead level designer. So, once he's up to speed, you should also be able to look to him for level design-related feedback.

### Polls

- MC designs.
- Meeting frequency.
	- It's really hard to understand what's going on with the project, especially since we kinda have 2 halves of the team that don't talk to each other too often.

### Anything Else?

- Expect a google form some time next week for a post-mortem.
