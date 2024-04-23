
# Getting Started With Scene Forge

Welcome to the **Getting Started** guide for **Scene Forge** this short guide is designed to help you become familiar with the core features and functionality of this tool so that you can start using it effectively in your Unity projects. Whether you are a beginner or an experienced Unity developer, this guide will provide you with the information you need to get up and running quickly. Let's begin by exploring the basic concepts and procedures.


# How to enable?
Enabling and disabling the tool can be done in the same two ways:
- Navigating to the top bar and selecting **Tools/Scene Forge/Enable**.
-  Pressing the **F5** key.


# Workflow and Components
Prototyping a scene using Scene Forge consists of two basic steps.
- Create Scene Forge Prototype objects and Collections
- Convert the Collections of objects to the prefabs they represent.

#

The two main components used by the tool are **Scene Forge Prototype** and **Scene Forge Collection**.

**Scene Forge Prototype** is a component that is attached to a game object in order to be used by the Scene Forge tool in its operations. Adding a prototype object in your scene can be done easily by pressing **Shift+A** or by navigating to **Tools/Scene Forge/Prototyping**. 
By default when you first add a prototype object the tool will create a base collection for it.

**Scene Forge Collection** is simply the parent of a group of prototype objects. For example you can have a collection called Cliffs, Houses, Trees, etc. The collection object lets you modify its objects/children more easily, like changing the color of all your Cliff prototype boxes to red.
You can add and modify collections in your scenes by pressing the **M** key or navigating to **Tools/Scene Forge/Prototyping**. 

>You can move selected objects to a certain collection by selecting it from the menu. 

>Selecting prototype objects and creating a new collection will automatically assign them to it.

#

**Converting your Collections**
Once you have created your prototype objects and collections you can replace them with your actual game prefabs by opening the Convert Inspector Window. You can find it inside the **Shift+S** Functions menu, **Convert/Convert Objects** or the top bar items **Tools/Scene Forge/Convert Objects**.
Inside the inspector you can either manually drag and drop your prefabs or you can use **Folder Path** from where the tool will automatically load every prefab it can find. 

Simple explanation of what the different conversion methods are:

- **Match Model Size** replaces the prototype object with the prefab that best matches its average bounds size.
-  **Random** does what you've already guessed. It simply chooses a random prefab for every object. Can be useful when dealing with prefabs that don't have much size variation.
-  **Match Specific Axis** unlike Match Model Size this method only looks at the specified axis of the prototype objects size and finds a match for it. For example if you have trees with different heights using this method will ensure that every tree prefab will match the prototype objects **Y** size perfectly instead of its average.

Once you have set your settings the final step it to click the **Convert** button. The workflow is non-destructive so you can experiments and iterate with different settings and prefabs. 

#
That concludes this very basic explanation of the core feature that Scene Forge empowers. Feel free now to take your exploration further by delving deeper into this documentation, or by taking the initiative to experiment and discover new ways to leverage the tool in your Unity projects. 

If you have any questions, feedback, or simply want to connect with fellow users and me, feel free to join our Discord group https://discord.gg/BGsYeCvJ.
