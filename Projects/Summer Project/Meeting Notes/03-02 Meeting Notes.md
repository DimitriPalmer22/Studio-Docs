# 03-02 Meeting Notes

## Meeting Times

| Meeting                             | Possible Times |
| ----------------------------------- | -------------- |
| **LD Meeting**                      | Tuesday @ 8pm  |
| **Narrative Designer + CD Meeting** |                |
| Environmental Artist Meeting        |                |
| **2D Artist**                       | Friday @ 5pm   |
| Animation Meeting                   |                |
| Character Artist Meeting            |                |

## Updates Outside the Game

### Next Fest

- Next Fest is DONE
- We've gotten over 500 wishlists, but we definitely want more. So, we need to keep working on marketing and boosting the game's visibility.

### Marketing & Socials

We've created social media accounts for the game to try to further boost our visibility. The *plan* is to post regular updates about the game on these accounts to try to get more people interested in the game. As of right now, only the trailer for the game has been uploaded to these accounts, but we will be posting more content in the future.
- YouTube: <https://www.youtube.com/watch?v=iiwUaiCx2-k>
- TikTok: <https://www.tiktok.com/@od_avernoth?is_from_webapp=1&sender_device=pc>

## Updates Inside the Game

We've been updating the game throughout Next Fest, as well as updating some things behind the scenes. These are all the updates that have happened during / after Next Fest, but have not been published to the demo build of the game.

### Art Style Overhaul

- **Tone-mapping / color grading update**: Removed UE5's default tonemapping, so the game should be MUCH more saturated now. Also, contrast has been increased, so the colors should pop a lot more.
- **Pixel filter update**: The pixel filter / dithering that is applied to the entire screen is now stronger than it was before, so the game should look more pixelated now.
- **PSX Vertex Jitter**: In PS1 games, the vertices of models would wiggle around a little (due to technical limitations at the time). This is one of the biggest, most recognizable parts of the PS1 aesthetic. This effect has been applied to the Master Material, so pretty much _everything_ in the game should have this effect now. This effect is most visible on things that move.

### Small Combat Updates

- **Improved hit-stop effect**: Whenever an attack lands (either from the player or an enemy) a hit-stop effect is applied to give the attack more weight. There was a hit-stop effect before, but it was implemented poorly.
- **Damage Flash**: Whenever a player or enemy is hit, they briefly flash white. This gives the attacks more visual feedback and makes it easier to tell when an attack has successfully hit.
- **Camera Shake**: Whenever the player's attack hits an enemy, the camera shakes. There was a camera shake before, but it wasn't as weighty or impactful.

### Cinematic Black Bars

While the player is in dialogue, cinematic black bars appear at the top and bottom of the screen to give the game a more cinematic feel. It transforms the screen from a 16:9 aspect ratio to a 21:9 (ultra widescreen) aspect ratio.

## Plans Going Forward

### When Are We Done?

I want to be DONE with the game by the end of May. By that point, it would have been around a full calendar year since we've started this game. So, that leaves us with around 3 full months to finish the game.

### Sprints + This Sprint

In the remaining 3 months of time, I want us to use our time much more wisely so development doesn't drag on. So we're gonna do more focused "sprints" so we can achieve our goals with a lot more efficiency.

The main goal is that by the end of THIS WEEK, we have a firm understanding about how we want the players attacks to feel. This way, we can just focus on adding new attacks and abilities in the following weeks without wondering why the game doesn't feel as good as it can.

There are 4 Main Goals I have for this week:
1. ***Improve player combat***: I want people to see the player attack and immediately be blown away by how good it looks and feels. In a 10-second clip of combat alone, how can we get someone to play our game?
2. ***Improve level design & atmosphere***: I want people to see the spaces in our game and want to physically be there. I want them to feel the mystery and danger of the world through the environments alone. How can we get someone to wishlist the game just by showing them the environments?
3. ***2D Art & Overall Presentation***: I want to develop a more cohesive art style / plan for the 2D art in the game. This includes the in-game UI, the character portraits, and any menus. How can we make our existing mechanics seem more visually appealing through 2D art alone?
4. ***Complete the next enemy's model***: In the upcoming weeks, I want to introduce a new enemy type so we can get some more variety in combat. Getting the model in has to come first, though.

### Tasks and Assignments

#### The Player's Attacks

Combat is the game's driving force, so we want to make sure that it is as fun and engaging as possible. So, we are making strides to make it even more engaging:
- More weighty & expressive combat animations for the player
- Experiment more with the VFX that are applied when enemies are hit to make them more impactful
- Improve sound effect quality wherever possible
- Create a demo level where we can test / showcase the player attacks (this is so we can also use it to create *content on social media*)

Dimitri, Andre, and Mikel will work on these.

#### The Next Enemy

Azalee is working on our next enemy model. Hopefully our next enemy is done before the end of the week. Next week, I want to start implementing the next enemy's attacks and behavior, so we can have a more complete combat experience.

### Level & Atmosphere

#### Level of Detail

The biggest thing holding back our game in terms of level design is our environmental kit. Our levels can never really look too dynamic if we're using basic rectangular prisms to make everything.

So, for future levels (and potentially a revision of our existing levels), we want to use more complex designs for the pieces that make up the levels. For example, walls could have a couple bevels, pillars can have more complex geometry. This is something I want to explore more in a meeting.

#### Atmosphere

This has to do more with level composition, spacing, lighting, and VFX. As of now, the levels all feel kinda claustrophobic and not very "fantasy-like". I want to experiment with making the levels feel more grand and open, and I want to experiment with lighting and things like fog to make the levels feel more mysterious and dangerous. We can even experiment with making the level more open the the point where the player can see the outside world from inside the levels (granted, this means we would also have to populate the outsides of levels, but we can do this with large towers or something and then use fog to obscure the details of the outside world)

### 2D Art & Overall Presentation

#### In-game UI (Health Bar, Spell Icons, etc.)

I have been thinking about going with a more minimal look for the in-game UI to modernize the aesthetic while still keeping the retro fantasy vibe.

### 3D Prop Stuff

#### Update the Tome Altar

The tome altar is good, but there's one thing about it. The big diamond behind the altar kinda looks like the symbol that the good guys all use, which might be a little confusing since the tome altar is associated with the bad guys. So, I want to try changing the design of that symbol to that of the bad guys or something similar to it.

#### Writing Desk

In the game, we have our *Addendums*, or upgrades to the player. Currently, in the upgrade rooms, the player interacts with an *anvil* to get to the addendum screen. This makes no sense, though. If we're upgrade our *tome (book)*, then why isn't the upgrade object something book-related?

So, I want to replace the anvil with a writing desk with a magical pen and ink or something. This will make more sense thematically, and it will also look cooler.

#### Item Pedestal (For Shops)

When we first introduced the idea of item pedestals, the game's progression and upgrade system was very different. Now, the item pedestals are reserved exclusively for the shops.

Lore-wise, the mage who created Avernoth left some items behind. In order to keep them safe from other people, he placed them within these item pedestals that have some kind of *barrier* around them. In order to break the barrier, the player has to spend the currency that they have collected from defeating enemies.

The pedestal itself (the slab that lays on the ground) should look much more *plain* and flat, and we'll use a special material / VFX to show a barrier around it. Enforcing the idea that the items are locked behind a magical exchange system.
- We want chains around it in an armillary sphere pattern.
	- Note: try to keep the item inside as visible as possible.
- When we interact w/ it, the chains go away and the item is unlocked.

##### Task

- Model the slab for the pedestal
- Model the chains for the pedestal separately, that way we can animate them or something, add VFX, and make them disappear when the player spends money.

# Summary

- We've gotten over 500 wishlists from Next Fest, but we want more, so we need to keep working on marketing.
- 

--- 
- Subscribe to the YouTube: <https://www.youtube.com/watch?v=iiwUaiCx2-k>
- TikTok: <https://www.tiktok.com/@od_avernoth?is_from_webapp=1&sender_device=pc>
- Art style update: added PS1 vertex jitter, stronger pixel filter, and updated tonemapping to make the colors pop more.
- 
