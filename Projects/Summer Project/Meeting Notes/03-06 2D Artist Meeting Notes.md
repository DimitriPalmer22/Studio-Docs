# 03-06 2D Artist Meeting Notes

## In-Game HUD

Reference board: <https://miro.com/app/board/uXjVGJb2XGs=/>

### Breathability

The HUD in general takes up too much space on the screen and can make the game feel a little claustrophobic at times. We should try to make the HUD a little more minimal and less intrusive on the screen. This will allow the player to focus more on the game and less on the HUD.

I think this is because the HUD feels like it has some wasted space in it, and kinda walls off the top left corner of the screen.

![](<../../../_Meta/Attachments/Pasted image 20260306160323.png>)

### Communication of Information

In concept, the ribbon idea as we had it was pretty cool. Having the "addendums" pop up as they activate and then stay on the screen for a little while is a pretty good way to communicate to the player what addendums they have active and what they do. 
- However, the way we had it set up, it was pretty intrusive on the screen and made it hard to see what was going on in the game.
- Also, without intimate knowledge of each of the addendums in the game, it made it a little difficult to know which ones were active.
- Also, the player isn't necessarily going to be looking at their HUD in the middle of combat, so having the addendums pop up there isn't necessarily the best way to communicate to the player what they have active.

### Possible Solutions

Reduce padding to get the UI even more out of the way.

For the bars (health, mana, and shield), I think we should make the orb (for the shield) a little bit smaller. Then, we can make the health and mana bars take tall enough in total to pretty much fill up the space the orb takes up vertically.

The mana essence counter does not need to be under the HUD like this. We can move it to the top right or bottom left corners of the screen.

The primary and secondary abilities can stay where they are. Maybe we can shrink those down a little, too.

The ribbon. The ribbon is probably the biggest concern since, no matter what, it is gonna obstruct a lot of the player's view if it is on the screen and is fully extended. Hades tends to keep their boons floating in the middle of the left side of the screen, which is a little better than having a UI element extend down from the top of the screen. But, if we're trying to keep the ribbon, I don't really know how we can make it less intrusive.

We *could* just put the bars at the bottom left.
We could have the addendums be horizontally stacking instead of vertical.
- If we did make these horizontally stacking and moved them, we might need a new housing thing for them.

### What Elements Are Needed for Our HUD?

- Health Bar
- Mana Bar
- Shield Bar

- Primary spell
- Secondary spell
- Slotted Addendums

- Mana essence (currency)

## Font

We need a font that we can use throughout the game that looks a little **better**. The existing font can be a bit hard to read at times and doesn't fully match the art style of the game.

Current Font: [Alkhemikal](https://www.dafont.com/alkhemikal.font?text=This+is+the+dialogue+that+plays+the+very+first+time+you+enter+any+standard+enemy)

#### Possible Fonts

- [x] [Dico Font](https://www.dafont.com/dico.font?text=This+is+the+dialogue+that+plays+the+very+first+time+you+enter+any+standard+enemy)
- [Pixelated English](https://www.dafont.com/pixeled-english.font?text=This+is+the+dialogue+that+plays+the+very+first+time+you+enter+any+standard+enemy)
- [Venice Classic](https://www.dafont.com/venice-classic.font?text=This+is+the+dialogue+that+plays+the+very+first+time+you+enter+any+standard+enemy)
- [x] [Belanidi Serif](https://www.dafont.com/belanidi-serif.font?text=This+is+the+dialogue+that+plays+the+very+first+time+you+enter+any+standard+enemy)
- [x] [Alagard](https://www.dafont.com/alagard.font?text=Interact&back=bitmap)
- [Modern Dos](https://www.dafont.com/modern-dos.font?text=This+is+the+dialogue+that+plays+the+very+first+time+you+enter+any+standard+enemy)
- [GothicPixels](https://www.dafont.com/gothicpixels.font?text=This+is+the+dialogue+that+plays+the+very+first+time+you+enter+any+standard+enemy)

### Dialogue Screen UI

- Shrink the dialogue UI a little?
- Move the text a little down to avoid the nameplate encroaching on the text.

## Addendum Screen UI

No references, but I can outline the task.

- Addendum screen paper update. Make it an actual asset.
## Character Portrait Updates

Reference board: <https://miro.com/app/board/uXjVGJb2XGs=/>

The main feedback we got about the character portraits is that they aren't dynamic enough.
- The shading wasn't dynamic enough
- The poses weren't dynamic enough

### Lighting & Shading

- Removed dithering
- More shading

### Posing

One of the main bits of feedback we got from people about our game's character portraits is that their poses aren't dynamic enough.

If we were to update the posing for these characters, we'd want to express more *personality* through the posing.

---

## Portraits
### Shading

![](<../../../_Meta/Attachments/Pasted image 20260306171652.png>)
Thicker outlines, more dynamic shading.

### Posing
 Have more concrete examples of poses.

- Which characters already have decent poses? We can get started on those first.
- Which peoples' poses need to be redone and how exactly?

## In-Game HUD

- We'll move the bars to the bottom left
- Shrink the bars to not go over the line established by the icons in the bottom right
- We'll either remove or move the addendums
- See how we feel about that.