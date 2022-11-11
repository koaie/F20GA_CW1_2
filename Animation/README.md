# Animation
## Workflow
### Importing objects
The scene was exported as a FBX file and imported to unreal, the results are the objects exist within unreal with major differences than blender in terms of faces.
https://i.imgur.com/FxC5GpP.png

![UE5](https://i.imgur.com/FxC5GpP.png "ue5")

The suspected reason for this is backface curling, game engines render objects differently than blender and thus this problem arose, it was attempted to mitigate by recaulating the normals of the problemtic objects, however that was proved to not be a successful approuch. Methods to mitigate this issue were searched but the most common issues were not relateable nor helped fix the issue. As a result the chess pieces objects used within the animation section of the CW are flawed.
### Importing textures
Texture roughtness, metalic, and normals are not transferred with FBX files, meaning they can not be used to import textures to UE5.
Textures for the chess pieces and the chess board are baked in blender and imported into UE5, allowing us to use the same textures without recreating them.
This is done by creating a UV map for each object, and then baking the right texture property (base colour, roughtness, and normal). No matelic textures exists in this project.

## Lighting

## Camera settings


## Project
Link to the unreal project:
https://heriotwatt-my.sharepoint.com/:u:/g/personal/yl2014_hw_ac_uk/EceTbk_K6QxCoOS-dY9B24MBZ4ge9PvybQsR2vBurG5FDg?e=O55qhj
