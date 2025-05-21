
# What Are your Tasks?

- Create a modular kit using Unreal primatives and modeling tools to find a good balance between granularity and ease of use
- Create at least 2 level blockouts 

If you want to see what I did for a modular kit open the "KitSizeTest01" Level in ``
- Here, you'll see a small gallery of the simple modular pieces I put together.
- Also, I made a room using these pieces.
- I color-coded the pieces to make it easier to see how they fit together.

# What is the Game Plan?

1. Create a very very basic modular kit. This kit should include several different types of wall, floor, and ceiling pieces.
	1. In terms of wall pieces, think of flat sections, doorways, windows (possibly), inward and outward corners, and so on.
	2. In terms of floor pieces, think of flat tiles, stairs, and so on.
	3. In terms of ceiling pieces, think of flat portions, portions that go up to create a slope, and so on.
	4. These pieces should be modular and should snap together easily so you can quickly build out a room without having to worry about the pieces not fitting together.
2. Using the modular kit you just made, create a very basic room.
	1. We'll be using these basic rooms to test out how effective the modular kits are
	2. We'll also use these rooms to determine how the rooms themselves should feel within gameplay
		1. Is the room big enough for the player to move around and effectively engage in combat?
		2. Would the room *still* be big enough once we add props to the room (tables, chairs, bookshelves, etc.)?
3. If you're comfortable with how the room looks, how the room feels, and how easy it was to create the room, then we can move on to the next step.
4. Let someone else (preferably another level designer) review what you've put together.
	1. Make sure whatever branch you're working on is currently public
	2. Ask for someone to check out the level you've been working on (let them know what the file's name is). Idk, if some people are currently in the discord in a call with each other, then maybe they can check it out together.
	3. Wait for feedback
5. Once, we've done this a couple times, we *should* have a set of modular pieces we're comfortable with.
6. We'll then send these pieces to the artists to create ACTUAL models for these pieces
7. The designers will then go back in-engine to replace their temporary pieces with the actual models. At this point, we'll have actual levels!

# What Needs to Be in the Kit?

### Floor Pieces
- Flat floor sections
- Pieces that create minor changes in elevation
- Anything else you think is necessary / would make the level design more interesting

### Wall Pieces
- Flat wall sections
- Inner corners
- Outer corners

### Ceiling Pieces
- Flat ceiling sections
- Ceiling sections that create minor changes in elevation

### Adding Extra Detail to the Pieces

- I don't want each floor, wall, and ceiling piece to be a completely flat box. This will look extremely visually uninteresting even with the most detailed textures.
- Even though we are targeting a PS1 type of art style, I still want some level of modern visual fidelity.
- So, I was thinking of adding things like beams and mouldings to the pieces. This will help break up the flatness of the pieces and add some visual interest.
	- It should be noted that these beams and mouldings should be simple and not too detailed. We want to keep the PS1 style, after all.
	- We should be able to accomplish this while keeping the poly count low.
	- IMPORTANT: Make sure that when these pieces are tiled together, no parts of them are overlapping / causing z-fighting issues.

> NOTE: I already have some optimizations in mind. There should only ever be like 1-2 rooms loaded at a time, so the object count in the level should never be that high. Also, since we're using low-poly assets, the poly-count should never be that high either. So, try not to worry *too* much about performance.

# What Are the Rooms Supposed to Look Like?

Basically, I imagine the rooms being made of stone and wood. Generally, I want the rooms to feel like they belong in the study of a magician who is in the process of losing his mind.

Here's the PureRef I sent to the artists for environmental art if you haven't seen it already. It has some more details about how I imagine the rooms looking.

![](<../../../_Meta/Attachments/Pasted image 20250521015148.png>)
