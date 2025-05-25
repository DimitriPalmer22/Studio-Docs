Sometimes, as devs, we need to add extra functionality for debugging purposes.
- This could be showing debug information on the screen

I have made some an Actor Component that allows for added functionality whenever debug mode is turned on or off.

# Turning Debug Mode On And Off

- I made a simple console command in Unreal to turn debug mode on and off
- to turn debug mode on, simply type `SetDebugMode true` in the console
- to turn debug mode off, simply type `SetDebugMode false` in the console

# How to Add Debug Mode Support for a Blueprint

1. On your blueprint, add a component called `BP_DebugComponent`
2. In the event graph of your blueprint, click on the `BP_DebugComponent`
3. With the `BP_DebugComponent` selected, go to the details panel and find the `Events` section
4. Click the `+` button next to `OnDebugModeOn` and `OnDebugModeOff` to add the events to your blueprint
5. From here, you can add any functionality you want to happen when debug mode is turned on or off
6. Also, as an added note, the `BP_DebugComponent` has a function called `IsDebugModeOn` that returns a boolean that indicates whether debug mode is on or off.
	1. You can use this function to check if debug mode is on or off and add functionality accordingly
