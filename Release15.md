## <font color='#336699'>Kuda 1.5.1 Release Notes (2011 November 30)</font> ##
### What's New ###
#### World Editor ####
  * Added accessibility object to work with 3d and non 3d elements in an asset  (JHT Contribution)
  * Various enhancements to the plugin API and plugin tools based on feedback and big reports
  * Added hover and selected to for hud buttons (JHT Contribution)
  * Added experimental Google Chrome support to import and load models from the local file system
#### Hemi Library ####
  * Added convenience function for creating lambert shaded material. Incorporated into particle curves
  * Added option for GpuParticleTrail to do a hard stop
  * Added experimental WebSocket example and support with nodejs

### Bug Fixes ###
> #### World Editor ####
    * [Issue 133](https://code.google.com/p/kuda/issues/detail?id=133): World Editor 3D perspective view does not show up in Chrome 15 on Windows 7 32 and 64 bit
> #### Hemi Library ####
    * Fixed loading bug caused by not checking lengthComputable flag. Reduced division operations as well


### Other ###
  * Updated README and new wiki page "Running the Editor" DownloadAndRunLocal
    * With new Windows and Mac install and simple shortcut creation instructions


## <font color='#336699'>Kuda 1.5.0 Release Notes (2011 October 11)</font> ##
### What's New ###
#### World Editor ####
  * Added dependency manager
    * The editor will warn the user when they attempt to remove an object that is used in multiple places within the editor, thus breaking the dependency chain.
  * Editor reworked from the ground up with a core plugin architecture
    * New look and feel for easier usage
    * All editor tools and functions are implemented as plugins
    * Plugins folder for easy deployment and access to developer plugins
    * Behaviors are in a table for easy searching and sorting
    * Plus more features in the API to make plugin development more productive
  * New app.js for running the World Editor using Nodejs
    * Can run using the native Windows node.exe for super simple installs
    * No external dependencies and need for npm modules
    * Consolidated inheritance style with the Kuda library
### Bug Fixes ###
#### World Editor ####
  * 100+ bugs addressed and resolved during release testing. To many to list here. Please see the commit logs for details.
> #### Kuda Library ####
    * Replaced inheritance scheme with enhanced best practices implementation
      * Consolidated with the Kuda World Editor style