﻿
# How to set root folder manually

By default Scene Forge locates and loads its assets automatically by searching for the **Scene Forge** folder by name and compares its content. If for some reason this fails the function will throw and error like this **"Unable to locate Scene Forge root folder. Check documentation on how to set it manually"** and will turn off the tool.

1. Locate the Scene Forge root folder in your project. The folder is called **"Scene Forge"**.

2. Right click on the folder in the Unity Project View and select **Show in explorer**

3. Locate a file called **Scene Forge.meta** and open it

4. Copy the **GUID** from the file, it looks like this **0068e01dd7a815340a908784b438eabf**

5. Inside the Scene Forge folder go to **Assets/Scripts** and open **SF_Prototyping**. You can open it using Notepad if you don't have an editor, its a very simple change.

6. At the top you will find two variables:
	**static bool MANUAL_GUID = false;
	static string FOLDER_GUID = "0068e01dd7a815340a908784b438eabf";**

7. Change **MANUAL_GUID** to **true**, like this **static bool MANUAL_GUID = true;**

8. Replace the **FOLDER_GUID** string with the one you copied, make sure that **"** remain at the start and end of the string.

9. Save the changes and enable the tool from the top bar **Tools/Scene Forge/Enable** or by pressing **F5**

11. If the error is still present you can try and reinstall the tool. Additionally you can find help in our [Discrod](https://discord.gg/9rUWFx9vxh).

# HDRI Heaven skyboxes

Links to the HDRIs used in the Time of Day Presets for URP. All HDRIs are from [HDRI Heaven](https://hdri-haven.com/).
 
- ### [Dawn](https://hdri-haven.com/hdri/clear-sky-afternoon-sky-dome) 
- ### [Dawn Foggy](https://hdri-haven.com/hdri/cloudy-sunset-sky-dome)
- ### [Day](https://hdri-haven.com/hdri/clear-sky-dome)
- ### [Dusk](https://hdri-haven.com/hdri/clear-sky-sunset-sky-dome)
- ### [Night and Dark Night](https://hdri-haven.com/hdri/starry-night-sky-dome)

*All HDRIs listed in HDRI Heaven are licenced as CC0 and can be downloaded instantly and anonymously, giving you complete freedom and privacy. No payments, no premium accounts, no donationware. No restrictions in use.*

# How will the tool change my project?

Upon importing, the package will be placed inside the **Editor** folder in your project. Once there a manager script will create another folder called **"SceneForge"** in your project and move several scripts there. This is done in order to allow for those scripts to be instantiated (you can't instantiate mono scripts from the Editor folder).

- **Your Project Folder/Assets/Editor/Scene Forge** (The majority of scripts and assets)
- **Your Project Folder/Assets/SceneForge** (Several mono behavior scripts)

### Building your project

When building your project Unity ignores everything that is inside the **Editor** (Assets/Editor) folder. The scripts inside **Assets/SceneForge** are made to only execute inside the editor, so in theory there will not not cause any issues. Though **I do not** recommend leaving them inside your scenes as they are only used in the editor. In order to clean them from your scenes before build, check **Package Clean Up** page in this documentation.





