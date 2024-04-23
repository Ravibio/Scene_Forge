
# Composition Guides
Composition guides are visual guidelines that can help artists create visually appealing and well-balanced scenes. One commonly used composition guide is the rule of thirds, which divides the visual space into three equal parts both horizontally and vertically. By placing the main subjects or focal points of the scene along these lines or at their intersections, the resulting scene is often more visually interesting and dynamic.

# Properties
You can enable composition guides by pressing **C** or by navigating to the top bar **Tools/Scene Forge/Composition Guides**.


Composition Guides:

- Center
- Diagonal
- Thirds
- Golden Ratio
- Triangle A (derived from Golden Ratio)
- Triangle B (derived from Golden Ratio)

>You can activate multiple composition guides at the same time.

#
**Composition Settings**
The composition settings inspector window provides some basic control over the guides:

- **Line Thickness** 
- **Line Color**

Also provides a way to adjust the guides to better fit your scene view:

- **Preview Guides** (Enables the **Diagonal** guide in preview)
- **Screen Width Offset** (Adjusts the scene view width)
-  **Screen Height Offset** (Adjusts the scene view height)

>By default the **Screen Height Offset** is set to **-47**, because **Screen.height** used in the function returns the height of the scene view inspector window instead of the scene view itself.

# Requirements
Scene Forge must be enabled in order to draw composition guides.


# Limitations
Different screen resolutions and Windows Zoom may shift the ends of the guides in which case the default adjustment values for **Screen Width Offset** and **Screen Height Offset** will be wrong.
