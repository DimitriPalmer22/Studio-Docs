# AI Rework

State machine-based approach where each state has a collection of tasks associated it.
We'll use latent / async nodes to control the flow of execution within the graphs to avoid any issues. We can also explore the idea of using interrupts to break out of certain tasks when certain conditions are met (e.g. player gets too close, player goes out of range, etc.).

## Injecting Unique State Unique Behaviors While Preserving Structure

AI System Components:
- Enemy AI Controller Blueprint
- State Tree Asset
- State Tree Tasks

I need to create a system that allows me to:
- inject unique behaviors into the state tree for each enemy type.
- preserve the overall structure of the state tree between different enemy types

I can implement custom behaviors by:
- Using a custom schema to allow unique variables to be set & guaranteed for each tree
- Using "parallel tree tasks" w/ custom parameters to define unique behaviors for each enemy type that can be injected into the state tree at runtime.

---

![AI Rework Graph](<./AI Rework Graph.png>)
