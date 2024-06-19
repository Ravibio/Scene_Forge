
# Scene Forge Collections

**Scene Forge Collection** is simply the parent of a group of prototype objects. For example you can have a collection called Cliffs, Houses, Trees, etc. The collection object lets you modify its objects/children more easily, like changing the color of all your Cliff prototype boxes to gray.

# Properties

You can add and modify collections in your scenes by pressing the **M** key or navigating to **Tools/Scene Forge/Prototyping**. 

Adding a new collection properties:

- Name (Name of the collection)
- Color (Color of the prototype objects inside the collection)
- Secondary Color (Used for placeholder objects with two materials, like trees, houses, etc.)

Edit collections properties:

-  Add Collection (Created a new collection)
-  Delete Collection (Deletes collection **together with all of its children**)
-  Name (Change the name of chosen collection)
-  Color (Change the color of chosen collection)

You can assign prototype objects to a collection by:

1.  Selecting object/objects.
2.  Pressing **M** and choosing one of the available collections in the scene.

# Requirements

In order for the shortcuts to work Scene Forge must be enabled.


# Limitations

Scene Forge Collections work only with objects that have the **SF_Prototype** component attached. 
For information about  **SF_Prototype** check the **Prototype Objects** section of this documentation.
