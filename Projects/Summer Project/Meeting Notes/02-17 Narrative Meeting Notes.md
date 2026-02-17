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
Addendums are upgrades that can be applied to the mage's spells or stats. They are not spells themselves, but rather upgrades that alter the mage's playstyle in various ways. Within the world itself, Addendums can be thought of as additional pages being added to the tome. There are two main categories of addendums: 
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
- The player will then be given a choice between three Major Addendums to choose from, each with a brief description of its effects. The player will only be given options for Major Addendums
- The player can only choose one, and the one they choose will be added to their loadout.

#### Minor Addendum Room
Here, we will teach the player about Minor Addendums. As the player approaches the object to upgrade their tome, the dialogue will explain what Minor Addendums are and how they work.
- The player will then be given a choice between three Minor Addendums to choose from, each with a brief description of its effects.
- The player can only choose one, and the one they choose will be added to their loadout.

###