The following levels need to be set up properly to be added to the pool of levels in the game:
- `Level2_Aiden`
- `MikelPOCLevel_Aiden`
- `Brian5thLevel`
### Preparing Your Levels to Be Put in the List of the Game's Levels

> Lowkey, you can open `BrianKit3_POCCopy` and see how that is set up as an example. In the level, if you look at the `00_Gameplay/Room` folder, you can see all the actors that are necessary to make the room run.

#### 1.Make Sure You Have a BP_RoomManager Actor
- Drag a `BP_RoomManager` anywhere into your level.
- This actor is responsible for managing the room's state in the background.

#### 2. Replace the PlayerStart Actor (If You Have one)
- Delete the existing PlayerStart actor in your level
- Replace it with `BP_RoomPlayerStart` actor
- This is where the player spawns from upon entering the room

#### 3. Make Sure You Have a BP_RoomPlayerEnd Actor
- In your level, place a `BP_RoomPlayerEnd`.
- This is the teleporter the player steps on to exit the room

#### 4. Make Sure You Have a BP_RoomDialogueManager Actor
- Place a `BP_RoomDialogueManager` anywhere in your level.
