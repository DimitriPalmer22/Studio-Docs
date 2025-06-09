I've been working on a separate branch to convert the project to C++, and now I'm ready to merge it into main. The thing is, not everyone's computer is set up to work with a C++ project. So, I put together a little tutorial to help them get started.

The tutorial is based off of this video, so you should watch it and follow along with the steps in this doc: <https://www.youtube.com/watch?v=WaBVxtG4xdY>

# Step 0: BEFORE Pulling the C++ Commit
At the time of writing this, I probably haven't even pushed the C++ commit yet. But, before you pull (while you can still open the project), do this first.

1. Open Unreal
2. Open the project
3. Go to Edit > Editor Preferences
4. Look up "Force Compilation at Startup"
	1. This makes it so that every time you open the project and there has been a change to the C++ code, Unreal will recompile the code automatically. This is super useful for us since we will be making changes to the code frequently.
5. Enable it
6. Close Unreal

# Step 1

From this step onward, you don't need to have pulled the C++ commit, but the only way to test if really works is by opening a version of the project with C++.

1. On your computer, open the "Visual Studio Installer"
	1. You may already have it installed. If not, you can download it from <https://visualstudio.microsoft.com/downloads/> (Download the *purple* one, NOT the blue one)

If the C++ commit has not been pushed by the time you are reading this and you want to test if the project works, close
