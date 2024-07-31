
# Package Clean Up

Package clean up inspector window is located in the top bar **Tools/Scene Forge/Package Clean Up**

The inspector provides several options for cleaning the Scene Forge tool. In case of saving errors or removing the package from your project cleanly.

# Inspector Options

**Check Current Scene** checks the current scene for any Scene Forge components and logs them in the console.

---

**Check All Scenes**  checks  all scenes in the project for any Scene Forge components and logs them in the console.

---

**Clean Current Scene** removes any Scene Forge components from the game objects in the current scene. 
>**Doesn't delete objects, only the Scene Forge components!**

---

**Clean User Data**: As you use the Scene Forge tool data gets saved by the tool in the Editor Prefs. This function will clear all of them.

**Save data that gets deleted:**

- Composition guide settings
- Point scatter presets
- Area scatter presets
- Mesh scatter presets

# How to remove Scene Forge 

 Before deleting the root folder you need to remove all Scene Forge components from your scenes, otherwise you will get **missing script** warnings and errors. You can do that by using the **Package Clean Up** window inspector located in **Tools/Scene Forge/Package Clean Up**. 
 
 1.  Use the **Check All Scenes** in order to find if any Scene Forge components are present in your scenes.
 2.  Open those scenes one by one and use the **Clean Current Scene** functionality inside  **Package Clean Up** window in order to remove any Scene Forge components from the scene.
 3.  Once you have cleaned your scenes you can delete the root folder of the Scene Forge tool in the Editor folder. If you don't know where it is you can use the **Search Bar** to locate it. The root folder is called **"Scene Forge"**. You will also find a **Scene Forge** folder outside the Editor folder that contains several more script components. Delete that too.
 4.  Restart your project in order to confirm that everything was removed cleanly.

#### Important, make sure that your scenes are not using any of the Time of Day Presets before deleting! They are found inside Scene Forge/Assets/Post Proccess Volumes. You could loose your scene lights, HDRIs or PP Volumes!

# Troubleshoot

If you encounter any errors after deleting files you can always restore them from the Recycle Bin or Trash and check you scenes again.
If you have any errors that you are unable to solve you can find help in our [Discrod](https://discord.gg/9rUWFx9vxh).
