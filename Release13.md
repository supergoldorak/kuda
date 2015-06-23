## <font color='#336699'>Kuda 1.3.2 Release Notes (2011 May 13)</font> ##
### Bug Fixes ###
#### Kuda Library ####
  * [Issue21](http://code.google.com/p/kuda/issues/detail?id=21&can=1) Missing bug fix from 1.3.1 tag which resolved a starting system "black ball" bug

## <font color='#336699'>Kuda 1.3.1 Release Notes (2011 May 11)</font> ##
### What's New ###
#### World Editor ####
  * Enhanced Preview function now renders previewed world in the same GL context that the Editor runs in.
#### Kuda Library ####
  * New curve particle system that is shader-based for vastly increased performance.
    * System can run as an emitter or as a trail
    * Optional particle orientation, color ramping, curve tension, etc.
  * New Hext SharedModel module for sharing a model's archiveinfo across multiple iframes.
  * New Hext Debug module that adds class and module names for readability when debugging.
  * Render cycle now takes advantage of requestAnimationFrame.
  * Progress messages can now be sent by any process, not just resource loading ones.
  * Created sample for the new GPU particle system.
  * Created sample for slides presentation from WebGL Camp #2.

### Bug Fixes ###
#### World Editor ####
  * Messaging tool would sometimes lose its third column.
  * Grid lines in model browser occasionally obscured geometry.
  * Javascript error would pop up when editing an existing Shape.
  * Transform handles in model browser would sometimes draw too small or large to be usable.
#### Kuda Library ####
  * Progress messages were not providing accurate information when loading models.
  * Bounding boxes were not correctly (re)calculated for o3d Transforms.
  * Performance issues with Hext progress bar.
  * Camera's update function could get stuck in infinite call cycle.
  * Camera's FOV and clipping planes would not update when moving to a Viewpoint.

## <font color='#336699'>Kuda 1.3.0 Release Notes (2011 April 12)</font> ##
### What's New ###
#### World Editor ####
  * Handles for rotation/translation/scaling added
  * Templates for particle effects
  * Material list and texture viewer added to model browser
  * Moved to node.js and express server in order to run as a web app
  * Project saving and loading: can now name projects and select projects from a list to load.
  * Form field validation added (though not to all the forms yet)
  * New UI for translation/rotation/scaling
    * Now have graphical handles centered around transforms that can be clicked and dragged to manipulate
#### Kuda Library ####
  * Kuda ported from O3D plugin to WebGL
  * HUD updated to use HTML5 canvas element
  * HUD now has support for HTML5 video element
  * HUD pages now have an option for rounded corners
  * Audio support expanded to use HTML5 audio element
  * Added material opacity feature to fx (from FadingWalls demo)
  * Draggable, Turnable, and Scalable manips can now operate in either world space or local space
  * Curve now has the option to specify if particles should rotate with curve or not
  * All samples updated to run on WebGL

### Bug Fixes ###
#### World Editor ####
  * Problems with multiple select in model browser fixed
  * Problems with animation form fixed (where a model has no animation)
  * Problems with particle effects form fixed
    * Color pickers in the color ramp field now operate correctly
    * Javascript errors from saving/editing/canceling and then creating a new effect have now been fixed
  * Fixed overlapping dialog boxes (shouldn't occur anymore)
#### Kuda Library ####
  * Bugs in manip, motion, and shape related to transform hierarchy fixed
  * Fixed bug with loading Octane from non-local file