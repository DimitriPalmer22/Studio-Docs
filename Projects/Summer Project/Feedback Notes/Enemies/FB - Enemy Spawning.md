# Problems with the Current System

Having discreet waves implemented for each room poses several problems
- Hard to quickly iterate on different enemy configurations
- Hard to implement scaling difficulty modifiers
- Incorporating new enemy types quickly becomes a hassle
- Manually revising the enemy configurations of each individual room quickly becomes a multi-person job, and we don't really have multiple people anymore.

# Ideas for a Revised System

Implement a style of enemy room configuration like Hades:
- Don't define exactly how many enemies there are per room, where they spawn, and which ones spawn.
- Instead, 