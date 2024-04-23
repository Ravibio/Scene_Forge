
# Point Scatter
Used to scatter chosen prefabs on surfaces by simple point and click. To scatter prefabs first you have to create point scatter presets. Each preset can be used to scatter different types of prefabs. 


# Presets
You can open the point scatter settings inspector by pressing **Shift + S** and navigating to **Scatter/Point Scatter/Presets Editor** or the top bar **Tools/Scene Forge/Scatter/Point Scatter**.

**Preset Properties:**
- **Name** (Name of the preset)
- **Hit Layers** (List of layers that the point scatter raycast will collide with) 
- **Use Surface Normal** (Should the prefab be oriented based on the surface normal)
- **Random Rotation** (Generates random rotation between the specified min and max values)
- **Prefab Properties**
	- **Weight** (The chance of this prefab being placed)
	- **Up Vector** (The vector that indicates the Up direction of the prefab)
	- **Uniform Scale** (Is the scale Uniform, that is all axis sizes are equal)
	- **Position Offset** (Adds a position offset after placement)  

 >Your presets get auto saved after making changes like adding new preset, deleting, changing values while scattering and closing the inspector.

# Scattering
The actual scattering happens after creating a preset and selecting it. To select a preset press **Shift + S** and navigate to **Scatter/Point Scatter** and select you preset.

New point scattering shortcuts will now be available:
- **Space Bar** key is used to place a prefab at mouse position.
- **Shift + S** keys are used to open the Point scatter presets editor inspector
- **Esc** key is used to exit Point Scattering


# Requirements
- Scene Forge tool is active
- Selecting a Point Scatter Preset

# Limitations
Unable to scatter on objects without colliders since the function uses **Raycast**.
