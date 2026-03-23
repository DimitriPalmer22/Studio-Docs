# 03-23 Meeting Notes

## Meeting Times

| Meeting                         | Possible Times |
| ------------------------------- | -------------- |
| LD Meeting                      |                |
| Narrative Designer + CD Meeting |                |
| Sound Meeting                   |                |
| Environmental Artist Meeting    |                |
| 2D Artist                       |                |
| Animation Meeting               |                |
| Character Artist Meeting        |                |

## Updates To The Game

Last week's main goals were primarily:
1. ***Improve player combat***
2. ***Improve level design & atmosphere***
3. ***Figure out more 2D Art & Overall Presentation***
4. ***Complete the next enemy's model***

Some of these things still need to be expanded upon, but we've made good progress on all these fronts.

### Player Combat Animations

Allister's animations for the "*Flame Volley*" spell have been updated to feel much heavier and more impactful. From this point on, most of the animations we get for Allister should feel like this.

#### Update to the Secondary Spells

**Before**: You could hold the secondary button and charge up the secondary spell for 3 tiers of power, each one stronger than the last and potentially with a different / modified effect.

This didn't flow well with the pacing of the game and often led to the player getting hit because charging took too long.

**Now**: You can hold the secondary button to charge up the secondary spell. But, there is only 1 extra tier of power. So, you can quickly tap the secondary button for a quick cast of the spell, or you can hold it down for a stronger version of the spell.
- [ ] Time briefly slows while charging as well

#### Background Elements in Levels

We've experimented with adding more background elements to the existing levels to give the game a little more atmosphere and life. Examples can be found in:
- L_Area01_Boss
- L_Area01_Room02

#### De-Square-ing the Levels

We've been making efforts to make the poly counts of the environments a little higher so we have more depth and detail in the environments. Here is the progress so far:
- L_Area01_Room03

The idea is to have a more detailed environmental kit that allows us to get a little more creative with the rest of the levels that need to be made (also will help w/ the existing levels).

#### Updated Portrait Style

Going forward, the portraits in the game will be updated to have more detailed shading.

#### UI Stuff

#### Font

Font in the game has been updated to be a little more readable. The font is still stylized, but it's not as difficult to read as the previous font.

- [ ] Dico

#### Other Small Stuff

- Shrunk the dialogue UI a little to allow for less of the screen to be obscured during dialogue sequences.
- Vignette instead of black bars whenever the dialogue UI is up.

### Updated Props

- Revised pedestal asset
- New writing desk asset
- New tome altar model

## Plans Going Forward

This week's goals are primarily:
1. ***Expand the game's meta-progression & narrative***: The rogue-lite aspects of the game (the things that carry over BETWEEN runs) are underdeveloped / unimplemented right now. As a result, this doesn't feel like a game.

### Bug Tracking

If you ever see a bug / a feature not working properly / a small oversight in the game, you can submit a bug report to our bug tracking system. It takes like 10 seconds. This will allow us to keep track of all the bugs in the game and prioritize them accordingly.

Link: <https://forms.clickup.com/90131425169/f/2ky40twh-3873/ZFSTRRZKQYU57356US>

### Meta-Progression & Narrative Expansion

#### Portrait Stuff

- Reshade the rest of the portraits.
- Keep poses the same

#### Journal Stuff

The crux of the game's narrative is the meta-progression (the things that carry over between runs). In our case, the only implementation of this is the journal entries, which are collected by Allister and recorded by Tarun. BUT, the journal system has been very minimally implemented so far.

The game's meta-progression revolves around the journal entries that Allister collects during his runs. These journal entries are recorded by Tarun and some contain objectives that the player needs to complete to progress through the game.

I want to start implementing the journal system a little more so we get a more complete narrative experience.

### Narrative Demo Level

I'll make a level containing several things we can use to rapidly iterate on the game's dialogue and progression mechanics. This will allow us to test out different dialogue options and different ways of communicating the game's narrative to the player without having to worry about the level design or the combat mechanics.

### Misc

#### Bookshelves

- Fix the Z-fighting on the bookshelf model.
- Retexture the bookshelves to use a better wood texture.
