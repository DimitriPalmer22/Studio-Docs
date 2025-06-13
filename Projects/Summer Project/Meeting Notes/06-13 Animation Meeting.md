- Andre's Maya does not work at all lol
- James can lowkey start using Cascadeur (the free version or whatever)
- So here's the plan, Andre will buy Cascadeur so that he can export the .fbx files
	- Any files that need to be exported, James will send to Andre

# Animating the Lower Body
- For Relapse, we didn't animate the lower body at all for the attack animations
- We need that same ideology for this game as well. We want the player to keep moving while attacking too
- In Unreal, we can turn off specific parts of the skeleton within the animation blueprint
- But, just to be safe, for now, we should keep the animation in the lower body very minimal

# Animations Refs for Attacks

Elden ring spells & incantations playlist: <https://www.youtube.com/watch?v=uTicUT_9V4s&list=PLroUIy_Wtyech5USZdezwlVi9hg_3LDD6>

Incants video: 0:26, 1:38, 1:46, 2:26, 2:46, 3:00, 3:36 maybe
Spells video: 1:58, 2:14, 2:22, 2:31, 2:57

Most of Elden Ring's magic is meant to stop the player from moving / slow them down while they are casting. In our game, I want the player to be able to move more freely while they are casting spells. So, the the attack animations should focus more on expression in the upper body. Also, in Elden Ring, the player needs a staff for casting spells. In our game, the player doesn't have any type of tool or anything they use to cast magic. So, for any animation from the spells video, try to imagine it where the player is waving their hand around or something for the animation.

Also, I picked animations that were really quick / didn't really have any wind-up. For fast-paced & ranged-based games like this one, it's super frustrating to have your aim all lined-up, but then miss because there was some type of delay or wind-up between when you pressed the shoot button and when the projectile was actually fired

# Walk Speed
- For Relapse, the walk speed was a big issue because the enemies were sliding in their walk animations
- For this game, for right now, I *think* the walk speed is about right, but it's kinda hard to tell. 