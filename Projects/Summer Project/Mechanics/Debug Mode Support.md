Sometimes, as devs, we need to add extra functionality for debugging purposes.
- This could be showing debug information on the screen

I have made some an Actor Component that allows for added functionality whenever debug mode is turned on or off.

# Turning Debug Mode On And Off

- I made a simple console command in Unreal to turn debug mode on and off
- to turn debug mode on, simply type `SetDebugMode true` in the console
- to turn debug mode off, simply type `SetDebugMode false` in the console

# How to Add Debug Mode Support for a Blueprint

1. On your blueprint, add a component called `BP_DebugComponent`
2. Once you do that,
