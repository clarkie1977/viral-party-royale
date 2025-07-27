Step-by-Step Guide: Setting Up VS Code for Roblox Development
1. Install the Required Tools

Download and install Visual Studio Code (VS Code).
Download Rokit from GitHub. Rokit manages Rojo, Wally, and other tools.
Extract Rokit and run the .exe file to install. If Windows warns you, you can ignore it (it’s a common warning for new apps).
Restart your computer after installing Rokit.
2. Set Up Your Project Folders

Create a folder for all your Roblox projects (e.g., Documents/RobloxProjects).
Inside that, create a folder for your game (e.g., Documents/RobloxProjects/Tutorial).
3. Open Your Project in VS Code

Launch VS Code and open the game folder you just created.
4. Install VS Code Extensions

Luau Language Server: For Roblox scripting language support.
Rojo: To sync VS Code with Roblox Studio.
(Optional but recommended) Selene (linter) and Stylua (code formatter).
5. Initialize Your Project

Open the terminal in VS Code.
Run the following commands (one at a time):
rokit init
rokit add rojo
rojo init
This sets up your project and creates the necessary files.
6. Configure Rojo

Edit the generated default.project.json file:
Remove everything under workspace unless you want Rojo to control those instances.
All your code should go under the src (source) folder.
7. Install the Rojo Plugin in Roblox Studio

In VS Code, press Ctrl+Shift+P, search for “Rojo”, and open the Rojo menu.
Install the Rojo plugin in Roblox Studio (restart Studio if it’s already open).
In Studio, click the Rojo plugin and connect to your project.
8. Live Syncing

Click the green arrow in the Rojo plugin to start live syncing.
Any changes you make in VS Code will now sync to Roblox Studio when saved.
9. Set Up Linting and Formatting (Optional but Recommended)

Selene: Create a selene.toml file in your project with the basic config (see Selene docs).
Stylua: Configure auto-formatting on save by editing your VS Code settings (instructions in the video description).
10. Enable Auto Imports

Go to the Luau Language Server settings in VS Code.
Find the “imports” option and enable it for better code suggestions.
11. Set Up Wally (Package Manager)

In the terminal, run:
rokit add wally
rokit add wally-package-types
This creates a wally.toml file. Add packages by copying their paths from Wally’s website and pasting them under the [dependencies] section.
To install packages, run:
wally install
Update your default.project.json to include the new package folders under ReplicatedStorage and ServerScriptService.
12. Set Up Git for Version Control

Download and install Git.
Create a GitHub account if you don’t have one.
In VS Code, open the terminal and configure Git with your username and email (see video description for commands).
Initialize a Git repository in your project.
Add a .gitignore file to exclude installed packages and auto-generated files.
Commit your changes and publish to GitHub for backup and collaboration.