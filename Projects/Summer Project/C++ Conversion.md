I've been working on a separate branch to convert the project to C++, and now I'm ready to merge it into main. The thing is, not everyone's computer is set up to work with a C++ project. So, I put together a little tutorial to help them get started.

The tutorial is based off of this video, so you should watch it and follow along with the steps in this doc: <https://www.youtube.com/watch?v=WaBVxtG4xdY>

# Step 0: BEFORE Pulling the C++ Commit
At the time of writing this, I probably haven't even pushed the C++ commit yet. But, before you pull (while you can still open the project), do this first.

If you pulled the C++ commit before doing this, I'm sure you'll be fine. If the project doesn't open, you'll just have to do this step at the end.

1. Open Unreal
2. Open the project
3. Go to Edit > Editor Preferences
4. Look up "Force Compilation at Startup"
	1. This makes it so that every time you open the project and there has been a change to the C++ code, Unreal will recompile the code automatically. This is super useful for us since we will be making changes to the code frequently.
5. Enable it
6. Close Unreal

# Step 1: Installing Visual Studio

From this step onward, you don't need to have pulled the C++ commit, but the only way to test if really works is by opening a version of the project with C++.

1. On your computer, open the "Visual Studio Installer"
	1. You may already have it installed. If not, you can download it from <https://visualstudio.microsoft.com/downloads/> (Download the *purple* one, NOT the blue one)
2. If you already have Visual Studio 2022 installed, you'll see a screen like this: ![](<../../_Meta/Attachments/Pasted image 20250609160450.png>)
	1. Click modify if you already have it installed
3. If you don't have it installed, or if you clicked "modify", you should see a screen like this: ![](<../../_Meta/Attachments/Pasted image 20250609172721.png>)
4. Here, we need to make sure all the correct components are installed.
	1. .Net Desktop Development
	2. Desktop Development with C++
	3. Windows Application Development
	4. Game Development with C++
5. In the side bar to the right, make sure the following components are checked:
	1. windows 11 SDK. It should be one of the ones circled in red. You ONLY need one of them. Really, I recommend the newest Windows 11 SDK (even if you don't have Windows 11) ![](<../../_Meta/Attachments/Pasted image 20250609172849.png>)
6. Install. This is gonna take a little while

# Step 2: Pull the C++ Commit

1. This is exactly what it sounds like. Pull the C++ commit from the repo (If it even exists yet)
2. If the C++ has NOT been pushed yet, you can instead switch to the branch called `feature/c-plus-plus` for the rest of the steps

# Step 3: Generate Visual Studio Project Files

Make sure your visual studio is done installing before you do this step.

1. In your file explorer, navigate to where the project is located
2. Right click on the `.uproject` file
3. Click "Generate Visual Studio Project Files". Be a little patient, it might seem like your computer isn't doing anything for a sec. ![](<../../_Meta/Attachments/Pasted image 20250609172024.png>)
4. If it fails to generate it will tell you with an error message. Try again a couple times. If it STILL doesn't work… ah man. dm me

# Step 4: Open the Project

1. Once the files are done generating, the project *should* be compiled properly
2. Open the `.uproject` file or open up the game from the Epic Games Launcher
3. it *should* work
4. If not, dm me
