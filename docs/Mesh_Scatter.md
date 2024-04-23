
# Mesh Scatter
Used to scatter prefabs on meshes. To scatter prefabs first you have to create mesh scatter presets. Each preset can be used to scatter different types of prefabs. 


# Presets
You can open the point scatter settings inspector by pressing **Shift + S** and navigating to **Scatter/Mesh Scatter/Presets Editor** or the top bar **Tools/Scene Forge/Scatter/Mesh Scatter**.

The scattering is done using a list of methods. Each method is used to scatter objects on certain parts of the mesh and then the methods are combined based on an math operation.

**Preset Properties:**
- **Name** (Name of the preset)
- - **Scatter Density** (Defines the density of scattered objects)
- **Limit Object Count** (If checked ignores the **Scatter Density** and instead sets object count between **Min Count** and **Max Count**)
- **Prefab Up Vector** (Defines the up vector of all prefabs)
- **Use Mesh Normal** (Should the prefab be oriented based on the surface normal)
- **Random Rotation** (Generates random rotation between the specified min and max values)
- **Methods**
	- Scatter Method **Random** (Scatters prefabs randomly)
	- Scatter Method **Normal Direction** (Scatters prefabs based on normals of the mesh and the value of **Normals** property.
- **Prefab Properties**
	- **Weight** (The chance of this prefab being placed)
	

 >Your presets get auto saved after making changes like adding new preset, deleting, changing values while scattering and closing the inspector.

# Scattering
The actual scattering happens after creating a preset and selecting it. To select a preset press **Shift + S** and navigate to **Scatter/Mesh Scatter** and select you preset.

New point scattering shortcuts will now be available:
- **Space Bar** key is used to scatter the prefabs on selected objects.
- **Shift + S** keys are used to open the Mesh scatter presets editor inspector
- **Esc** key is used to exit Mesh Scattering


# Requirements
- Scene Forge tool is active
- Selecting a Mesh Scatter Preset

# Limitations
Meshes above 100k triangles could take some time to compute especially with high scatter density values. 
