# Texture Color Reduction

- As a final step before importing the textures into Unreal, we need to reduce the color depth of the textures to help give them a more old-school look.
- This creates a dithered effect that makes the textures look less smooth and more pixelated.
- After looking it up online, there were two ways I've seen it done in Photoshop

### Method 1: Indexed Color (Probably Better)
- In the top bar, select Image > Mode > Indexed Color
- The only setting that NEEDS to be consistent is the "Dither" setting, which should be set to "Pattern" to get that gridded dither effect.
- For the number of colors, I've experimented with 16 and 32, but you can go for whatever you think looks best. I will say, though, reducing the colors too much, especially on an image with a wide range of colors, can make the image look weird.
- Here are the settings I've used with some of the character portrait references, you can experiment with these to see what works best.
![](<../../../_Meta/Attachments/Pasted image 20250518160608.png>)

### Method 2: Save For Web (Legacy)
- In the top bar, select File > Export > Save for Web (Legacy)
- For this method, you should change the image type to "GIF" and change the dithering type to "Pattern"
- I, personally, try 
# Texture Import Settings
![](<../../../_Meta/Attachments/Pasted image 20250518154551.png>)

### Mipping
- In the level of detail section, make sure the "mip gen settings" are left at whatever default value Unreal puts it at.
- Most of the values here are fine, just as long as you don't accidentally select "NoMipmaps", which causes some weird aliasing issues with the textures.

### Compression
- Since the textures themselves are already going to be 128x128 or 256x256 when we put them in-engine, we shouldn't need to compress them any further.
- However, if you do want to compress any high-res texture into a lower resolution, you can change the "Maximum Texture Size" setting under the advanced portion of the "Compression" section to 128 or 256.

![](<../../../_Meta/Attachments/Pasted image 20250518155031.png>)

### Filtering
- This is something you NEED to change.
- Normally, Unreal uses a default value defined by some configuration files somewhere. However, this default value adds unwanted filtering to the textures, making them look blurry.
- Change the "Filter" setting under the "Texture" section to "Nearest" to disable this filtering.
