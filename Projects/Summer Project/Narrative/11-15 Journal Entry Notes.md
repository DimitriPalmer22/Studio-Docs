# Quick Journal Entry Overview
- There was once an Archmage who worked for the Musarun Empire
- He made spells and other technologies that allowed the Musarun Empire to conquer many lands
- However, he slowly became more paranoid and delusional, fearing retaliation
- Overcome with guilt and the fear of retaliation from those he helped oppress, the Archmage created a new dimension to hide away in: Avernoth
- He fled to Avernoth, hoping to find peace and solitude.
- Avernoth was made to be a confusing disjointed labyrinth in which the Archmage could never be found
- As the Archmage lived in Avernoth, he slowly descended into madness
- He began to document his thoughts and experiences in a series of journal entries scattered throughout Avernoth
- It is through these journal entries that we can understand the Archmage's descent into madness, as well as how to escape Avernoth

# Journal Entries Are BORING!!!
- Although journal entries are tied to the progression in the game, they are still lackluster.

## Even Getting A Journal Entry Should Be an Achievement

### Goal Oriented Approach
- Instead of having the journal entries appear randomly in each area once per area, we should make the player actively pursue collecting the journal entries.
- Each journal entry (aside from the first one) should have a goal associated with it that the player must complete in order to spawn the next journal entry table

#### Narrative Explanation
- We are trying to find the rest of the journal entries written by the Archmage.
- However, Avernoth is a labyrinth of rooms that is nearly impossible to navigate or find anything in
- However, if we try to do things to recreate the conditions the Archmage was experiencing at the time, we may be more likely to find the journal entries

#### Notification of Goal Completion
- Upon completion, there should be an acknowledgement of (I did the thing, let's see if anything happened)

#### What Kinds of Goals?


##### Triggers
Triggers define points at which the journal entry conditions can be evaluated. These are based on in-game events.
- Enter a specific room type
- Defeat a specific enemy type
- Defeat a specific area / boss
- Defeat a number of specific room types
- Clear a number of alternate rooms
- Acquire a specific upgrade from the upgrade room

##### Modifiers (Use UObject classes to define these)
Modifiers are the specific conditions that must be met in conjunction with the triggers to consider a journal entry's conditions to be fulfilled.
- Have Specific spells / upgrades.
- Under a specific time
- Above a certain health percentage
- Below a certain health percentage
- A specific stat has to be high enough

##### Note: What Stops the Player From Restarting their Run As Soon As they Get A Journal Entry?
- Let's say the player unlocks a journal entry after reaching a certain area with a specific spell.
- Cool, the journal table spawns, and now they can restart their run. 
- But this would mean that they would only ever have to beat the game like once after getting all the journal entries.
- For each journal entry after a certain point, we should make it so that the player must "deposit" the journal entry at the end of the run for the progress to count.

## Make Journal Tables Harder To Miss

### Journal Entries Are Coated In Mana

#### Dialogue Acknowledging A Spawned Journal Table
- Dialogue on room enter
- "I sense a journal entry nearby"

#### Chromatic Aberration As the Player Draws Near
- Lerp using desired value vs actual value for smooth transitions
- Update on tick

#### Actually, they will ALWAYS spawn if you have met the conditions
- No RNG involved
- The FIRST time they spawn for that run, they will be acknowledged
- If you miss the first time, they will still spawn, but without any dialogue
- However, each dialogue entry is *STILL* limited to a specific area of Avernoth.

# What Exactly is on the Journal Entries?

### Personal Reflections / Lore
- Unimportant to the main progression of the game, but adds depth to the world and characters
- Provides insight into the Archmage's thoughts, feelings, and motivations

### Tips For Escape
- Bolded or highlighted text that provides hints or clues on how to escape Avernoth
- The part players should pay attention to if they want to progress through the game
- This *could* be a little vague, as the characters *WILL* discuss the journal entry afterward anyway

# Journal Story

### Journal Entry 1: 

#### Journal Table Spawns In
- Allister: I'm sensing a weird energy nearby. It doesn't feel like anything else I've encountered so far.
- Aristide (Maybe): Take a look around this room to see what it is...

#### Journal Table Entry:
- Lore: Yo, I'm TWEAKING
- Tips for Escape: In my research, I am putting together a spell that can manipulate space even further. I believe that with this spell, I can turn this realm into a place where nobody will find me ever.
- First, I am testing the effects of bringing *Insert Spell* into *Insert Area*.

#### Journal Response Dialogue:
- Allister: It appears this was written by the Archmage who made Avernoth. 
- Someone else: Yes, it appears Avernoth was initially incomplete. The Archmage must have been experimenting with different spells to finalize its design.
- Perhaps we should try to replicate his experiments. It could lead us to discovering more of these entries. 
- That seems to be the only lead to understanding how to navigate this place.
- Allister: Yup

#### Condition Complete:
- *The player completes the condition with the specified spell*.
- Allister: Ok, I've reached the area mentioned in the journal entry with the specified spell. 
- Hopefully, another one of those journal entries is nearby...


