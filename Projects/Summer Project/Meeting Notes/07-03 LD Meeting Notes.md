### Materials

#### You Guys Have Been Using Materials in Unreal WRONG
You're not really supposed to be using the "Material" Asset directly. You should be using ***material instances*** instead.
- In Unity, whenever we put a material on something, we made a a shader / shadergraph first. Then, from the shader / shadergraph, we made a material.
- In Unreal, this is the same thing. The only differences are that "Materials" in Unreal = "Shadergraphs" in Unity and "Material Instances" in Unreal = "Materials" in Unity.

#### Why is This an Issue?

The more "Materials" that are in the project, the longer the project will take to open / build. This is because Unreal is compiling the shader code for each material.

Also, if we have multiple materials that we want to look / behave the same, we would have to change all of them individually. This is a pain. If we use material instances, we can change the parent material and all of the material instances will update automatically.

#### Further Explanation for the Proper Workflow

Material assets are essentially supposed to be used to:
- establish the base look for an object (should it be shiny, rough, metallic, etc.)
- create the different settings and parameters that you can later tweak in the material instances, such as the texture asset, the scale of the texture, the shininess, etc.

Material instances are lightweight assets that inherit from a parent material. They allow you to easily change the settings and parameters established in the parent material without having to create a new material completely from scratch.

#### Naming Conventions

- Materials should have the prefix "M_".
- Material Instances should have the prefix "MI_". NOT Materials

#### Putting Materials on Objects

I noticed that you guys are placing the material instances on static meshes in the level individually rather than on the static mesh assets themselves. This is not how you should be doing it.

You should be placing the material instances on the static mesh assets themselves. This way, when you place the static mesh in the level, it will automatically have the correct material instance applied to it. And, if you ever need to change the material instance, you can do so in one place and it will update everywhere the static mesh is used.

With the way you guys are doing it, if you ever need to change the material instance, you would have to go through every single static mesh in the level and change it individually. This is a pain and should not be done.

### Some of Your Levels Have the Wrong Objects in Them

Old post-process volumes, sky spheres, and other objects that are not supposed to be in the level are in some of your levels. There are new & updated blueprints for these objects that you should be using instead.

The blueprints can be found in `/All/Game/Avernoth/Placeables/LevelVFX`

### Consistent Level Organization

We need some type of system for organizing the levels so that they are easy to navigate and understand for anyone and EVERYONE. Folders are the key to this. It would really help if the base hierarchies of the levels were consistent across all levels.

We can try to organize levels like this:

```
Root
├─ 00_Gameplay (Actors that control gameplay)
│    ├─ Room
│    ├─ Logic (Triggers, Volumes, Blueprints)
│    └─ …
├─ 10_Environment (Visual Assets)
│    ├─ StaticMeshes
│    ├─ Decals
│    └─ …
├─ 20_Lighting 
│    ├─ Global Lighting
│    ├─ Level Lighting
│    └─ …
├─ 30_Characters (Enemies and NPCs)
│    ├─ Enemies
│    └─ …
├─ 40_FX (VFX and SFX placed in the level itself)
│    └─ …
├─ 50_Cinematics 
│    └─ …
├─ 90_Debug (Anything related to debugging)
     ├─ …
```

### "How Do I Play The Game?"

Up to this point, I haven't actually set up a *real* way for you guys to play the game as-intended. It's mostly been a bunch of levels you guys can play individually and that's it.

What I do is I open the `HubRoom_POC` level, which is the temporary "hub room" for the game. From there, I can start the game.

### How Exactly Do the Game's Levels Work in the Back-End / How Do I Make My Level Spawn in the Game?

> Note: This is all still very temporary. If I get the chance to set up a better system / workflow, I will. But for now, this is how it works.

The game is architected in a very particular way to support our game's procedural generation and level design. Here's a brief overview of how it works:
- You guys make a level.
- At first, this level is NOT included in the list of levels that the game can spawn in randomly.
- To do that, there are TWO things that need to happen (*TO AVOID MERGE CONFLICTS, YOU CAN ONLY DO THESE WITH EXPRESS PERMISSION*):
	- 1. **Allow the level to be streamed in**: Open the `PersistentLevel_P` level. Open the "levels" window (In the top menu, go to `Window > Levels`). At the top of the levels window, click on the "levels" dropdown and add existing. Then, add your level in. Boom, now your level *can* be loaded, but that does not mean it will yet.
	- 2. **Add the level to the list of levels to choose from**: Navigate to the `/All/Game/Avernoth/Maps/RoomCollections/FloorInfo` folder. Open up the asset that represents the area you want to add the level to (area 1, 2, or 3). Here, we have dropdowns for the different room types. For the room type you want to add your room to, click the plus, then select your level from the dropdown. Now, your level will be considered for spawning in the game. Optionally, you can select a spawn weight to make your room appear more or less often, but keep it at 1.
- Now, when you play the game, your level will be considered for spawning in the game. You can test this by playing the game from the `HubRoom_POC` level.

### What Does My Room Need To Work Properly?

- In the `00_Gameplay` folder, create a subfolder called "Room". This is where all the room-specific blueprints will be. It should have the following:
	- BP_RoomManager
	- BP_RoomDialogueManager
		- Make sure to set the "RoomManager" variable in the details panel!
	- BP_RoomPlayerStart
	- BP_RoomPlayerEnd
		- Make sure to set the "RoomManager" variable in the details panel!
### Setting up the Enemies
- There are 3 things you need to do to set up enemies in your levels:
	- 1. Place a set of enemies in the `30_Characters` folder. Make sure these are one of the enemy blueprints we have already set up.
	- 2. In the same folder, add a BP_RoomEnemyManager blueprint. This is responsible for managing the enemies in each wave of enemies.
		- Click on the BP_RoomEnemyManager
		- In the details tab, under the section that says "Enemy Management", you need to add all the enemies of that wave into the "Managed Enemies" array.
	- 3. Then, in your level, find the BP_RoomManager and click on it.
		- In the details tab, there is an array for Enemy Managers.
		- Add all of the enemy managers you created in the previous step to this array.
