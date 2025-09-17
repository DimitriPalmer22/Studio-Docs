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

#### Cancel Point
This is a frame during the Follow Through where the player can cancel the animation into another action. This is important for making the character feel responsive and allowing for combos.

- This is usually a few frames before fully transitioning back to the *Standby* pose.
- The *cancel point* should be at some clear indication that the player can move again

## Animation Philosophy
The player's animations should:
- be responsive and quick
- be weighty and satisfying
- be easy to ready

### Responsive and Quick
When I say *Responsive*, I mean that there shouldn't be that much time between the player's input and the desired action happening on screen. This is important because it makes the player feel in control of their character. 

In particular, let's say we're making an attack animation. The *Lead In* of the attack animation should be short, so that the player can see the attack (the desired action) happening quickly after they press the button.

- Shorter animations tend to feel more responsive.