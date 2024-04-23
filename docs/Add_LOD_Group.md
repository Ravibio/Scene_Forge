
# Add LOD Group

Adds the LOD Group component to the selected objects and assigns the appropriate children to their LOD slots. As well as setting colliders (if present). In addition it sets the correct object size and percentages for each LOD based on the bounds of the objects.

# Properties

There are no user controllable property fields.

# Requirements

The **Add LOD Group** functionality works with several LOD object structures:

1. **Numbered object structure**

	Uses the naming of the child objects in order to determine the LOD objects and levels.
	
	**Example structure:**
	
	- Rock_LODs
	
		- Rock_LOD_0
		- Rock_LOD_1
		- Rock_LOD_2
		- Rock_Collider
	
	With this structure the function will look at the **last number** of each child and sort the objects based on that. If the function finds any objects that end with **Collider** or **Coll** the function will exclude them from the LOD Group and instead assign them a **Mesh Collider** Component, otherwise every object will get a **Mesh Collider**. 

2. **Keywords object structure**

	This method uses a list of keywords in order to determine the LOD objects and levels.
	
	**Example structure:**
	
	- Rock_LODs
	
		- Rock_High
		- Rock_Med
		- Rock_Low
		- Rock_Collider

In this structure the function looks how the names of the child objects end and attempts to create a LOD Group based on that. The keywords are **"high", "med", "medium", "low"**.  In the same manner as structure 1, the function will set **Colliders** based on the **Collider** or **Coll** keywords.

>*The function sets all letters to lowercase before comparing with the keywords list. Applies for **collider** keywords as well. Its **not** key sensitive.*


3. **No Structure**

	If none of the above structures are found by the function. The objects will be sorted by polycount and assigned to the LOD Group.

# Limitations

Won't work with complex objects with **more than 1 level of children**. If the function encounters a complex object it will skip it and write a log in the console.

**Complex object structure example:**

- Parent

	- Level 1 child
	
		- Level 2 child
		
			- etc..
