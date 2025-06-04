
### The Task

2 Dialogue Interactions for this week:
- written out first for feedback
- once approved, they should be implemented in-engine

Due Sunday.

### The Dialogue

I like the idea of having dialogue where the player talks to a specific ally for the first time. However, depending on how this is written, both keeping the writing consistent and implementing the dialogue in-engine could be a bit tricky.

To elaborate, let's say the dialogue is written in a way where Allister is unaware of a specific ally being able to talk to him. For example like he doesn't yet know that Tarun can speak to him while in Avernoth. EVERY single dialogue interaction with Tarun would need some flag to check if Tarun has introduced himself yet. This could be very tedious and is very error-prone.

Not only this, but any mention of Tarun in the dialogue would need to be checked to see if Tarun has introduced himself yet, which would make writing the dialogue a bit more complicated.

I think an easier way to write the dialogue would be to have some type of forced interaction during the first run where it is conveyed that all of Allister's allies can speak to him. This way, the dialogue can be written more freely and implemented more easily.
- Idea 1: Magnus just tells Allister "hey, all of these guys (list of allies) can talk to you too"
- Idea 2: A group interaction where everyone introduces themselves to Allister in a single dialogue interaction.
If we do it like this, then I think it would make sense to have this interaction after completing a room.

*Which one do you like better?*
- To me, the first idea feels kinda meh, but then the introductory interactions with the other allies would really feel like the first time the player is talking to them.
- The second idea seems cooler to me. I really like the idea of even having multiple people included in a conversation at once. Any "introductory" interaction beyond that would be less introductory and more like "this is the first time we're talking one-on-one"

### A Note about Implementing In-Engine

On one of my own branches, I am completely reworking the dialogue, so DONT DO ANY DIALOGUE STUFF IN-ENGINE YET. The work you do will probably be erased.

I am converting the blueprints I used for the dialogue system to C++ (because I absolutely can't stand blueprinting), so it's under construction for rn.