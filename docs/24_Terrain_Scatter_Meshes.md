
# Terrain Scatter Meshes

Group of objects that the terrain scatter will use when placing object. Mesh objects are children of a parent that has the Terrain Scatter Mesh Group component attached.

# Quick Start

**1. Create group** 
To create terrain scatter mesh group, in the scene view press **Shift + S** to open the functions menu and navigate to **Scatter/Terrain Scatter/Add Mesh Group** or from the top bar **Tools/Scene Forge/Scatter/Terrain Scatter/Add Mesh Group**.

**2. Set Tag**
Create a  **SF Mesh Group** tag  and set it to the mesh group object

**3. Add meshes**
Create a simple box and add it to the group as a child

**4. Presets**
At this point in order to use you need to have a terrain scatter preset, Terrain Scatter Group and a terrain. If you don't check out the Quick Start in the [**Terrain Scatter**](https://scene-forge.readthedocs.io/en/latest/22_Terrain_Scatter/) page in this documentation.

Once you have a preset, a terrain and a terrain scatter group, press **Update** on the Boolean Group or Scatter Group game object.

## Notes

If you are using mesh colliders in your objects I recommend setting them as Convex. This will both improve the processing speeds and detection of points.

# Properties

- **Target preset:** Terrain scatter preset to influence
- **Auto update:** Updates the scatter automatically when you make any changes to the position of the objects
- **Max angle:** Objects will not be placed on mesh triangles with normal angle greater than this
- **Grid Spacing:** Lower grid spacing increases processing times but provides a more accurate result. The algorithm creates a grid of points for every object, which is then used to determine if a scatter object should be placed on the surface of the mesh.
- **LOD index:** If you are using LODs for your objects this settings allows you to specify which LOD to process. Meshes with lower polycount are processed faster.

# Requirements

- **Terrain Scatter Group** - in order to use you need to already have a Terrain Scatter Group object using the same preset as the boolean group

- **Tag** - parent object is required to have the **SF Mesh Group** tag 

- **Collider** - mesh objects are required to have a collider in order for the algorithm to be able to use them as booleans and remove intersecting objects.

- **Convex Colliders** - If using Mesh Colliders make sure that they can be set to Convex. The algorithm uses method [ClosestPoint()](https://docs.unity3d.com/2022.3/Documentation/ScriptReference/Collider.ClosestPoint.html) in order to determine if a point is inside the collider or not. This method requires that Mesh Colliders are set to Convex = True. The program will automatically try and set Convex to True for the duration of the scatter but if your mesh exceeds the limit a warning will appear. **You can disable the use of "ClosestPoint()" by setting "Mesh Collider Limits" option to true in the preset settings, but that will increase process times**.

