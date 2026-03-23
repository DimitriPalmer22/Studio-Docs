# 03-23 Meeting Notes

## Meeting Times

| Meeting                         | Possible Times |
| ------------------------------- | -------------- |
| LD Meeting                      |                |
| Narrative Designer + CD Meeting |                |
| Sound Meeting                   |                |
| Environmental Artist Meeting    |                |
| 2D Artist                       |                |
| Animation Meeting               |                |
| Character Artist Meeting        |                |

## Updates To The Game

### "Summoner" Enemy Functionality

I created the new "summoner" enemy using placeholder visual assets (model & animation). However, it should behave pretty much like how the final version of the enemy will behave.

The summoner will spawn **a maximum of 3** other enemies near it at a time. The summoner will wait until the enemies it spawned are defeated before it can spawn more. The summoner itself won't really do anything other than spawn other enemies, so it will be a pretty easy enemy to deal with if the player focuses on it. However, if the player ignores it, it can quickly become overwhelming as more and more enemies are spawned.

### "Chapter 1"'s Quests Are All "Complete"

Functionally speaking, the player should be able to complete all the quests associated with chapter 1 and see the corresponding dialogue and journal entries. However, there are still some placeholder elements that need to be replaced with the final versions.

## Plans Going Forward

This week's goals are primarily:
1. ***Finish up "Chapter 1" of the game***: By the end of this week, I want the player to be able to complete all the quests associated with the first "chapter" of the game. This includes the necessary dialogue and journal entry text associated with the quest as well.
2. ***Prepare for "Chapter 2" of the game***: This means to figure what kinds of quests we want to give the player and what kind of dialogue we want to have in the second chapter. We can start writing some of the dialogue and journal entries for the second chapter as well.
3. ***Finish Up Work from Previous Weeks***:
	- Properly de-squaring levels
	- Completing more updated character portraits
	- New enemy models - (I still don't have a design for the new one I gave Erin).
	- Other 2D UI assets
	- More animations & animation revisions

> This is the part 
## An Idea Real Quick: The Enemies

**Problem**: We know our enemy variety in the game is pretty lacking right now. We only have 2 enemy types (the "melee" knight enemies and the "ranged" wraith enemies). Furthermore, the fact that they all look alike makes them feel *even more* similar.
- Them looking similar is something that has been noted on. The fact that our enemies are all essentially re-skins of each other makes us seem a little *uninspired* as developers.

I'm thinking about implementing two solutions that will hopefully add some more variety to the enemies in the game without requiring us to create a ton of new assets.

### Solution 1: Large Tank Enemy

 After these two enemies that are currently being made are done, I'm thinking of adding just 1 more enemy type: a large, healthy, slow-moving, heavy-hitting tank enemy.

Once we have this in *ALONG WITH* the two new enemies we're trying to make, we should be able to make a decent variety of **enemy combinations** in the game.

### Solution 2: Re-design the Enemy Variants

The knight and wraith enemy types each have 3 variants (6 enemies total). Although the variants DO have different attack types, they still look and behave pretty much the same:
- Knight enemies will all do their attack once the player is in range. Otherwise, they will chase the player down.
- Wraith enemies will stay in place and shoot at the player once the player is in range. Otherwise, they will just stay in place.

I think we'd be able to get away with these enemy types each having basic similar behavior if they looked different enough from each other.

**Here's what I think**: Our enemies can all fit within a specific visual theme / aesthetic. This way, there isn't a lot of visual conflict in the enemy designs. Then, once we decide that, we use that artistic direction to inform the *REVISED* designs for the existing enemy types.

## Bug Tracking

Link: <https://forms.clickup.com/90131425169/f/2ky40twh-3873/ZFSTRRZKQYU57356US>

If you ever see a bug / a feature not working properly / a small oversight in the game, you can submit a bug report to our bug tracking system. It takes like 10 seconds. This will allow us to keep track of all the bugs in the game and prioritize them accordingly.
