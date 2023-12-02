![](https://i.ibb.co/VYJSgGk/TITLE.png)

# T8 Compiler GUI (v1.2)
This app is a very basic front-end for [t7-compiler](https://github.com/shiversoftdev/t7-compiler), by Serious.

It allows users to compile and inject GSC projects for Black Ops 4 without needing to install Visual Studio Code, in a simple GUI format.

### Features
• Inject pre-compiled scripts with one-click\
• Compile GSC project folders to "pre-compiled" GSC scripts\
• Supports CSC, LazyLink & Detours\
• Portable app, you just need the .exe file to run it\
• User-selectable themes

### Credits
• [Serious](https://github.com/shiversoftdev): for the t7-compiler program itself, without which BO4 modding wouldn't even be possible\
• [ATE47](https://github.com/ate47): for adding CSC, LazyLink and Detours support to the compiler, and for help troubleshooting and other queries\
• [Pea](https://github.com/NotNierPea): for help with various aspects of the creation of this app and help troubleshooting\
• [BodNJenie](https://github.com/bodnjenie14): for help with testing the app on the [Project-BO4 client](https://github.com/project-bo4/shield-development)

### How it works
The app reads GSC scripts from the `Scripts` folder, which is in the same directory as the .exe itself, and displays them in the drop-down box. If there is no `Scripts` folder, the app will make one automatically.

You just select the script you want to inject from the drop-down box, and click `Inject GSC`. 

If you have a GSC project folder (not compiled), you can compile it to a GSC file using the `Compile Project` button. Once successfully compiled, it will automatically prompt you to import it to the `Scripts` folder, with a filename of your choosing (to help differentiate your compiled scripts). If you enable auto inject, it will automatically inject it for you once it has been compiled.

### How to use the app
1. [Download](https://github.com/Jek47/BO4-GSC-Mods/blob/main/Tools/PC/T8%20Compiler%20GUI.zip) and extract `T8 Compiler GUI.zip` (password is: **Jek47**).

2. Download the GSC script or the project folder for the mod you want to play.\
   I have a few pre-compiled mods [here](https://github.com/Jek47/BO4-GSC-Mods/tree/main/Zombies%20Mods) for you to try out.

3. Make sure that you are on the in-game menu that's relevant to the mod you want to play (not actually in-game yet).

![](https://i.ibb.co/mhkjbD0/Zombies.png)\
*e.g.* if you have a zombies mod, you need to be on this menu.

4. Run `T8 Compiler GUI.exe`

5. If you have a pre-compiled GSC script, you can either drag and drop the file into the `Scripts` folder manually,\
   or you can click the `Import GSC` button and browse for the file.

   If you have a project folder, you can compile that to a GSC file yourself by clicking the `Compile Project` button and browsing to the location of your project folder (make sure you select the folder that contains your `gsc.conf` as well as the scripts for your mod).
   
   Once compiled it will ask you to give it a name, and then automatically import the compiled script for you.
   
7. Once you've imported your script, just select it from the drop down box on the right-hand side.\
   Select your game mode, and click `Inject GSC`

   You should get a message telling you that your script was injected successfully.

![](https://i.ibb.co/rvPQH8K/STEP6.png)

### Notes:
• If the mod you're using has both a **.gscc** and a **.cscc** file, make sure you choose the **.cscc** script from the drop-down box when you inject.

Otherwise if you select the **.gscc** script, it will only inject that part, and not the .cscc part as well. 

• The game mode you select controls which script gets hooked during injection:\
**Zombies**: *scripts\zm_common\load.gsc*\
**Multiplayer**: *scripts\mp_common\load.gsc*\
**Common**: *scripts\core_common\load_shared.gsc - (should work for all game modes)*

• Ticking the `Detours` box will enable advanced features within the compiler, but they rely on you running the [Project-BO4](https://github.com/project-bo4/shield-development) client to work. If you're not running Project-BO4, enabling detours **will crash your game**. 

If your GSC script does not use detours, then just leave the box unticked.\
If your script does use detours, you'll need to tick the box and make sure you're running the client.

• Windows Defender and/or other anti-virus programs might flag the app as a Trojan, this is a false positive.\
The app is a front-end for the t7-compiler program, created by Serious, a trusted scene developer.

Since the compiler is modifying the memory of the game while it's running, it will trigger some anti-virus programs.\
You may need to make an exception for the app in your anti-virus settings.

The source code of the compiler that this app uses is [here](https://github.com/ate47/t7-compiler/tree/dev_csc_inj).

### Version History:
#### Version 1.2
• Fixed an oversight when injecting csc scripts\
• Compiler will no longer print MOTD, speeding up compiling and injecting scripts

#### Version 1.1
• Added .cscc and .csic inject support (thanks ATE47 for updating the compiler... again)\
• Added a "check for newer versions" button to the Version History page\
• Fixed a couple of bugs and inconsistencies

#### Version 1.0
• Public release

#### Version 0.2
• Added a new button that "un-injects" any GSC mods that you are currently running\
• Added tooltips to all the buttons and tickboxes on the app\
• Fixed a couple of UI bugs

#### Version 0.1
• Initial "beta" release, sent out to a few community members for feedback

### //

If you've read this far, there's a hidden settings panel on the `About` page, maximize the page to see it.\
Here you can change the theme of the app, disable the detours warning message and enable the console for troubleshooting.\
Any settings I add to the app in the future will probably end up here.
