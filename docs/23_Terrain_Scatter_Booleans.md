
# Terrain Scatter Booleans

Group of objects used as booleans when using the terrain scatter tools. Boolean objects are children of a parent that has the Terrain Scatter Boolean Group component attached.

# Quick Start

**1. Create group** 
To create terrain scatter boolean group, in the scene view press **Shift + S** to open the functions menu and navigate to **Scatter/Terrain Scatter/Add Boolean Group** or from the top bar **Tools/Scene Forge/Scatter/Terrain Scatter/Add Boolean Group**.

**2. Set Tag**
Create a  **SF Boolean Group** tag  and set it to the boolean group object

**3. Add booleans**
Create a simple box and add it to the group as a child

**4. Presets**
At this point in order to use you need to have a terrain scatter preset, Terrain Scatter Group and a terrain. If you don't check out the Quick Start in the [**Terrain Scatter**](https://scene-forge.readthedocs.io/en/latest/22_Terrain_Scatter/) page in this documentation.

Once you have a preset, a terrain and a terrain scatter group, press **Update** on the Boolean Group or Scatter Group game object.

## Notes

If you want to use mesh colliders as booleans I recommend setting them as Convex. This will both improve the processing speeds and detection of points.

# Properties

- **Target preset:** Terrain scatter preset to influence
- **Auto update:** Updates the scatter automatically when you make any changes to the position of the objects
- **Draw colliders:** If your boolean object doesn't have a renderer component and this is set to True your collider will be drawn in scene. 
- **Invert:** If True the objects will be scattered inside the boolean objects only

# Requirements

- **Terrain Scatter Group** - in order to use you need to already have a Terrain Scatter Group object using the same preset as the boolean group

- **Tag** - parent object is required to have the **SF Boolean Group** tag 

- **Collider** - boolean objects are required to have a collider

- **Convex Colliders** - If using Mesh Colliders make sure that they can be set to Convex. The algorithm uses method [ClosestPoint()](https://docs.unity3d.com/2022.3/Documentation/ScriptReference/Collider.ClosestPoint.html) in order to determine if a point is inside the collider or not. This method requires that Mesh Colliders are set to Convex = True. The program will automatically try and set Convex to True for the duration of the process but if your mesh exceeds the limit a warning will appear. **You can disable the use of "ClosestPoint()" in the preset settings but that will increase process times**. (Mesh Collider Limits)

