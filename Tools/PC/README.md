![](https://i.ibb.co/SdsfNyD/Head.png)

# T8 Compiler GUI
This app is a very basic front-end for [t7-compiler](https://github.com/shiversoftdev/t7-compiler), by Serious.

It allows users to compile and inject GSC projects for Black Ops 4 without needing to install Visual Studio Code, in a simple GUI format.

### Features
• Compile GSC project folders to "pre-compiled" .gscc files\
• Inject pre-compiled scripts with one-click\
• LazyLink & Detours support\
• Portable app, you just need the .exe file to run it\
• User-selectable themes

### How it works
The app reads .gscc and .gsic files from the `Scripts` folder, which is in the same directory as the .exe itself, and displays them in the drop-down box. If there is no `Scripts` folder, the app will make one automatically.

You just select the script you want to inject from the drop-down box, and click `Inject GSC`. 

If you have a GSC project folder (not compiled), you can compile it to a .gscc file using the `Compile Project` button. Once successfully compiled, it will automatically import it to the `Scripts` folder for you, with a filename of your choosing (just to keep your scripts sorted).

### How to use the app
1. [Download](https://github.com/Jek47/BO4-GSC-Mods/blob/main/Injectors/PC/T8%20Compiler%20GUI.zip) and extract `T8 Compiler GUI.zip` (password is: **Jek47**).

2. [Download](https://github.com/Jek47/BO4-GSC-Mods/tree/main/Zombies%20Mods) the GSC file for the mod you want to play.

3. Make sure that you are on the in-game menu that's relevant to the mod you want to play (not actually in-game yet).

![](https://i.ibb.co/mhkjbD0/Zombies.png)\
*e.g.* if you have a zombies mod, you need to be on this menu.

4. Run `T8 Compiler GUI.exe`

5. If you have a pre-compiled GSC script, you can either drag and drop the file into the `Scripts` folder manually,\
   or you can click the `Import GSC` button and browse for the file.

   Or if you have a GSC project folder, you can compile that to a GSC file yourself by clicking the `Compile Project` button.\
   Once compiled it will automatically import it for you.

![](https://i.ibb.co/hWbRbjv/Step5.png)
   
6. Once you've imported your script, select it from the drop down box on the right-hand side, select your injection point, and click `Inject GSC`

![](https://i.ibb.co/LQprrzk/Step-6.png)

Select your injection point based on the game mode your mod was made for, as per below:\
**Zombies**: *scripts\zm_common\load.gsc*\
**Multiplayer**: *scripts\mp_common\bb.gsc*\
**Blackout / common**: *scripts\core_common\load_shared.gsc*

### Credits
• [Serious](https://github.com/shiversoftdev): for the t7-compiler app itself, without which BO4 modding wouldn't even be possible\
• [ATE47](https://github.com/ate47): for adding LazyLink and Detours support to the compiler, and for help troubleshooting and other queries\
• Pea: for help with various aspects of the creation of this app and help troubleshooting\
• BodNJenie: for help with testing the app on the [Project-BO4 client](https://github.com/project-bo4/shield-development)
