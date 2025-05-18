
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