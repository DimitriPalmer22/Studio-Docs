# Important Notes

### Dialogue Test Level?
For the sake of letting you get a feel of how the dialogue you write will look & feel in-game, let me know if you want me to set something up. It'd be very easy and quick for me to do.

### I Have *Very Slightly* Changed How to Add New Dialogue!
- [I have updated the relevant information on this page](<../Mechanics/Using the Dialogue Interaction System.md>)
- Literally everything should be the same except:
	- the very first step of creating a dialogue asset
	- the naming convention for the dialogue assets

### Rich Text
- The rich text implementation is still a little jank, so it isn't exactly ready for use yet.
- However, it'd be pretty useful if you though of a couple specific things you'd want to use rich text for to make the dialogue more expressive (e.g. bolding certain words, changing the color of certain words, etc.)
- I'll see what I can do to get those in.
- One thing for sure I want to look into is making people's names very obvious (italicizing, bolding, changing color, etc.). We should pick one of these and stick with it consistently.

# Rewriting Some Old Dialogue 

Here are a couple interactions that I think need to be rewritten or at least broken up into smaller chunks. There are probably more, but I'll have t

### Beginning Dialogue

> Note: Literally as I was writing this, I realized I *still* need to modify the implementation of the dialogue system specifically for the beginning sequence (respawning & getting very specific dialogue at very specific points). So, this will need to wait a *little* longer.

### DDI_EnchantAristide1
This interaction takes place in the upgrade room. It feels pretty long for an interaction the player MUST go through to get an upgrade. 

This interaction has 14 lines whereas the other upgrade room interactions have 7-8 lines.

I wanna try this idea: Instead of thinking about the length of these interactions in terms of the total number of words, try to *also* think about the *total number of inputs* the player would have to make to get through the interaction if they were reading it in-game.

Me personally, instead of letting the text write all the way out, I press the `confirm` button to quickly finish the current line of text. Then, I press `confirm` again to move onto the next line of text. So, the number of inputs I need to get through the interaction as quick as possible while still reading everything is 2x the number of lines of text. 

### DDI_MagnustFirstDeath2

> Again, I'll need to wait on this one until I modify the dialogue system to better accommodate the beginning sequence.

This is the interaction that plays when Allister dies and resurrects for the first time. This DEFINITELY needs to be broken up. It's 27 lines long.

# Writing New "First" Dialogue

- The player's first run isn't going to be scripted or anything, but there are several key interactions the player must go through. 
- All of these interactions are mandatory, so it is very important to not make them too long.

### Entering a Standard Enemy Room for the First Time
- Condition: Upon loading into the first standard room of the run (so, any room after the beginning room(s) of the game)
- Description: A quick interaction should play out explaining that there is imminent danger. After this, the player regains control, walks deeper into the room, and fights enemies.

### Clearing a Room for the First Time
- Condition: Upon defeating all enemies in the first standard room of the run (so, right after the above interaction)
- Description: A quick interaction should play out explaining that the player has cleared the room and can now proceed to the next room. They'll probably need to keep doing this to escape.

### Encountering a Journal Table for the First Time
- Condition: A journal table randomly spawns in one of the rooms. This interaction plays once the player walks within a certain distance of the journal table for the first time (This interaction will only play if the player has cleared the enemies in the room).
- Description: One of Allister's allies (idk maybe Tarun? He seems like a book kinda guy) points out the journal table and the note on it. The player then walks over to the table and reads the note.

### After Reading the First Journal Entry
- Condition: After reading the first journal entry and closing the journal entry UI (This interaction plays immediately after the above interaction)
- Description: One of Allister's allies briefly informs him of the mage who wrote the journal entry. However, not much is known about this mage. Perhaps we can find out more.

### Entering the Upgrade Room for the First Time
- Condition: Upon loading into an upgrade room for the first time
- Description: Allister is confused by the sudden change in scenery. One of his allies is like, "it looks like this is a place where we can upgrade our abilities. Let's see if we can find anything useful here." The player then regains control and (hopefully) interacts with the table to upgrade abilities

> Note: There is a chance this "table" becomes a "magical workbench" or something based on future art assets.

### Interacting with the Upgrade Table for the First Time
- Condition: Upon interacting with the upgrade table for the first time (before opening up the upgrade UI)
- Description: Allister explains that he isn't exactly sure how to use this table. One of his allies responds with "Don't worry, I got you. You can spend mana essence here to upgrade your abilities. I'll walk you through the process."

### Encountering A Shop Room for the First Time

***Let's hold off on this one for right now.***

- Condition: Upon loading into a shop room for the first time. 
- Description:
- Note: The shop room ALWAYS spawns after the upgrade room (not immediately after, but it is guaranteed to spawn at some point after the upgrade room). So, the player will have already gone through the above two interactions before this one.

### Entering a "Boss Room" for the First Time
- Condition: Upon loading into a boss room for the first time
- Description: 

### Clearing a "Boss Room" for the First Time
- Condition: Upon defeating the waves of enemies in a boss room for the first time
- Description: Hidetomo comes to talk to Allister (Assume this is our first time meeting him). Hidetomo remarks that although Allister has made decent progress, there is still no hope of escaping Avernoth.
