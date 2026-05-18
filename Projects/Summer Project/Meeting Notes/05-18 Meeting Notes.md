# 05-18 Meeting Notes

## Revisiting the "Unfinished Features" From Last Week

Last week's meeting notes: [05-11 Meeting Notes](<./05-11 Meeting Notes.md>)

### Questions the Start of the Game

The questions at the start of the game are being scrapped.

Before, when the player interacted with the Tome Altar in the beginning room, they would be given a quick questionnaire that would determine their starting spells, stats, and possibly addendums. This was meant to add a roguelike element to the game and make the player's starting setup feel more personalized.
- However, this feature is just too much work to implement and it doesn't add enough value to the game to justify the effort.
- It also adds a lot of complexity to the game's design and development, which is not ideal given our time constraints.

Instead, we have a new 3-step tome creation process that is more customizable, but also more structured and easier to implement. The player will still have some choice in their starting setup, but it will be more guided than the original questionnaire idea.

See [the Tome Altar Pivot](<../Production/Pivots.md#Tome Altar>) for more details. At this point, steps 1 and 2 have been implemented, but step 3 still needs to be implemented.
- Also, the UI for this has NOT been implemented yet.
- The layout and 2D elements are still placeholders.

### Summoner & Summoner Variation (Buffing Enemy)

The summoner enemy's model & animations are close to completion (It's not done being textured, yet).

![](<../../../_Meta/Attachments/Pasted image 20260518194048.png>)

To help a little with enemy variety, a variation of the summoner enemy is being created that will buff other enemies.
- While enemies are "buffed", their resilience (defense) increased dramatically. So, they take very little damage from the player's attacks.
- Players will need to either wait for the effect to wear off or kill the Buffing Enemy to get rid of the buff on the other enemies.

The behavior and logic for this has been implemented, so designers *can* begin placing this enemy in levels (preferably in Areas 02 and 03). However, the model is incomplete, so it looks like a placeholder for now. This also applies to the base summoner enemy, whose logic is also complete.

### Normal Levels

The normal levels for Area 03 are still very incomplete. We only have 1 or 2 levels done, and they don't have much variety in terms of room types or enemy placement. So, we should try tackling that by going with the [pivot discussed in last week's meeting](<./05-11 Meeting Notes.md#Normal Levels#>).
- Use an existing room from Area 01 or 02 as an overall layout template.
- Change the overall aesthetic of the level by
	- Making the level look more abstract & otherworldly (exposed sky, weirder shapes)
	- Changing the lighting to make sure it mathe

If you are struggling with this, look at the existing levels in Area03 as a style reference.

## Tasks and Such

### Normal Levels

- Brian - We need another new Level for Area 03.
