So, I played around in-engine and tried to find something that could work roughly for the environmental assets. I placed some temporary materials on the assets just to see what would work and what wouldn't.

I was also playing around with the lighting, dithering / pixelation shader, and the fog to get a better idea of what the game would look like in a more finished state.

I did all this on a private branch and didn't push it. If you want me to push it so you guys can look around for yourselves, let me know.


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

### My Takeaways

![](<../../../_Meta/Attachments/Pasted image 20250531060607.png>)

- With the rooms being so large, we'll likely run into issues where large portions of the room have the same texture repeating over and over again (kinda like in the image above). 
