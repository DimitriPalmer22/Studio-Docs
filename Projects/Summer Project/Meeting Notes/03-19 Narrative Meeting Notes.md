# 03-19 Narrative Meeting Notes

**Main goal**: Flesh out the journal-related dialogue for "chapter 1" of the game.

## Major Changes to the Presentation of the Game's Narrative

### Pre-determined Journal Entry Order

> See [Linear Narrative](<../Avernoth/Narrative/Linear Narrative/Linear Narrative.md>) for more details.

Journal entries used to work a little differently before.

BEFORE, there would be a pool of active journal entries. The player would collect a random journal entry from this pool whenever they encountered a journal table. However, this made it a little difficult to create an engaging story that was also easy enough to follow and write for.

NOW, the order in which the player encounters these journal entries is pre-determined and fully linear. This way, we can have the dialogue of characters reference details in previous entries they found without having to worry about whether the player has actually encountered that information yet.

### "Chapters"

> Again, see [Linear Narrative](<../Avernoth/Narrative/Linear Narrative/Linear Narrative.md>) for more details.

For organizational purposes and also as a way of regulating the player's progress, we are dividing the game into 3 *chapters*.
- Note: This is purely on our (the devs') side. There will be no screen saying "chapter 2" or anything like that.

The player progresses through each chapter by collecting the Journal Entries that correspond to that chapter.
- For example, chapter 1 has 3 journal entries and 2 experiment logs. The player completes the chapter once each of these entries is completed and the player reaches the end of Avernoth to "deposit" these journal entries.

The final journal entry in each chapter will *ALWAYS* be an **experiment log** basically telling the player to tamper with the seal at the end of Avernoth that is keeping Allister trapped inside. So, once Allister tampers with this seal 3 times, he escapes Avernoth.

### Dialogue Surrounding Journal Entries

With the changes made to ordering the journal entries, the journal entries are now one of the main things we have to consistently communicate the game's narrative. Furthermore, with the *quests* that are associated with the experiment logs, the game's narrative is even more closely tied to them.

As a result, I'd like to focus a little more on the dialogue surrounding the journal entries:

- *Response dialogue*: **EVERY** journal entry (standard journal entries AND experiment logs) must have some *response* dialogue associated with it. This means that upon collecting and reading a journal entry, some character must say something about what the player just read.
- *Completion dialogue*: Every **EXPERIMENT LOG** must have dialogue associated with completing the objective. The quests associated with these journal entries are no longer just going to be "reach x room with y spell equipped." The player must actively interact with some element to "recreate an experiment". The dialogue must be in response to that.

## Testing the Dialogue

I remember at some point a couple months ago, you mentioned that there isn't really a way for to test the dialogue in-game without playing the game yourself. This has been remedied.

### Narrative Demo Level

I have created a level strictly for testing out any narrative / dialogue / quest stuff. It's called *L_Demo_Narrative*. The level is set up so that editing it should result in very few merge conflicts if any ever. So, feel free to edit some things for the sake of testing out the game's narrative.

It can seem a bit intimidating at first, so here's a quick overview:

Currently, there are 3 stations in this level:
- The quest area - a little area to test the minigames and such associated with the quests
- The dialogue area - a simple space for testing specific conversations
- The journal table area - an area focused on testing journal entries

#### Quest Area

This is *mainly* for me, as it is used for testing out the mechanics of a quest to see if it functions properly. However, you (I'm assuming the narrative guy is reading this) can also use it to test the dialogue you encounter after completing a specific quest.

As of right now, it only contains the quest minigame for Pool01_Log01.

#### Dialogue Area

This is probably going to be the most useful area for you. When you step on them, the blue pads on the ground will play a specific dialogue interaction. Within the editor, you can set them up to play any interaction you want, so edit them to your heart's content.

#### Journal Table Area

This is also going to be pretty useful for you.

The journal table spawns the "next" journal entry at the time of loading the level. This depends on the user's save data, so you may need to walk over the save / load pads to change which entry spawns in.

When walked over, the pink pads make you collect a specific journal entry. So, these are probably going to be much more useful than the table would be. In the editor, you can change which entry is spawned by the pad, so edit them to your heart's content.

### Debug Menu

A quicker tool you can use in *any* level is the **Debug Menu**. You can open the debug menu by pressing **H**, and you can dock it anywhere or even drag it to another monitor. It'll even stay open after stopping your play session.

I'm not going to lie, this is probably going to be much more useful and quick to use than the level I set up specifically for the narrative. But, you have the option to use either.

This debug menu has buttons and dropdowns for testing most features in the game. However, you'll probably focus more on the dialogue section.

![](<../../../_Meta/Attachments/Pasted image 20260319181017.png>)

This section contains:
- a dropdown to load specific save data
- a button to clear your existing save data
- a dropdown to play a specific dialogue interaction
- a dropdown to open a specific journal entry
- a button to force the journal table in the current room to spawn a journal entry
- a dropdown to collect the "item" associated with a quest

## Implementing & Updating Dialogue

The setup for the dialogue system in the game *should* be fully complete (barring any additional improvements we want to make). It is also *completely* different from how it was before, so most documentation on that is obsolete.

## Task: Fill out the Ch Dialogue For the Journal Entries
