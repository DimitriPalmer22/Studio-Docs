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

### 