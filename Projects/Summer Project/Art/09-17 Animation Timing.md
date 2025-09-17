# Videos from Masahiro Sakurai
- https://www.youtube.com/watch?v=LewXWM7HDd8
- https://www.youtube.com/watch?v=cIB0BUe6Ihk
- https://www.youtube.com/watch?v=E8DKndKkHw8

## Takeaways

### Starting Pose, AKA Standby
- The characters in Smash all have a distinct idle animation from which they go into all their attacks
- Sakurai says to nail this first and to keep it consistent so the other action animations can flow from it and come back from it.

### The Parts of an Animation
An animation can be broken down into ***four main parts***:
- **Lead In**
- **Action
- **Follow Through**
- **The Cancel Point**

#### Lead In, AKA Anticipation
The duration at the beginning of the animation, where the character prepares for the action.

- These start with big, unexpected movements on the first frame
- We ***SHOULD NOT*** smoothly transition from the Standby into the Lead In. This takes too long and makes the animation feel unresponsive.
- In Smash, you'll see characters quickly jump into the pose rather than transition into it.
- Quicker Lead Ins feel more responsive & communicate to the player that their input was recognized
- These quicker lead-ins are also easier to read even though they are quicker

#### Action, AKA the Attack
The main part of the animation, where the action takes place. The "attack" part of an attack animation. Typically,

- This is the *KEY POSE* of the animation
- In our game, this is when our spells will fire out.
- In games with melee combat, hit-stop will apply here to emphasize the impact of the attack and strongly emphasize the pose.

#### Follow Through
The duration at the end of the animation, where the character recovers from the action.

- After the *Action* has finished registering, the pose will hang for a second before transitioning back to *Standby*.
- During this time (before the cancel point), the player cannot control the character
	- This is important for making the character feel weighty and satisfying
- The pose the character holds during the follow through should be clearly distinct from the *Standby* pose, so that the player can easily read when they are able to move again.
- The follow through should ALWAYS ALWAYS ALWAYS ***animate*** back to the original *Standby* pose.
	- Never just interpolate back to the standby pose from the action pose.

#### Cancel Point
This is a frame during the Follow Through where the player can cancel the animation into another action. This is important for making the character feel responsive and allowing for combos.

- This is usually a few frames before fully transitioning back to the *Standby* pose.
- The *cancel point* should be at some clear indication that the player can move again
- Practically, the part of the *Follow Through* AFTER the *cancel point* is just for show. If we wanted to, we could make this longer to look better.
	- It's just important to indicate to the player when they gain control of their character again.


### Specifying An Animation

Whenever making new attack animations, you can characterize them by specifying 4 things:
- The standby pose
- The attack pose
- The attack start frame
- The total number of frames until the attack can be canceled

With these 4 things, we should know how long each portion of our animation is.

# Animation Philosophy
The player's animations should:
- be responsive and quick
- be weighty and satisfying
- be easy to ready

## Responsive and Quick
- Lead Ins should be quick and snappy to communicate to the player that their input was recognized.
- Also, this game is pretty fast-paced, so the player needs quick animations to react to the action on screen as fast as possible.

## Weighty and Satisfying
- Follow throughs should be long enough to make the action feel impactful and satisfying.


## Easy To Ready
- The poses should be distinct and exaggerated to communicate the action clearly to the player.

# Timing
Ideally, the animations should be the perfect length BEFORE importing them in-engine.

We SHOULD NOT have to change the rate of the animations in-engine. It looks janky and awkward. Also, if some animations are sped up more than others, then the animations are no longer consistent with each other.

| Speed     | Standby->Action @ 30FPS | Action->Cancel @30FPS |
| --------- | ----------------------- | --------------------- |
| TOO FAST! | <4 Frames               |                       |
| Fast      | 4-6 Frames              |                       |
| Normal    | 6-7 Frames              |                       |
| Slow      | 9-11 Frames             |                       |
| TOO SLOW! | >12 Frames              |                       |
