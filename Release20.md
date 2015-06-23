## <font color='#336699'>Kuda 2.0.1 Release Notes (2012 April 14)</font> ##
### What's New ###
#### World Editor ####
  * COLLADA Camera support, viewpoints are automatically created from the source file
  * Environment Lights plugin, add other types of lights to your project
  * Added moveTo and turnTo actions for absolute movements
  * Edit the main cameras viewpoint parameter
  * Manually edit model shapes (transforms) position, scale, and rotation
  * Keyboard triggers, use the keyboard instead of the mouse for actions
  * File support for Three.js loaders, example OBJ, etc
  * Added percent offset for HUD placement
  * New samples index page for easy viewing once installed http://localhost:3000/samples
  * Experimantal shadow support plugin, not enabled by default
#### Hemi Library ####
  * Turned on antialiasing for all client renders
  * Added orthographic camera support
  * Added SharedClient sample
    * Allows for multiple simultaneous views of the same scene
  * Added Pump sample
    * Good example of keyframe animation support
  * Updated to the latest Three.js
### Bug Fixes ###
> #### World Editor ####
    * Enhanced COLLADA support
    * Numerous bug fixes
      * Most issues from 70 to 144 addressed
      * Tree progressive rendering bugs fixed
      * Behavior widget fixes
      * Transform handles functioning properly fixed
      * Fixed payload editor project sample
      * Fixed FirstAid editor project sample
      * Fixed issue with the case of model file extensions, DAE vs dae
> #### Hemi Library ####
    * Numerous bug fixes
      * Fixed issues with PressureHouseB sample
      * Curve bugs fixed, changing parameters while rendering
      * Restored curve draw function
### Other ###
  * Added a build.js node module to fix COLLADA files with missing samplers and surfaces
    * The fix is for files, usually Autodesk COLLADA exporter created, that have common shading effect diffuse or emission that directly reference a texture. A sampler and surface should be referenced per the 1.4.x spec.

## <font color='#336699'>Kuda 2.0.0 Release Notes (2012 February 14)</font> ##
### What's New ###
#### World Editor ####
  * World Editor COLLADA support
  * World Editor has new behavior transform actions
    * A transform action can also be a trigger
  * Added minified World Editor JavaScript
  * Ported World Editor to Kuda2 hemi
  * Updated samples built using the Kuda2 World Editor
#### Hemi Library ####
  * Ported hemi to three.js
    * Enhanced COLLADA support, added keyframe animation support
    * Enhanced particle effects, ported O3D's to hemi
  * Added firstAid sample
  * Added payload sample
  * Ported hext library to Kuda2 hemi
### Bug Fixes ###
> #### World Editor ####
    * Numerous bug fixes
> #### Hemi Library ####
    * Numerous bug fixes
### Other ###
    * Changed hemi license to MIT for better integration with three.js and other MIT style licensed projects