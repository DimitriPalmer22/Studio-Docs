# 03-25 Animation Feedback Notes

## General Notes

IMPORTANT:
- DELETE the old Allister skeletal meshes that are no longer being used. `Redone_Allister_Coat_PostMerge` is the skeletal mesh being used on the character so it should be the only one in the project. I ended up using the wrong one, and that messed up my positioning for the hitboxes.
- When positioning the hitboxes for the any of the melee attacks, it is VERY IMPORTANT to use the correct preview asset. Not every skeletal mesh has the same orientation on their bones, so that can mess up the hitbox positioning if the wrong one is used. For instance, melee attacks for the knights should use the knight asset, and melee attacks for Allister should use the correct Allister asset.

## Melee Attack Hitboxes

## Tempest Slash Animation Feedback

Some of these animations were a bit too fast. These are supposed to be attacks with more of a longer sweep to them, but the speed of the attacks doesn't really allow the enemies to get caught in the attack.

The flame volley animations kinda need to be fast so the player can respond to surrounding threats quickly. We can get away with these attacks being a little slower since they cover a wider area and should protect the player more from surrounding threats.

### Hit 1

- A bit too fast. Try not to make it too slow, either. Then, it'd be frustrating to use because you wouldn't be able to respond to surrounding threats as quickly.
- Not enough forward movement / the step-in doesn't go far enough. I often found myself whiffing the first hit because the attack didn't reach the enemy. Afterward, I usually got hit because I didn't stun the enemy with the first hit.
	- Remember, this attack doesn't fire directly forward like the flame volley attack does, so it's harder to catch enemies in it. A person wielding a backhanded dagger would have to step in more than a person wielding a forward-thrusting spear, so we should make sure to reflect that in the animation.

#### Hit 2

- Speed seemed good.
- Forward movement on this was good (I think). If I hit the previous attack, I probably hit this as well.

#### Hit 3

- Too fast. Doesn't really sell the weight of this attack. To me, this is a pretty defining part of this attack chain, so we should make sure it feels as good as possible.
- Hit 3 should rotate the opposite way. In the combo, Allister rotates to the right too many times. The previous hit rotates to the right, this rotates to the right, and the final hit rotates to the right as well.
	- Rotating the opposite way would help the combo feel more dynamic.
	- Could also help the attack feel much weightier as well if we're rotating from the end pose in the previous animation to a full-on rotation in the opposite direction

#### Hit 4

- Too fast
	- Also, I don't know how final this animation is, so I'm not tripping or anything. But, if all the previous attacks use the little blade thing coming out of Allister's hands, does this mean the blade thing would come out of his foot here? Or something else entirely?

#### Close Distance Hit

- Way too fast. Somewhat jarring because it feels like there's so much going on in the animation, but it goes by so quickly that you don't really get to see it.
