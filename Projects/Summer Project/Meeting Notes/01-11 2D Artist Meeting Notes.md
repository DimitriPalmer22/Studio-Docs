### Pause Menu

![](<../../../_Meta/Attachments/Pasted image 20260111182104.png>)

This is the *current* pause menu.

The revised pause menu should have options for:
- Resume
- Codex
- Settings
- Restart
- Main Menu

### Settings Menu?

We need this to be flexible, as I'm not sure of ALL the options we want to have in here yet. Consider than any page is probably going to be scrollable. 

#### Required UI Pieces
To build the settings menu in-engine we need:
- Buttons for the different tabs (pressed, not pressed)
- Vertical Scroll bars (background fill, handle) 
- Sliders (background fill, foreground fill, handle)
- Checkboxes (checked, unchecked)
- Dropdown menus (background, options list background, option selected, option not selected)

#### The Different Tabs
Right now, the settings menu has tabs for: "Video", "Audio", "Controls", and "Credits". The credits tab ***WILL BE REMOVED FROM THE SETTINGS MENU***.

Here are the tabs we actually need:
- Gameplay - Options for toggling subtitles, changing difficulty, toggling tutorials, idk, etc.
- Video - Options for resolution, fullscreen/windowed, graphics quality, etc.
- Audio - Options for master volume, music volume, sfx volume, voice volume, etc.
- Controls - A place to LOOK AT the game's controls and rebind them (for both keyboard and controller)

#### The Video Settings Page
![](<../../../_Meta/Attachments/Pasted image 20260111184954.png>)
Current "Video" Settings page.

The video settings page is going to have all the options listed above. 

#### The Audio Settings Page

![](<../../../_Meta/Attachments/Pasted image 20260111185437.png>)
Current "Audio" Settings page.

There may be more options added here later, but for now, this is fine.

#### The Controls Settings Page

![](<../../../_Meta/Attachments/Pasted image 20260111185558.png>)
Current "Controls" Settings page.

There *Are* more keybinds than this currently available, so this page may need to be scrollable.

Additionally, we need to add controller support for rebinding keys as well. So, there would need to be another column for controller inputs.