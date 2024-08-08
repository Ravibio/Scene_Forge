# Terrain Scatter

Used to scatter prefabs on the Unity Terrain. To scatter first you have to create terrain scatter presets and then create terrain scatter group objects that use the presets. Each preset can be used to scatter different types of prefabs. 


# Quick Start

**1. Create Terrain Scatter preset** 
In the scene view press **Shift + S** to open the functions menu and navigate to **Scatter/Terrain Scatter/Presets Editor** or from the top bar **Tools/Scene Forge/Scatter/Terrain Scatter/Presets Editor**.
Create a preset and navigate to the prefabs tab to assign a prefab. If you don't have ready prefabs you can toggle **Use placeholder** and click on the button next to the field which will allow you to chose a placeholder from the asset library.

**2. Create Terrain Scatter Group** 
 In the scene view press **Shift + S** to open the functions menu and navigate to **Scatter/Terrain Scatter/Add Scatter Group** or from the top bar **Tools/Scene Forge/Scatter/Terrain Scatter/Add Scatter Group**. This will add and select a Terrain Scatter game object.

**3. Scattering** 
 Create a Unity Terrain and assign it to the Terrain Scatter Group game object (Tile 1 field). Press **Scatter**.

# Preset Properties

You can open the point scatter settings inspector by pressing **Shift + S** and navigating to **Scatter/Terrain Scatter/Presets Editor** or the top bar **Tools/Scene Forge/Scatter/Terrain Scatter/Presets Editor**.

- **Properties:**

	- **Name** (Name of the preset. **Note: keep the names unique**)
	- **Density** (Density of scattered objects) 
	- **Add to terrain** (Allows you to add your scattered objects as terrain tree and detail instances. Instances will be created automatically if they are not present. If set to true a new option will appear under every prefab allowing you to choose between Tree and Detail instances. **Note: terrain details don't work on all Unity Versions**)
	- **Prefab Count** (Number of Prefabs)
	- **Align with normal (%)** (Aligns the object with the terrain up direction based on %)
	- **Align with direction (%)** (Aligns the object with the terrain forward direction based on %)
	- **Add random rotation (%)** (Allows you to add random rotation around the local orientation of the object. **Note: this happens after the object has been aligned with the terrain and can cause unexpected results if being used together with "Align with normal" or "Align with direction"**)
	- **Use object scale** (If True scattered objects will use the scale they were originally set as)
	- **Per Component** (If **Use object scale** is set to False. Allows you to specify min and max scale individually for every object. New options for scale will appear under every prefab in the Prefabs tab. 
	- **Min and Max Scale** (If **Use object scale** is set to False. You can set the min and max scale of objects)
	- **Scale Range** (If **Use object scale** is set to False. Defines areas of likelihood for random scales. Values outside of the range are less likely to be picked.)
	- **Border Prefabs** (If True the algorithm will detect objects close to Boolean objects and replaces them. Can be used to distribute smaller objects around borders to avoid clipping. When True a new option will be available to every prefab where you can specify a replacement object.) *Settings for Boolean and Mesh groups*
	- **Border Distance** (Sets the maximum distance from the boolean border where objects will be detected and replaced) *Settings for Boolean and Mesh groups*
	- **Remove Surroundings** (Removes objects surrounding the boolean in a given distance) *Settings for Boolean and Mesh groups*
	- **Max Distance** (Distance from boolean where points will be removed) *Settings for Boolean and Mesh groups*
	- **Fall Off** (Determines the chance a point will be removed based on its distance from the boolean object) *Settings for Boolean and Mesh groups*



- **Slope**

	- **Invert** (If True inverts the result)
	- **Min Angle** (Sets the minimum angle. Objects won't be placed  when normal is below this angle)
	- **Max Angle** (Sets the maximum angle. Objects won't be placed when normal is above this angle)

- **Curvature**
	
	- **Invert** (If True inverts the result)
	- **Scatter on peaks** (If True a slider **Peaks** will appear allowing you to define what a peak is)
	- **Peaks** (A value from 0-100 where at 0 everything is considered a peak. There is no value that will works for every terrain, I recommend experimenting until you find the best value)
	- **Scatter in valleys** (If True a slider **Valleys** will appear allowing you to define what a valley is)
	- **Valleys** (A value from 0-100 where at 0 everything is considered a valley. There is no value that will works for every terrain, I recommend experimenting until you find the best value)
	- **Sample Points** (Number of heights to sample around every point to calculate peaks and valleys. The detection is also based on terrain resolution so increase this value only if you have a high resolution terrain.)
	- **Sample distance** (Distance from point where sample heights will be taken)
	- **Peak threshold** (How big the difference between sample heights and point has to be in order for the point to be deemed as a peak. If you have 7 sample points and this value is set to 2 then the peak sample points have to be +2 more than the valley points in order for this point to be deemed a peak)
	- **Valley threshold** (How big the difference between sample heights and point has to be in order for the point to be deemed as a valley. If you have 7 sample points and this value is set to 2 then the valley sample points have to be +2 more than the peak points in order for this point to be deemed a valley)

- **Height**
	
	- **Min Height** (Objects below this position won't be placed. **Note: the value is global Y position NOT taking into account the position of the terrain itself**)
	- **Down fall off (%)** (Percentage value that allows objects to be placed bellow the **Min Height**)
	- **Max Height** (Objects above this position won't be placed. **Note: the value is global Y position NOT taking into account the position of the terrain itself**)
	- **Up fall off (%)** (Percentage value that allows objects to be placed above the **Min Height**)
	- **Prefab levels** (If set to True for every prefab will appear an option that allows you to specifically set their min and max allowed height)

- **Noise**

	- **Width** (Width in pixels of the noise texture)
	- **Length** (Length in pixels of the noise texture)
	- **Translate** (Allows you to move the noise)
	- **Rotate** (Allows you to rotate the noise)
	- **Scale** (Allows you to scale the noise)
	- **Uniform scale** (Scales the noise uniformly)
	- **Amplitude** (Controls the amplitude of the noise)
	- **Frequency** (Controls the frequency of the noise)

- **Biomes**

	- **Use textures** (If set to True, allows you to specify textures instead of terrain layers)
	- **Invert** (If set to True, inverts the result)
	- **Terrain layers** (If Use textures is False. Allows you to specify terrain layers where objects will be placed)
	- **Biome textures** (If Use textures is True. Allows you to specify terrain textures where objects will be placed. **Note: place Albedo textures used by the terrain layers**)


- **Prefab settings**

	- **Weight** (Determines the likelihood of placing this object)
	- **Prefab up vector** (Specifies the up direction of the object)
	- **Offset** (Adds position offset after the object was placed)
	- **Use placeholder** (Allows you to specify a placeholder object. You can choose your own or click on the button next to the **Placeholder** field and you can choose an object from the asset library)
	- **Add as prototype** (Adds the SF_Prototype script to the object which will allow you to swap it later using the Object Conversion methods. For more info check **Prototype Objects**, **Collections** and **Object Convert** pages of this documentation.)
 
 
 
 >Your presets get auto saved after making changes like adding new preset, deleting, changing values while scattering and closing the inspector. And if there is a Terrain Scatter Object that uses the selected preset with Auto Update set to True any changes will result in rescattering.


