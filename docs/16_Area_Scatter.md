
# Area Scatter

Used to scatter chosen prefabs on surfaces in an area by simple point and click. To scatter prefabs first you have to create area scatter presets. Each preset can be used to scatter different types of prefabs. 


# Presets

You can open the point scatter settings inspector by pressing **Shift + S** and navigating to **Scatter/Area Scatter/Presets Editor** or the top bar **Tools/Scene Forge/Scatter/Area Scatter**.

**Preset Properties:**

- **Name** (Name of the preset)
- **Scatter Density** (Defines the density of scattered objects)
- **Object Count** (If checked ignores the **Scatter Density** and instead sets object count between **Min Count** and **Max Count**)
- **Fall-Off Curve** (The curve defines the density of the prefabs based on the distance from the center)
- **Hit Layers** (List of layers that the point scatter raycast will collide with) 
- **Align with normal (%)** (Aligns the object with the surface up direction based on %)
- **Align with direction (%)** (Aligns the object with the surface forward direction based on %)
- **Add random rotation (%)** (Allows you to add random rotation around the local orientation of the object. **Note: this happens after the object has been aligned with the terrain and can cause unexpected results if using both**)
- **Prefab Properties**

	- **Weight** (The chance of this prefab being placed)
	- **Up Vector** (The vector that indicates the Up direction of the prefab)
	- **Uniform Scale** (Is the scale Uniform, that is all axis sizes are equal)
	- **Position Offset** (Adds a position offset after placement)  

 >*Your presets get auto saved after making changes like adding new preset, deleting, changing values while scattering and closing the inspector.*

# Scattering

The actual scattering happens after creating a preset and selecting it. To select a preset press **Shift + S** and navigate to **Scatter/Area Scatter** and select you preset.

New point scattering shortcuts will now be available:

- **Space Bar** key is used to place a prefab at mouse position.
- **Shift + S** keys are used to open the Point scatter presets editor inspector
- **Shift + D** holding down those keys and moving the mouse to the left or right will decrease of increase the scattering radius
- **Esc** key is used to exit Point Scattering


# Requirements

- Scene Forge tool is active
- Selecting a Area Scatter Preset

# Limitations

Unable to scatter on objects without colliders since the function uses **Raycast**.
