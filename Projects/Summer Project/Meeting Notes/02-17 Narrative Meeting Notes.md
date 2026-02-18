The main goal for right now is to convey the game's main ideas to the player in the best ways possible through the dialogue. In other words, "*Tutorialization*."

# Core Ideas
### "Tome Altar"
The "*Tome Altar*" is the object in the beginning room that the player interacts with to acquire a new tome. The Tome Altar presents the person using it with a quick personality assessment, from which the Tome Altar determines the *Loadout* for the Tome they will receive. 
#### Loadouts 
Loadouts are the set of spells and upgrades contained within a specific tome. Specifically, each loadout is made up of:
- **A primary spell**: The mage's main method of attack
- **A secondary spell**: A stronger spell the mage can use less frequently
- **Addendums (FKA Passive Spells)**: Upgrades with unique effects that altar the mage's playstyle in various ways. These are not spells, but rather upgrades that can be applied to the mage's spells or stats. (More on this in ["Addendums"](<#"Addendums">))
#### Lore
As we know, the archmage who created *Avernoth* is responsible for inventing this device. It was used to empower the troops of the Empire, enabling them to oppress various peoples.

### "Addendums"
Addendums are upgrades that can be applied to the mage's abilities. They are not spells themselves, but rather upgrades that alter the mage's playstyle in various ways. Within the world itself, Addendums can be thought of as additional pages being added to the tome. There are two main categories of addendums: 
- Major (Slotted) Addendums 
- Minor (Unslotted) Addendums.

> Note: 
> The Addendum system in our game is supposed to be very much like the boon system from Hades II, whereas the Primary and Secondary spells operate much like the weapons the player chooses before their run in Hades. The spells are supposed to be relatively immutable, while the Addendums provide much of the run-to-run variety. 
> I opted to transition to a system like this instead because the rigid structure makes it much easier to concept abilities and implement them within the game's progression system. It was much easier to operate within a structured set of rules.

Here's a Google Sheet containing all the existing Addendums in the game: https://docs.google.com/spreadsheets/d/1KFx0LBjvIDT_CriO2C3WWN4KZiQRiFcYdw6Axi6NLJI/edit?usp=sharing
#### Major Addendums
*Major addendums* are addendums that apply powerful playstyle-changing effects to various actions the player can perform. *Each slot with a tome's loadout can only hold **ONE MAJOR ADDENDUM AT A TIME***. Within the player's loadout, there are 5 slots for major addendums:
- **Primary Spell Slot** - Effects that apply when the player uses their primary spell / their primary spell hits an enemy (or maybe some other condition depending on the effect)
- **Secondary Spell Slot** - Effects that apply when the player uses their secondary spell / their secondary spell hits an enemy (or maybe some other condition depending on the effect)
- **Dodge Slot** - Effects that apply when the player dodges or executes a *perfect dodge* 
- **Damage Taken Slot** - Effects that apply when the player takes damage (or maybe some other modifier like taking a certain amount of damage in a small time)
- **Shield Slot** - Effects that apply when the player has more than a certain amount of shield or when their shield breaks (or maybe some other modifier like having a certain amount of shield when performing an action) 
##### Quick Example: Chain Lightning Major Addendums
This is where I showcase the chain lightning addendums I created to demonstrate how this system works in practice.
#### Minor Addendums
*Minor addendums* are lesser, miscellaneous effects that make the player feel stronger without necessarily affecting their playstyle too much. The effects for these can vary from simple stat increases to more complex effects that trigger when certain conditions are met. *Minor addendums can stack with each other and with major addendums.* There are no specific slots for minor addendums; they simply apply their effects to the player as long as the player has them. However, the player cannot receive duplicate minor addendums. 
##### Major vs. Minor Addendums: A Source of Confusion.
Upon looking at some of the examples of existing Addendums, you may notice that some Minor Addendums have very similar activation conditions to Major Addendums. 
- For instance, the "*Evasive Current*" **Major** Addendum sends out chain lightning when the player perfectly dodges. 
- Meanwhile, the "*Arcane Reflex*" **Minor** Addendum restores some mana whenever the player perfectly dodges. 
This has led some people to ask, "Wait, if Arcane Reflex ALSO activates when perfectly dodging, why is it not a **Major** Addendum?" 
- Well, that's because the effects of Arcane Reflex are much less impactful on the player's playstyle than Evasive Current. Arcane Reflex simply restores some mana, which is *a nice bonus but doesn't really change how the player approaches combat*.

### Addendum Rooms (Upgrade Rooms)
Throughout Avernoth are rooms where the player can upgrade their current tome by acquiring new Addendums. These rooms are called "*Addendum Rooms*". There are two types of Addendum Rooms:
- Major Addendum Rooms: Rooms where the player can acquire new Major Addendums for their current tome.
- Minor Addendum Rooms: Rooms where the player can acquire new Minor Addendums for their current tome.
Each "Area" of Avernoth has one Major Addendum Room and one Minor Addendum Room. 
#### Major Addendum Room
Here, we will teach the player about Major Addendums. As the player approaches the object to upgrade their tome, the dialogue will explain what Major Addendums are and how they work. 
- The player will then be given a choice between three Major Addendums to choose from, each with a brief description of its effects. The player will only be given options for Major Addendums in slots that are not yet filled by another Major Addendum.
- The player can only choose one, and the one they choose will be added to their loadout.

#### Minor Addendum Room
Here, we will teach the player about Minor Addendums. As the player approaches the object to upgrade their tome, the dialogue will explain what Minor Addendums are and how they work.
- The player will then be given a choice between three Minor Addendums to choose from, each with a brief description of its effects.
- The player can only choose one, and the one they choose will be added to their loadout.

# Narrative Tasks

## Beginning Room Dialogue
### Write a New Initial Wake-Up Sequence
The existing initial wake-up sequence is something we've needed to rework for a bit. 
- The main issue with it is that it's just way too long. Front-loading the game's exposition wasn't working well.
- Also, the layout of this room is gonna change AGAIN, so the dialogue needs to be reworked to fit the new layout. 
- ALSO ALSO, we're no longer gonna have a static portal spawn in front of Allister at the beginning, so the dialogue needs to be reworked to fit this change as well.

1. Allister - Ah my head
2. *Portal Spawns*
3. ??? - Yo
4. Allister - says something
5. Magnus then explains everything concisely. 
6. Once Magnus is done, then they have some quick banter.
7. Before Magnus leaves, he acknowledges the Tome Altar (although he doesn't know what it is yet) and encourages Allister to go check it out. 
### Write a Tome Altar Tutorial
This dialogue pops up automatically as Allister approaches the Tome Altar. *Somebody* explains that this is the Tome Altar, and that it will give Allister a tome with a set of spells and abilities (we won't say the word "Addendum" yet). They explain that the Tome Altar determines which tome to give Allister based on a quick personality assessment, so Allister should just go ahead and interact with it to see what happens. 
### Write an Exit Portal Tutorial
As soon as Allister finishes the personality assessment:
- Acknowledge that he got a new tome and is ready to get out of here
- *The camera pans to the exit portal*
- Somebody explains that the exit portal is how Allister can leave the current area and move on to the next one, and that he should use it when he's ready.

## Major Addendum Room Dialogue

### Write Entrance Dialogue
A quick acknowledgement that this room is nothing like the rest. 
### Write Dialogue for Approaching the Upgrade Object
As of right now, the "Upgrade Object" is an anvil (I know, its a little weird, but it is what it is. Ok ok, special writing desk with special magical ink.) placed toward the back of the room. 
- As the player approaches it, the dialogue will explain what Major Addendums are and how they work. 
- The dialogue will also explain that the player can only have one Major Addendum in each slot at a time, so they should choose wisely.
### Write Dialogue for After Choosing an Addendum
After choosing an addendum, we can have a quick bit of text talking about how Allister feels stronger and he should try out his new addendum on some enemies.
## Minor Addendum Room Dialogue

### Write Entrance Dialogue
The minor addendum room will *ALWAYS* appear AFTER the Major Addendum room. So, by this point the player will already be familiar with the concept of addendums, and they will already have at least one major addendum in their loadout. 

Also, The two rooms are visually similar, so an acknowledgement of this room feeling similar to the other addendum room would be a nice touch.

Something along the lines of "Hey, this room looks a lot like that other addendum room I was just in. I wonder what we'll find in here?"

### Write Dialogue for Approaching the Upgrade Object
Again the upgrade object is an anvil. The dialogue here can be a little more casual and less explanatory than the dialogue in the Major Addendum Room. 
- As the player approaches the anvil, we get dialogue explaining that Allister will get a new minor addendum for his tome, which will make him feel stronger and more powerful, but won't necessarily change how he approaches combat like the major addendums do. 
- The dialogue here can also reference the fact that the player has already been to a Major Addendum Room and has already acquired a Major Addendum, which will help reinforce the idea that there are two types of addendums and that they are different from each other.
### Write Dialogue for After Choosing an Addendum
Similar to the Major Addendum Room, we can have a quick bit of text talking about how Allister feels stronger and he should try out his new addendum on some enemies.
## Shop Dialogue

### Room Entrance Dialogue
The shop is one of the least fleshed-out parts of the game right now, so it's definitely difficult to write dialogue for it without knowing more about how it's gonna work. However, we can still write some basic dialogue for when the player first enters the shop.

- Acknowledge the lack of an enemy presence.
- Comment about the items scattered about, but how they are confined to the pedestals they sit on.
- We need to use the mana essence we've collected from defeating enemies to purchase these items.

### NOTES
- The item pedestals themselves can be named something unique / specific to further convey their function within the game's world.
- 

# Summary of Tasks

1. Beginning Room Dialogue
	1. Wake-Up Sequence
	2. Tome Altar Tutorial
	3. Exit Portal Tutorial
2. Major Addendum Room Dialogue
	1. Room Entrance
	2. Approaching the Upgrade Object
	3. After Choosing an Addendum
3. Minor Addendum Room Dialogue
	1. Room Entrance
	2. Approaching the Upgrade Object
	3. After Choosing an Addendum
4. Shop Dialogue
	1. Room Entrance