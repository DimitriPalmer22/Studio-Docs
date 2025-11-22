# There are two types of Journal Entry Collectables:

### Standard Journal Entries

Provide backstory about:
- The world
- Avernoth itself
- The mage who created Avernoth and his descent into madness
- The journal entries are considered "*Complete*" when the player picks them up and reads them

### Experiment Logs

- Detail the various experiments conducted by the mage
- Are used to give the player objectives that they need to actively pursue as they attempt to escape Avernoth.
- These are considered "*Complete*" when the player picks them up and reads them, and then completes the objective outlined in the experiment log.

# There Are 3 Sets of Journal Entry Collectables

### What Are Sets?

To control progression, journal entries have been divided into groups. The player needs to "*complete*" each journal entry within a group before being able to collect journal entries from the next group. This way, we can clearly indicate when large steps in progression have been made.

### Number of Journal Entries per Set

Set 1 contains:
- 3 Standard Journal Entries
- 2 Experiment Logs

Set 2 contains:
- 6 Standard Journal Entries
- 4 Experiment Logs

Set 3 contains:
- 9 Standard Journal Entries
- 6 Experiment Logs

### Limiting Journal Entries to Specific Areas

The Archmage who made Avernoth was creating these journal entries as he progressed through building Avernoth. Therefore, it would make sense that each area of Avernoth would contain journal entries from a specific set.

#### Each Area and its Corresponding Set

The first area of Avernoth:
- Is mainly themed around being a mage's study
- Contains entries from set 1

The second area of Avernoth:
- Is mainly themed around being a magical forge / armory-ish area
- Contains entries from set 2

The third area of Avernoth:
- Is a little more abstract and exposed to the outside
- Contains entries from set 3

#### In Areas where the Player Has Completed All Journal Entries
Let's say the player has completed all journal entries for set 1. They would no longer find and *NEW JOURNAL ENTRIES* in the first area of Avernoth. However, if the player is in the first area of Avernoth and they are in a room where a journal table would have spawned, we will have an upgrade there that simply indicates to the player that they have already collected all journal entries in this area.

#### In Areas where the Player has not unlocked the Next Set of Journal Entries
Journal tables won't spawn in these areas. 

# Collecting Journal Entries

### Layout of Avernoth
As of right now, each section of Avernoth contains 12 rooms:
- 8 Standard enemy rooms
- 1 Passive Upgrade Room (Pick up a new passive spell)
- 1 Upgrade Room (Choose between 3 upgrades)
- 1 Shop room
- 1 Boss room

### Distribution of Journal Entries
- Journal tables can only spawn in standard enemy rooms.
- Each area of Avernoth contains 3 journal tables that are placed in random standard enemy rooms.

### Actually Picking Up and Reading Journal Entries
- Since these appear in standard enemy rooms, the player will need to defeat all enemies in the room before being able to pick up the journal entry.
- Once the player picks up the journal entry, a reading UI will appear that allows the player to read through the journal entry at their own pace.
- After reading through the journal entry, the player can close the reading UI and continue on their way.

### Sequential Collection of Journal Entries
- In each set, journal entries appear in a *mostly random* order.
- We *can* make certain journal entries appear before others if we feel that it is important for story progression.
	- As a matter of fact, right now, I have it set up so that in each set, the very first entry the player picks up is always a specific standard journal entry that we want them to see first.
	- The second journal entry the player picks up is always a specific experiment log that gives them their first objective in that area.
	- We *can* turn this off, though.

#### Another Idea for Sequential Collection of Journal Entries
- If we want to have more control over which entries the player sees first, we can make each journal entry have its own set of prerequisites.
- For example, Journal Entry 3 might require that the player has already collected Journal Entries 1 and 2 before it can spawn.
- This way, we can keep *most* of the journal entries in a random order, but we can make sure that certain important entries are seen first.

# Tracking Journal Entry Completion

### How Do the Characters Remember all this Information?
- Lore-wise, Allister cannot keep a physical record of the journal entries he has encountered, as he loses everything when he dies / resets.
- However, one of Allister's allies can copy down the journal entries he has encountered and keep track of which ones he has completed.
- This leans into what our "Codex" is (we may need to find a better name for this)
- The Codex is a menu that the player can open to see all the journal entries they have collected so far.

### Viewing Entries in the Codex

In the codex, viewing a standard entry will simply show the text of the entry (a very similar view to the reading UI that appears when the player picks up a journal entry).

However, when viewing an experiment log entry, the player will see the text of the entry with the objective written in very plain text beside it. This way, the player will know exactly what they need to do to progress.

# Dialogue

### Entering a Room with A Journal Entry
Upon entering a standard enemy room with a Journal Table (that has a journal entry on it, NOT AN UPGRADE), A very brief dialogue interaction (1-3 lines) will play. 

In this dialogue interaction, Allister acknowledges the presence of the journal entry and comments on it. One of his allies may also chime in with a comment.

#### How Do We Choose Which Dialogue To Play?
Each journal entry does NOT have its own unique "table spawn" dialogue. Instead, there is a pool of dialogue interactions to choose from. We can have generic dialogue that can apply well to any situation the player is currently in.

We also have support for specific dialogue to play under specific conditions. Such as:
- The total number of journal entries the player has collected so far
- The current area of Avernoth the player is in
- The current pool of journal entries the player is currently collecting from
- Any dialogue flags that are true or false (as a result of any dialogue the player has encountered so far)

### After Collecting A Journal Entry Collectable
Each journal entry collectable (regardless if it is a standard journal entry or an experiment log) has its own unique "on collect" dialogue interaction.

In this dialogue entry, Allister and his allies will comment on the contents of the journal entry that was just collected. This dialogue interaction is meant to give the player more context about what they just read.

#### For Standard Journal Entries
Since the standard journal entries mainly give lore about Avernoth or its creator through the eyes of the Archmage, the dialogue interaction should mainly consist of Allister and his allies discussing the lore they just learned. 

#### For Experiment Logs
Since the experiment logs mainly give the player objectives to complete, the dialogue interaction should mainly consist of Allister and his allies discussing the objective they just received. This can also be a good opportunity for Allister to express any concerns or excitement he has about the objective.

The objective should be written in plain text within this dialogue interaction. Think of it like Allister or his Allies are trying to reason out what exactly the Archmage was doing in his experiments so Allister can recreate it.

### After Completing An Experiment Log Objective
After the player completes an objective given in an experiment log, another unique dialogue interaction will play. This is an acknowledgement from Allister and his allies that the objective has been completed.

# Journal Entry Content

### Standard Journal Entries
Standard journal entries should literally read like short diary entries written by the Archmage as he was creating Avernoth.

These are some topics that should be covered in the standard journal entries and how they could be approached in each set:

#### Set 1 Standard Journal Entries
- The Archmage's mind is still *mostly* in tact. His line of thinking should seem clear and rational.
- He made the decision to create Avernoth and flee to it because he was growing increasingly paranoid about the consequences of his actions
- While serving as part of the Musarun Empire, the Archmage created a magical device that could create magical tomes that underskilled mages could use, bolstering the Empire's military might. 
- Although the Archmage feels guilty about the destruction he caused, he believes that he should continue his magical resear 

> Note: There are only 3 standard journal entries in set 1.

#### Set 2 Standard Journal Entries
- There is a clear decline in the Archmage's mental state
- 

> Note: There are 6 standard journal entries in set 2.

#### Set 3 Standard Journal Entries
- 


> Note: There are 9 standard journal entries in set 3.

### Experiment Logs

#### Experiment Log Layout