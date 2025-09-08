### Meeting Notes

| Meeting                                | Possible Times |
| -------------------------------------- | -------------- |
| LD Meeting                             |                |
| VFX Meeting                            |                |
| Narrative Designer + CD Meeting        |                |
| Sound Meeting                          |                |
| Environmental Artist Meeting           |                |
| 2D Artist + Narrative Designer Meeting |                |
| Animation Meeting                      |                |
| Character Artist Meeting               |                |

### Big Change, Huge Even - Mana Rework
- Instead of mana being a resource that depletes and refills, it is a resource that builds up as you play.
- Primary spells will no longer cost any mana.
- Dodging will also no longer require any mana.
- ONLY secondary spells will cost mana.
- Mana no longer passively regenerates.
- Mana builds up as you:
	- Land hits with primary spells?
	- Perform timely dodges?
	- Clear rooms?

#### Why the change?

##### Why other games don't do this
- The main contemporaries for gameplay are Kingdom Hearts II and Hades
- Those games don't have a resource system tied to their basic attack and dodge mechanics, and for good reason.
- Limiting the player's ability to attack and dodge severely slowed down the pace of gameplay, and also make it frustrating to engage with groups of enemies.
	- It essentially felt like the player was being punished for engaging with enemies.
- A "stamina" system works in a game like Dark Souls or Elden Ring because combat is much slower and is really like a reactive dance between the player and the enemies.
- In a much faster game like this, the "stamina" system just feels like an unnecessary hindrance to the player.

##### More Variety for passive abilities
- We can have abilities that activate when over / under a certain mana amount.
	- Choose to use secondary spell more / less often
- Same for health

##### An excuse to make the secondary spells more special

- If the secondary spells are literally the only thing locked behind this resource, them it should feel more special when you use them.
- Also, it gives us an excuse to make the secondary spells more powerful and flashy.
- Fullscreen VFX (like a vignette or chromatic aberration) when using a secondary spell.
- Super-armor while longer animations play out.

#### How do we feel about this chat?
- None of these changes are on the main branch yet. They are on a separate branch
- If we feel good about this and think it is a good idea, I'll push the changes I have right now.

##### Current Changes
- Mana no longer passively regenerates
- Mana builds up when you land hits with primary spells.
- The primary spells do a little bit more damage in general

### Playtesting 
- It'd be pretty fire for you guys to playtest the game and give feedback on the following:

	- **The current enemy density**. Are there too many / too little enemies per-wave?
	- **The time-to-kill**. Are the enemies too tanky / too squishy? Does it take too long to kill enemies, or are you able to kill enemies before they really get a chance to pressure you?
	- **How long the player spends in the room**. Is it too long / too short? Should there be more waves? Should there be more enemies per-wave?
	- **How often you are having to dodge**. Does it feel like you need to dodge too often / not often enough? Does it feel like you really need to be a ***gamer*** in order to play this game?
	- **How you feel about the new mana system**. Do you find yourself using your secondary spells more often? Less often? Do you feel like you are being punished for using your secondary spells? Should mana build up faster?
	- **Secondary Spells In General**. Do they need to be buffed / nerfed.
	- **Does the game feel too monotonous?** How long does it take before it sinks in that you're just doing the same thing over and over again? What can we do to make the gameplay loop more engaging and varied?

- Based on how we feel about the feedback, we can make informed design decisions going forward. 

- For the people who don't work in-engine, I'll try to have a build out as soon as possible (with a readme so you know what to do / how to play / what feedback we're specifically looking for)
	- I would've had a build out by the time I had this meeting, but a little oopsie is preventing the game from building so I gotta tackle that first.
- I WILL ping you guys when the build is out, and I WILL ask you guys to play it and ***have some feedback prepared for the next meeting***.

### A Little Update on the VFX

- Last week, Mikel and I had a VFX meeting where we tried to establish a more consistent style & methodology for the game's VFX
- You can find the notes from that meeting here: https://docs.google.com/document/d/1CotzuKCkylPIRJDt6q5vqK-lmzU9-B8RgKnVZGS5qYQ/edit?usp=sharing
