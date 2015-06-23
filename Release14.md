## <font color='#336699'>Kuda 1.4.3 Release Notes (2011 September 7)</font> ##
### What's New ###
#### World Editor ####
  * Trigger "messages" now have tool tips
  * Improved the speed of loading saved projects
  * Added a dependency manager
    * Notify user if editor created object, example camera viewpoint, has dependencies, example a move to view behavior
### Bug Fixes ###
#### World Editor ####
  * Stop preview would stop working under certain conditions
  * Tranform applied to keyframe-animated object crashes editor
  * Clicking on left-side editor selection button kills right side panel
  * Problems previewing motions and manips with keyframed transforms
  * Timer panel doesn't list all timers
  * Path to support files are incorrect in published html file
  * Rotator defaults to disabled and ignores a disable when rotate is called
  * Model loader lists non-model directories
  * Rotator motion does not update the angle when previewing
  * HUD text not editable after save
  * Fixed support for instant move or rotate action for motions, support 0 time
  * Changing particle color kills particles for the session
#### Kuda Library ####
  * Fixed O3D WebGL skinned mesh support
    * Bounding boxes were not being calculated correctly

## <font color='#336699'>Kuda 1.4.1 Release Notes (2011 August 9)</font> ##
### What's New ###

Special Note: This release has single minified versions of Kuda hemi and o3d. Please use these files. We also discourage the use of o3djs.require, it is deprecated within Kuda as of this release, and our samples no longer use it.

#### World Editor ####
  * Allows a hidden transform to be made pickable as a behavior. This allows the editor author to use simple select objects for more complex objects.
  * Has a new timer behavior
  * Has an added unloading models menu function
  * Has behavior tooltips for trigger objects and actions. Parameters also have tooltips and more complex input types
#### Kuda Library ####
  * Library concatenation into a single file and minification for performance. The build produces both hemi and o3d  source and minified files.
### Noted Bug Fixes ###
  * Editor has numerous bug fixes, please see the verified issues project page

## <font color='#336699'>Kuda 1.4.0 Release Notes (2011 July 1)</font> ##
### What's New ###
#### World Editor ####
  * File browser for models
  * Publish a project, it creates the html etc needed to put projects anywhere on the web
  * Set opacity on model materials
  * Edit and put the camera on a GUI defined curve
  * Create and modify live particle system curves
  * Import models that are zipped
  * New timer trigger
  * Set behaviors at the tool level without going into behavior editing
  * Numerous bug fixes and minor improvements as mentioned on the site
#### Kuda Library ####
  * Library has GPU based particle system which has much greater performance
### Bug Fixes ###