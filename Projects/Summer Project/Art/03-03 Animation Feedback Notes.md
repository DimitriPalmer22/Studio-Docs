# 03-03 Animation Feedback Notes

> Important note about in-engine movement + root motion: It's kinda seeming like we can only have one or the other with the way Unreal Engine is set-up. This isn't horrible or anything, but it seems like we'll have to rely on the root motion to get the proper movement in our attsack animations.

## Swing 01

- The tail end of this animation doesn't stay for long enough, making it easy to drop the combo.
- Also, the animation doesn't transition very well from idle to the first frame of the attack. It loops nicely with the finisher, but the transition from idle to the first frame of the attack is a little jarring.
- Also, a little bit of a _step-in_ or something would be appreciated here as well. Having no forward movement at all is a little rough, especially when trying to initiate a combo.

## Swing 02

- You forgot to enable root motion for this animation sequence, but I re-enabled it when I was testing it. _I MAY NOT PUSH MY CHANGES SO DOUBLE-CHECK TO SEE IF YOU NEED TO RE-ENABLE IT_
- For right now, I don't think this animation needs to be touched anymore.

## Swing 03

- Allister seems a little _too_ off-balance here, like he couldn't possibly recover from this attack without falling over. Maybe we can tone down the amount of lean a little bit?
- Allister doesn't actually move forward / step into this attack very far, which makes it harder to land. This also makes it look a little strange visually since the previous hit takes a significant step forward.
- Possible fix: Have Allister's right foot move much more forward (and a little out to the right so he can maintain his balance).
- Also, in the tail end of the attack where he goes back to his idle position, he moves his _right leg_ backwards to get back to his resting position. This is strange since he should be leaning all of his weight on his right leg for the majority of the attack, so it would make more sense for his left leg to be the one that moves forward to get him back to his idle position.