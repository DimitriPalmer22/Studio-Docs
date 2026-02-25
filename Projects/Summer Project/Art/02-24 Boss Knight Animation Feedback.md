# Boss Knight & Animation Notes

## Charging Sections @ The Beginning Are Too Long
They leave the knight way too open for way too long. Assuming the player is in an active battle with just the boss, the boss will never get an opportunity to attack. We can get away with a pose that's unique to each attack, so that:
- The player can quickly recognize what the boss is about to do
- The boss can quickly get the actual attack out

Also, the whole "breathing" effect for the knight is kinda weird considering its just an animated suit of armor. It also looks off if we don't have any VFX, sounds, or theming to go with the whole breathing action. Like, if this was some type of beast or something, then yeah, it'd make sense.

## No Multi-Hit Animation Montages
The way our game is set up right now, these just aren't going to work properly / look good. When there is more than one attack per animation, there are issues with:
- Moving the character the proper distance toward the player
- Rotating the character toward the player

Even with splitting up the animations into multiple montages, the code isn't *exactly* set up for that right now, so it ends up becoming way more work.

We can experiment with this more later, but I don't wanna try to figure this out while Next Fest is still going on.

## That Dodge Attack Isn't Working As Intended
Something to note about the dodge attack that *used* to be on the fire knights is that their "Dodge Attack" wasn't one full attack attack animation; it was a *dodge* and an attack that played directly after.
- The dodge part of the animation should be its own animation.
- The attack part of the animation should be its own animation. 

## Take Note of the Swing Path of the Swords
The swing path of the swords in the animations doesn't always hit what is directly in front of the boss. In some instances, if the player hugs the boss, they are safe from some attacks. So, try to make sure the swords are hitting the area directly in front of the boss.

## Simpler Attacks
There's way too much heft in the attack animations of the knight. To me, they don't really fit the game's aesthetic, and would fit more in a Souls game. We can really let bro swing the sword. (Lowkey, try to find footage of the characters swinging the sword in ***Tenebyss***)

### Attack 01
This is cool, just make it less heavy

### Spin Attack
Real talk, this should just be the character rotating in place.

### Lunge Attack
This can play after the dodge. We can make this similar to the primordial knight's spear attack.