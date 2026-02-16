# VFX

- As of right now, most VFX in the game are using Niagara components attached to some type of Actor (The enemy or player we want the effect to play on).
- However, this is NOT the way to go. This is not as *modular* or *reusable* as we want our VFX to be.
- Instead, we are going to lean even harder into using *Gameplay Cues* for our VFX. This will allow us to have a much more modular and reusable system for our VFX.

## !!!TRANSMUTATION CIRCLES!!!
- The transmutation circles I made NEED to get out of the game
- They are a little unperformant (because they use the ribbon renderer) and don't fit well with the game's art style.
- They need to be redone, but better. 
	- Most of the effect should be modeled / textured externally and not generated within Niagara.
- The plan is to reuse these transmutation circles in the sections listed below, since I *did* want them to be part of the game's visual identity

### Enemies Casting Spells / Attacking
- *THIS IS STILL A LITTLE IFFY*. With the number of effects in the game right now, the game is very visually noisy, and this could potentially make the problem worse.
- Before, I had an idea of using transmutation circles heavily to telegraph enemy attacks and spell casts (in addition to the animations of course)
- Wraith enemies will have a transmutation circle appear at the location they will fire their projectile from.
- The Knight enemies will have a transmutation circle appear at their feet as they are about to attack. (Accompanied with a little glow or something so that the player can see it even if they aren't looking straight down at the floor)

### Room Exit Portal
- The room exit portal needs to be tweaked a little.
- Originally, we had a large glow emit from the center of the portal to make it visible from far away in the level.
- HOWEVER, this large glow OVERLAPS with Allister as he steps inside, creating this weird visual effect that not only looks a little weird, but kinda blinds the player as they step inside the portal.
- Instead, we can have a hollow swirl around the outside of the portal so we can still make it visible from far away without creating that weird overlap effect when the player steps inside.

![](<../../../_Meta/Attachments/Pasted image 20260213013926.png>)

### Enemy Spawn Transmutation Circle
- Again, my old transmutation circle is being used for this, and it is not good. It needs to be redone.

### Journal Table???
- As of right now, a huge transmutation circle appears above the journal table whenever there is a new entry available. However, I don't think we should move forward with this. It looks too weird.

## Journal Table!
- Rather than have the huge transmutation circle sitting above the journal table, we can do something else.
- Above the *page*, we can have a rune symbol floating.
- This rune symbol is gonna be constantly flipping through all the rune symbols that we have in the game. (This is because each journal entry has a corresponding rune symbol that gets revealed later, so we don't want to spoil which entry is which by having a specific symbol for each entry sitting above the table)
- Last, we should have this symbol billboarding towards the player at all times so that it's visible and readable from any angle.
- And then maybe some other effect to it so that it is clearly visible and sticks out to the player.

## Flame Volley

- Now that the melee attacks are actual melee attacks, we can have more liberties with the VFX for our melee attacks
- No more just sparks and impacts!!!
- **NOTE**: As you work on the Flame Volley animation montages, nobody else can work on them. So the following can't really be adjusted until you're done with them:
	- Hitbox placement / timing
	- Completely changing out animations for new ones