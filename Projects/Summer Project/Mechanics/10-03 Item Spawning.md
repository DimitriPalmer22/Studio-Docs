
# What is the problem
- I need players to know when PHYSICAL items spawn
- I need to make sure that they are aware of when they pick them up
- I need to make sure the player knows what it is they are picking up
	- Right now, the green health orbs are too *nothing*

# Ugh Solution

Legit, I can't think of a way to spawn items intelligently without deliberately creating spawn volumes in each level. Yeah, this works, but:
- someone would have to go back into old levels to do this (potentially causing merge conflicts)
- this is yet another thing the LDs would have to make sure is in the levels and set up properly

# An Actual Solution

- Spawn items @ the end portal
- Make sure the player *interacts* with the object?
	- ehhh what if they don't want to pick it up? This essentially forces the player to do whatever the game wants it to?

# An Even Better Solution

- Spawn the item on the dead body of the last-killed enemy.