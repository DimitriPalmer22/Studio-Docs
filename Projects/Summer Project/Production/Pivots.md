# Pivots

## Tome Altar

Idea: the tome creation process is more customizable, BUT you need to unlock the customization. In total, its is a 3-step process.

### Step 1: Choose Your Starting Primary & Secondary

> This is unlocked by default.

The player is presented with
3 possible combinations of primary and secondary spells. They can choose one of the combinations to determine their starting spells. These are NOT completely random, they are chosen from a pre-set pool of combinations that we create. This way, we can ensure that the combinations are all interesting and viable, while still giving the player some choice in their starting setup.

![](<../../../_Meta/Attachments/Pasted image 20260515191029.png>)

### Step 2: Choose Your Starting Stats

> This is unlocked at the beginning of chapter 2.

By default, each set of primary and secondary spells has a pre-determined set of starting stats associated with it. If this customization option is NOT unlocked yet, the player will just get the default stats associated with their chosen spells.

However, once this option is unlocked, the player gets (idk, 5?) ADDITIONAL attribute points that they can distribute among their starting stats however they want. This allows the player to further customize their starting setup and playstyle. But, the player cannot remove points from their default stats, they can only add additional points on top of their default stats.

![](<../../../_Meta/Attachments/Pasted image 20260515191310.png>)

### Step 3: Choose Your Starting Addendum

> This is unlocked at the beginning of chapter 3.

By default, the loadouts come with no addendums. If this customization option is NOT unlocked yet, the player will just start with no addendums.

However, once this option is unlocked, the player can also choose one addendum to start with from a random set of 3 addendums. This allows the player to further customize their starting setup and playstyle by giving them a powerful passive ability right from the start.

![](<../../../_Meta/Attachments/Pasted image 20260515191615.png>)

### How Do We Explain This Narratively?

- Every time we unlock a new option for the tome altar, an explanation is given at the beginning of the run.
- We can have *some character* be in charge of understanding how to use the tome altar and explaining it to the player. At the beginning of chapters 2 and 3, they'll explain the new options that are now available to the player and how to use them.

### Another Thing

For the locked steps of the tome creation process, should we show the locked options in the UI, but just make them unclickable and have a lock icon on them or something? Or should we just not show them at all until they're unlocked?
- I think showing them with a lock icon is better, because it gives the player a visual representation of the fact that there are more options to unlock and it gives them something to look forward to unlocking.

## Normal Levels

## Boss Levels

To make the boss fights more interesting and unique, we should try to make each boss have a unique **mechanic or gimmick**. Such as:
- Multi-phase fights, with each phase of the boss having different attacks and behaviors.
- Environmental hazards or mechanics that the player needs to navigate while fighting the boss.
- Objectives or conditions that need to be fulfilled before the boss can be damaged or defeated.
- Minigames or quick-time events that the player needs to complete during the boss fight.

Given that each **Boss**'s design is derived from that of an existing enemy, we should play on the existing mechanics of that enemy and try to expand on them in interesting ways for the boss fights.

> It should be noted that the boss fight arenas for Area 01 and Area 02 have already been created without consideration for any boss mechanics. So, we should try to come up with boss mechanics that can work within the existing arenas for Area 01 and Area 02. However, the boss fight arena for Area 03 has not been created yet, so we can design that arena with the boss mechanics in mind.

### Some Generic Mechanic Ideas

Ideas from:
- <https://www.reddit.com/r/RPGdesign/comments/148o0t4/boss_fight_mechanics_worth_stealing_from/>
- <https://www.mmo-champion.com/threads/676950-Encyclopaedia-of-Boss-Fight-Mechanics>

#### **Kick The 'Laser'**

The boss starts chargin' his laser. Interrupt the spell before it finishes casting or it will wipe the raid.

#### **Till Death Do They Part**

The encounter consists of two bosses that must die at roughly the same time or terrible things ensue.
- Think of the Trigger Twins in Enter the Gungeon

#### **Two Mobs One Boss**

A pair of mobs with linked health pools, allowing the encounter to require more than one tank and giving positional or other challenges while not having to deal with the question of "what if X dies before Y".
- Think of the Godskin Duo in Elden Ring.
- Think of the Trigger Twins in Enter the Gungeon

#### **Teleportal**

Players are teleported to another zone/phase/area by an item or the boss, in order to do part of the fight.

#### **Boom, Headshot!**

A single, very big hit of damage is required to have some special effect on a mob.
- In our case, this can be our secondary spells. However, this would require our secondaries to frequently be readily available.

#### **Damage Immunity Windows**

The boss is invulnerable except during specific moments the player must recognize and exploit.

#### **Environmental Hazard**

The arena itself becomes a weapon (rising lava, shrinking platforms, rotating walls).

#### **Burst Your Bubble**

The boss shields themselves, requiring a burst of DPS to break the shield and interrupt the boss before they cast some kind of Spell Of Doom.

#### **Bait And Punish**

The boss has a dangerous attack with a long recovery window that is the primary damage opportunity.

#### **Adds Management**

The boss periodically spawns minions that the player must prioritize or manage alongside the main threat.

#### **Clone / Doppelganger**

The boss creates decoys or copies of itself that the player must identify and distinguish.

#### **Timed Execution**

A mechanic that only works if the player does something within a tight time window.

### Boss 1: Knight

In terms of mechanics and abilities, the existing knight enemies in the game are our most basic enemy type. It's a little difficult to come up with ideas for mechanics that rely on the enemy's existing behavior. HOWEVER, this means we can kinda play around with externally modifying the boss fight's mechanics.
- Focus less on the boss itself.
- Focus more on the overall fight's mechanics and the environment of the fight.

####

### Boss 2: Wraith

The existing wraith enemies have the most varied set of mechanics and behaviors in the game. So, we can play around with those mechanics and behaviors to create a really interesting and unique boss fight.
- Primordial wraith: Fire wall
- Tempest wraith: Lightning strike
- Twilight wraith: Simple shadow ball projectile

This room's arena is very different from the others in the sense that rather than be one large arena, it is split into several smaller sections with teleporters between them. I think we should leverage this unique layout.
- Each section has an objective that needs to be complete in order to progress / damage the boss.
- In each section, the boss takes on a different wraith form with different mechanics and behaviors. So, the player needs to adapt their strategy and playstyle in order to defeat the boss in each section.

#### Idea 1: 3 Wraiths, 1 Boss

[**Teleportal**](<#**Teleportal**>)

Each area of the level has an associated "Boss" version of one of the three wraith types.
- Each "Boss" version of the wraiths will have more health and stronger versions of the mechanics of their regular wraith counterparts.
- The player won't *just* be fighting the enhanced wraith enemy; they will also be fighting a regular wave of enemies as well.
- Additionally, the player won't just be able to outright attack the boss wraiths; they will have to complete an objective in order to make the boss wraith vulnerable to damage.
	- For example, at first the boss wraith will be in an inaccessible part of the level, still firing spells at the player.
	- Once the player finishes the objective (kills the rest of the wave & interacts with something, idk), the wraith gets warped into the main area and becomes vulnerable.

### Boss 3: Summoner

The summoner enemy's mechanics very clearly rely on the presence of other enemies. So, we can play around with that and make the boss fight's mechanics rely on the presence of other enemies as well.

#### Idea 1: 3 (Potentially More) Phases

**DURING THE PHASE**

[**Adds Management**](<#**Adds Management**>)

- The boss summons a wave of enemies.
- While these enemies are alive, the boss is invulnerable (due to being in an inaccessible part of the level).
- The player needs to kill all of the summoned enemies in order to make the boss vulnerable and be able to damage it.
- While the other enemies are active within the phase, the boss will try to do one of the following for the phase:
	- Heal several enemies
	- Apply temporary defensive buffs to several enemies
	- Apply an attack speed / damage buff to an enemy, making it a pseudo-boss

**BETWEEN THE PHASES**

[**Clone / Doppelganger**](<#**Clone / Doppelganger**>)
[**Timed Execution**](<#**Timed Execution**>)

Between phases the boss will try to recover. Stop it before it successfully recovers!
- To confuse the player, the summoner spawns two clones of itself. The player needs to identify which one is the real summoner and kill it before it finishes recovering.
	- To further disorient the player, we'll do a white screen flash and play a sound effect when the summoner spawns its clones.
	- There *SHOULD* be some consistent visual element that the player can learn to identify in order to be able to tell which one is the real summoner. Otherwise, it would just be a coin flip every time and that would be really frustrating.
- Attacking the wrong clone stuns the player for a short duration (getting the summoner closer to recovering)
- If the summoner successfully recovers, they heal themselves (not fully) and restart the current phase.
- If the player manages to prevent the summoner from recovering, the fight progresses to the next phase / finishes if the enemy dies.

- ANOTHER IDEA: the player needs to stand in a specific area (like a circle on the ground or something) to indicate which enemy is NOT the doppelganger.

## Enemies

### Unfinished Azalee Enemy

### Summoner Variation: Buffing Enemy

- Play animation
- Get up to X allies in range.
- Apply a Gameplay Effect to them
	- Have a corresponding gameplay cue
- Gameplay cue:
	- A shield around them?
	- A rune above them
	- A rune above the buffing enemy as well to let the player know they're linked?

## Narrative

## Overarching Progress
