> Note: This is not the Art Style Guide.

# Overview
- Overall, we're going with a non-photorealistic art style for this project.
- In particular, I've been really drawn to the PS1 / PSX art style for a couple reasons:
	- Could be really interesting to try and modernize
		- Lower quality assets could help with getting more things done within the short time we have
- The goal is to have a low-poly art style that is still visually appealing and interesting in a modern way

### The PS1 / PSX Art Style

#### Things I Want
- The low-poly aesthetic of the PS1 era. All models should generally have some pretty hard angles. Even circular objects need to have very noticable edges.

- Low res textures. I want to try and keep the texture resolution low, but not so low that it becomes hard to tell what you're looking at.
- Reduced Color Depth. Most games on the PS1 used a 15-bit color depth.

#### Things I Don't Want
- The weird vertex and texture warping on models that happened as a result of the PS1's hardware limitations. (The actual names for these are [screen space vertex snapping](https://www.youtube.com/watch?v=Ap-RV6pcXDk&ab_channel=Marcis) and [affine texture mapping](https://www.youtube.com/watch?v=byYNo2Puv9g&ab_channel=DanielIlett))
- The extreme pixelization due to the PS1's low resolution. I feel like trying to do this on modern screens would make the scene harder to read
- The low framerate found in many PS1 games. A lot of those ran at 15-20 FPS, which is not something I want to replicate. I want the game to target 60 FPS.

# References

### Magnix Games (Lowkey Exactly What I want the Game to Look like)
- I stumbled across this one guy on Instagram and he was making this game that is very similar to ours in terms of visuals. Also, he's making his game in Unreal Engine 5, so anything he's doing should also be achievable by us.

[Here's his YouTube](https://www.youtube.com/watch?v=F3u7SyMXLWU&ab_channel=MagnixGames).

Both of the videos on here are pretty short, but they show off a lot of the game's visuals.

[Here's his Instagram as Well](https://www.instagram.com/magnixgames/)

#### What I Like Visually About the Game
- His VFX are insane. They're not exactly what you would find in a PS1 game, but they still fit the aesthetic anyway.
	- Ghost effect thing when he does his dash
	- Sword trails
	- Hit effects
	- Sparkles around projectiles
	- Dust and stuff when he jumps (its a little hard to see)
	- Random particles just chillin in the air
	- Also, they all seem low quality to the point where I could see them being in a late PS1 / early PS2 game
- His fullscreen dithering effect is perfect
- His character model looks cool.
	- I like the silhouette of the character
- His environmental models are low poly + his textures are low res. However, they are still easy to read. They are detailed enough that the low-poly nature of them isn't distracting
- The animations / posing is really good
	- Very fluid. In fact, too fluid for a PSX game, which is good.
	- The way he holds his swords while idling is sick.
- Still uses modern techniques to give his game a good feel
	- Things like camera shake when hitting enemies
- I noticed that his FOV seems pretty high
- Fog is an excellent touch

#### What I Don't Really Want In Our Game
- His game is a dark fantasy game, and his color choice + his overall art style is dark and gritty. I want our game to be a little brighter and more colorful. Also, its generally just hard to see in his game because its so dark at some points
- Pixelization shader is a little too harsh

### Actual PS1 Games for Reference
I think these games are also pretty good references for how I want this project to look. I could probably download any of these games and play them in call if any of you want.

- Vagrant Story
	- An excellent example of a 3D PS1 game that looks really good.
	- This game came out at the very end of the PS1's lifespan, so it looks a lot better than most other games
	- I really like the way the characters in this game look
![](<../../../_META/Attachments/Pasted image 20250509171117.png>)
![](<../../../_META/Attachments/Pasted image 20250509170856.png>)
![](<../../../_META/Attachments/Pasted image 20250509171035.png>)
![](<../../../_META/Attachments/Pasted image 20250509171221.png>)

- Final Fantasy IX
- The Legend of Dragoon

# Models
- Even though we're going for a low-poly art style, I don't want everything in the game to be completely flat to the point where we solely rely on textures to add detail.
- Im ngl, modeling is like my weakest area, so I don't have much to write here other than low-poly good, high-poly bad

![](<../../../_META/Attachments/Pasted image 20250509165446.png>)

> Octagonal barrel model

# Textures
- Textures should be 512x512 at the max. I want to try and keep them lower than that if possible. 128x128 or 256x256 would be ideal.
- I've seen people start out by creating a low-res texture completely from scratch and just stick it in-engine like that
- I've also seen people get a high-res texture and downscale it to a low-res texture. This is pretty easy to do in Unreal, but this should be done with caution, as you might lose some of the more important details of the texture.

# Post Processing
- A black outline shader is applied to everything (although this may be unnecessary / may muddy up the look of the game)
- A color reduction shader + dithering shader is applied to the entire screen. In areas where the screen is dark, the dither texture subtly shows up, which helps to create the illusion of a wider range of colors
![](<../../../_META/Attachments/ScreenShot00002.png>)

> Without Dither

![](<../../../_META/Attachments/ScreenShot00003.png>)

> With Dither

# UI / 2D Elements
- Given that the game has a retro aesthetic to it, the UI would need to fit into that as well
- I've been thinking that the whole idea of using a reduced color palette for any 2D elements as well would help to sell the retro aesthetic
- Also, I've been thinking that applying a dithering filter to any 2D asset before we put it in-engine would help with making everything feel retro and cohesive

![](<../../../_META/Attachments/Pasted image 20250509180006.png>)

- I'm against having a completely minimal UI. Some things are allowed to be on screen at all times (like a health bar or something)
- The 2D elements are not meant to be completely 8-bit like some games. Having the UI be too pixelated / low-res might be too much. Honestly, this might be one of those points where we can take some liberties and make the UI a little more modern

![](<../../../_META/Attachments/Pasted image 20250509174846.png>)

> Castlevania: Lament of Innocence (PS2)

![](<../../../_META/Attachments/Pasted image 20250509175042.png>)

> Valkyrie Profile (PS1)

![](<../../../_META/Attachments/Pasted image 20250509175318.png>)

> Xenogears (PS1)

- Character portraits: When the different characters in-game are talking to the player, a character portrait will show up on the screen. This will be a 2D image of the character.
	- Since we don't know how many different characters there will be at this time, I don't think they'll be animated like they were in Relapse. It might be too much work for the time we have
	- At the bare minimum, each character needs a single portrait image
	- Depending on how things go, we can probably get multiple portraits for each character that show different emotions for different lines of dialogue

- To help with conveyance, I'm thinking we can try to lean into having a lot of 2D UI elements.
	- Some will be on-screen
	- Some will be in world-space
	- We can have indicators for
		- Player health (next to the player / above their head)
		- Enemy health (next to the enemy / above their head)
		- Some type of UI to let the player know the room has started / ended
		- A little pointer to let the player know where an interactable item is
		- other stuff

- Also, menus are a thing
	- I don't really have an idea for how these should look right now
	- The overall style of the menus should fit the overall style of the game and should also be pretty consistent between the different menus
	- However, the overall look is up to whoever designs them

# Modernizing the Look
- The goal is to modernize the PS1 look, not just copy it. This means that we can take some liberties in some areas to make our game stand out a little more.
- We can do things like
	- Abuse Unreal Engine's lighting
	- Use post-processing effects (Bloom, chromatic aberration, etc)
	- Use particles & VFX at every opportunity
	- Provide visual feedback to the player every time they do something (add a camera shake, play an animation, have the UI do the dougie idk)
