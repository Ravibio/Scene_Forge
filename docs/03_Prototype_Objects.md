
# Scene Forge Prototype Objects

**Scene Forge Prototype** (SF_Prototype) is a component that is attached to a game object in order to be used by the Scene Forge tool in its operations. Those are typically basic shape objects like cubes, planes, cylinders, etc. Those objects are then added to a **Collection** object as children, so that they can be grouped in categories and managed more easily.

>*You can prototype entire scenes using simple cubes.*

# Properties
Adding a prototype object in your scene can be done easily by pressing **Shift+A** or by navigating to **Tools/Scene Forge/Prototyping**. 

Additionally you can convert your own basic shapes to Scene Forge prototypes by:

1.  Selecting object/objects from the scene
2.  Pressing **Shift+S** and navigating to **Convert/Add SF Component**

As well as removing the Scene Forge prototype component by:

1.  Selecting object/objects from the scene
2.  Pressing **Shift+S** and navigating to **Convert/Remove SF Component**

>*If you want to clean your scenes from any **Scene Forge Components** you can do so by navigating to the top bar **Tools/Scene Forge/Package Clean Up** and click on the **Clean Current Scene** button.*

The **SF_Component** by itself has no other function than to just mark the assigned object as Scene Forge Prototype so it has little to none impact on game performance when testing.

# Requirements
Scene Forge must be active in order to add prototype objects using the shortcuts.


# Limitations
Using the **Convert/Add SF Component** function will not change the materials of your object to Scene Forge prototype materials. It will only add the **SF_Prototype** component to it. **The color of the parent collection with have no affect on the object.**
