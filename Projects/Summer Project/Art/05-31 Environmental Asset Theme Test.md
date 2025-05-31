So, I played around in-engine and tried to find something that could work roughly for the environmental assets. I placed some temporary materials on the assets just to see what would work and what wouldn't.

I was also playing around with the lighting, dithering / pixelation shader, and the fog to get a better idea of what the game would look like in a more finished state. Also, I turned off the outline shader since it doesn't really fit the aesthetic we're going for (it was also clashing really bad with the fog)

I did all this on a private branch and didn't push it. If you want me to push it so you guys can look around for yourselves, let me know.

FULL DISCLAIMER: I don't think this looks that good, but it just represents the idea of what we can do for the assets for right now.

![](<../../../_Meta/Attachments/Pasted image 20250531054050.png>)

> Medium Lighting, Fog on, Dithering + Pixelation Shader on

![](<../../../_Meta/Attachments/Pasted image 20250531053927.png>)

> High Global Illumination, Fog on, Dithering + Pixelation Shader on

![](<../../../_Meta/Attachments/Pasted image 20250531054456.png>)

> High Global Illumination, Fog on, Dithering + Pixelation Shader on

![](<../../../_Meta/Attachments/Pasted image 20250531054640.png>)

> Medium Global Illumination, Fog off, Dithering + Pixelation Shader off

![](<../../../_Meta/Attachments/Pasted image 20250531054616.png>)

> High Global Illumination, Fog off, Dithering + Pixelation Shader off

![](<../../../_Meta/Attachments/Pasted image 20250531054724.png>)

> High Global Illumination, Fog on, Dithering + Pixelation Shader on

![](<../../../_Meta/Attachments/Pasted image 20250531061818.png>)

> High Global Illumination, Fog on, Dithering + Pixelation Shader on

### My Takeaways

![](<../../../_Meta/Attachments/Pasted image 20250531060607.png>)

- With the rooms being so large, we'll likely run into issues where large portions of the room have the same texture repeating over and over again (kinda like in the image above).
	- If we're going to be using gray brick for the walls and floors, this is going to be an even bigger issue since gray is just so ugly and bland.
	- One of the biggest things that makes the issue so apparent in the image above is the fact that the texture is tiling A LOT.

![](<../../../_Meta/Attachments/Pasted image 20250531061204.png>)

- If I increase the size of the texture and make it tile less, the wall seems a little bit less like a sea of gray (the issue is still there though).

Honestly, after playing around in-engine with a couple different sets of materials, I figured that having too much stone would make the levels seem too dungeon like or castle-like. The stone base is fine, but we should probably break a lot of the stone portions up with wood.

As we get further into development, we can get more pieces in the kit to add small details and break up the monotony of the textures. But for now, I think we should focus on getting a good base down that looks good enough to play with.

**For these reasons, I think we should go for something with a lot of wood framing + a stone base instead of primarily using brick & adding wooden accents** (My bad, I know I said before we'd do the brick + wood accemts, but I thought about it some more and changed my mind)

![](<../../../_Meta/Attachments/Pasted image 20250531065830.png>)

There's also the possibility of having too much wood in one area. If some of the props are made of wood and too many of them are in one area, then that could clash with the wood in the environmental assets as well.

### The References

![](<../../../_Meta/Attachments/Pasted image 20250531070334.png>)