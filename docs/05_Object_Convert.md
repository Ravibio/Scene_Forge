
# Objects Convert

The Objects Convert function in Scene Forge streamlines the process of replacing placeholder objects, such as boxes and basic shapes, with finalized environment objects and structures. By analyzing settings and properties like bounds size, the function automatically matches each prototype object to the most suitable final object. This saves time and effort in the design and development of scenes, ensuring a seamless transition from placeholders to polished assets as well as allows for easy scene iterations and changes.

The Function works by first fitting the size of all prefabs to the size of all prototype objects so that the largest prototype can be matched with the largest prefab. Then based on the method the prefabs will be matched to the prototype objects both in size and orientation.

# Properties

You can find the **Objects Convert** window inside the **Functions** menu by pressing **Shift + S** and selecting **Convert/Convert Objects** or from the top bar **Tools/Scene Forge/Objects Converter**.

Once open you will find all your scene collections listed their.


- **Methods**

	-  **Match Models Size** matches the average size of the prototype bounds to the average size of the prefab bounds.
		-	**Requires that both prototype and prefab objects have a renderer component!**
	-  **Random Match (Bounds)** chooses a random prefab for every object. It also matches the prefab size to the prototype bounds size
		- **Requires that both prototype and prefab objects have a renderer component!**
	- **Random Match (No Bounds)** uses a random system to pair prototypes and prefabs.
	- **Match Object Name** matches prototypes and prefabs by name.
	-  **Match Specific Axis**, unlike Match Model Size this method only looks at the specified axis of the prototype objects size and finds a match for it. For example if you have trees with different heights using this method will ensure that every tree prefab will match the prototype objects **Y** size perfectly instead of its average.
		-  **Requires that both prototype and prefab objects have a renderer component!**

- **Match Scale** when checked won't change the size of the prefab after matching it. Matching happens at 1:1 scale and after that the prefab is scaled to match the size of the prototype as close as possible. This option disables that. 
	
- **Folder Path** is used to load all prefabs from a specified project folder.
- **Parent Name** specifies the name of the parent that will hold the new prefabs.
- **Hide Collection** when checked will hide the prototype objects after conversion.
- **Complex Prefabs** are prefabs that have more than one object with mesh filter attached. There are two methods that are used to match those prefabs.

	- **Use Larges Mesh** will only match based on the size of the larges mesh. For example if you have a house prefab that is made out of a single mesh but has small attachments like a chimney, this method will ignore the chimney and only take the size of the house.
	- **Combine Meshes** will combine the size of all meshes. For example if you have a house that is made out of different room segments, this method will combine the sizes of all rooms and match based on that.

>*For prefabs with **LOD group** the function will only use the meshes found in LOD_0 of the group!*

# Requirements

The option will only be available if there are Scene Forge collections present in the scene.


# Limitations

- The conversion will only work on prototype objects that have the **SF_Prototype** component attached and are inside a collection.
- The prototype objects must have a Renderer component attached (Needed to calculate the bounds of the object).
