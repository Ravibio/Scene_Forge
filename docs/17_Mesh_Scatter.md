
# Mesh Scatter

Used to scatter prefabs on meshes. To scatter prefabs first you have to create mesh scatter presets. Each preset can be used to scatter different types of prefabs. 


# Presets

You can open the point scatter settings inspector by pressing **Shift + S** and navigating to **Scatter/Mesh Scatter/Presets Editor** or the top bar **Tools/Scene Forge/Scatter/Mesh Scatter**.

The scattering is done using a list of methods. Each method is used to scatter objects on certain parts of the mesh and then the methods are combined based on an math operation.

**Preset Properties:**

- **Name** (Name of the preset)
- **Coverage** (Percentage based on scattered prefab and targets area) 
- **Scatter Density** (Defines the density of scattered objects)  
- **Limit Object Count** (If checked ignores the **Scatter Density** and instead sets object count between **Min Count** and **Max Count**)
- **Prefab Up Vector** (Defines the up vector of all prefabs)
- **Use Mesh Normal** (Should the prefab be oriented based on the surface normal)
- **Align with normal (%)** (Aligns the object with the surface up direction based on %)
- **Align with direction (%)** (Aligns the object with the surface forward direction based on %)
- **Add random rotation (%)** (Allows you to add random rotation around the local orientation of the object. **Note: this happens after the object has been aligned with the terrain and can cause unexpected results if using both**)
- **Scatter Height** (Defines maximum and minimum scatter height based on the target, **NOT global**)
- **Fall-Off Curve** (Scatter density curve)

- **Methods**

	- Scatter Method **Random** (Scatters prefabs randomly)
	- Scatter Method **Normal Direction** (Scatters prefabs based on normals of the mesh and the value of **Normals** property.
	
- **Prefab Properties**

	- **Weight** (The chance of this prefab being placed)
	

 >*Your presets get auto saved after making changes like adding new preset, deleting, changing values while scattering and closing the inspector.*

# Scattering

The actual scattering happens after creating a preset and selecting it. To select a preset press **Shift + S** and navigate to **Scatter/Mesh Scatter** and select you preset.

New point scattering shortcuts will now be available:

- **Space Bar** key is used to scatter the prefabs on selected objects.
- **Shift + S** keys are used to open the Mesh scatter presets editor inspector
- **Esc** key is used to exit Mesh Scattering


# Requirements

- **Scene Forge tool is active**
- **Selecting a Mesh Scatter Preset**
- **Convex Colliders** - If using Mesh Colliders make sure that they can be set to Convex. The algorithm uses method [ClosestPoint()](https://docs.unity3d.com/2022.3/Documentation/ScriptReference/Collider.ClosestPoint.html) in order to determine if a point is inside the collider or not. This method requires that Mesh Colliders are set to Convex = True. The program will automatically try and set Convex to True for the duration of the process but if your mesh exceeds the limit a warning will appear. **You can disable the use of "ClosestPoint()" in the preset settings but that will increase process times**. (Mesh Collider Limits)

# Limitations

Meshes above 100k triangles could take some time to compute especially with high scatter density values. 
