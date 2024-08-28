
# Objects Convert

The Objects Convert function in Scene Forge helps you replace placeholder objects, like boxes and simple shapes, with finished environment objects and structures. It looks at settings and properties, like bounds size, to find the best match for each prototype object. This makes designing and developing scenes easier and allows for simple adjustments and changes to your scenes.

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

- **Position**
	- **Match Centers** positions the prefab object so that its center matches the center of the prototype.
	- **Match Pivots** positions the prefab object so that its pivot matches the pivot of the prototype.
	- **Pivot to Center** positions the prefab object so that its pivot matches the center of the prototype.
	- **Center to Pivot** positions the prefab object so that its center matches the pivot of the prototype.
	- **Per Component** allows for individual position settings for each prefab.
	- **Offset** is used to translate the object by a given amount after being placed. Uses the world vectors.
	- **Directional Offset** is used to translate the object by a given amount after being placed. Used the local object directions.

- **Scale**
	- **Copy Local** is used to copy the local scale of the prototype to the prefab.
	- **Copy Global** is used to copy the global scale of the prototype to the prefab. In cases when the parent/collection has a scale other than (1,1,1).
	- **Add to Prototype** is used to add the scale value to the existing  scale of the prototype and set it to the prefab.
	- **Add to Prefab** is used to add the scale value to the existing scale of the prefab and set it to the prefab.
	- **Set** is used to set scale to the prefab. Overwrites the prefab scale by the new value.
	- **Multiply by Prototype** is used to multiply the scale value by the existing scale of the prototype and set it to the prefab.
	- **Multiply by Prefab** is used to multiply the scale value  by the existing scale of the prefab and set it to the prefab.
	- **Per Component** allows for individual scale settings for each prefab.
	- **Match Bounds** is only available with methods that use Bounds (see above). When checked the prefab object size will match the bounds size of the prototype. This happens before the above methods.


- **Rotation**
	- **Copy Local** is used to copy the local scale of the prototype to the prefab.
	- **Copy Global** is used to copy the global scale of the prototype to the prefab. In cases when the parent/collection has a scale other than (1,1,1).
	- **Add to Prototype** is used to add the scale value to the existing  scale of the prototype and set it to the prefab.
	- **Add to Prefab** is used to add the scale value to the existing scale of the prefab and set it to the prefab.
	- **Set** is used to set scale to the prefab. Overwrites the prefab scale by the new value.
	- **Multiply by Prototype** is used to multiply the scale value by the existing  scale of the prototype and set it to the prefab.	
	- **Multiply by Prefab** is used to multiply the scale value by the existing scale of the prefab and set it to the prefab.
	- **Per Component** allows for individual scale settings for each prefab.


	
- **Folder Path** is used to load all prefabs from a specified project folder.
- **Parent Name** specifies the name of the parent that will hold the new prefabs.
- **Hide Collection** when checked will hide the prototype objects after conversion.
- **Complex Prefabs** are prefabs that have more than one object with mesh filter attached. There are two methods that are used to match those prefabs.

	- **Use Largest Mesh** will only match based on the size of the larges mesh. For example if you have a house prefab that is made out of a single mesh but has small attachments like a chimney, this method will ignore the chimney and only take the size of the house.
	- **Combine Meshes** will combine the size of all meshes. For example if you have a house that is made out of different room segments, this method will combine the sizes of all rooms and match based on that.

>*For prefabs with **LOD group** the function will only use the renderers found in LOD_0 of the group!*

# Requirements

Scene Forge must be enabled.


# Limitations

- The conversion will only work on prototype objects that have the **SF_Prototype** component attached and are inside a collection.
- The prototype objects must have a Renderer component attached (Needed only when converting using methods that require bounds).
