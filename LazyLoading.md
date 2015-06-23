## <font color='#336699'>Lazy Loading</font> ##

### Why ###

In SCORM learning modules on NWTP, each SCO is actually one HTML page that has sections that are displayed one at a time as virtual pages. If a SCO contains multiple pages with 3D assets, all of those assets have to load their resources and initialize before the first virtual page becomes responsive. For SCOs with several large 3D assets, this can create a poor user experience and may even create problems with the browser timing out. We decided to implement a "lazy loading" mechanism that will allow Kuda assets to wait to initialize until their virtual page is actually viewed by the user.

### How ###

The makeClients() function call is used to initialize a Kuda asset and is called for each asset in a SCO. Typically the function call is keyed off of the window load event. Because all of the "pages" of a SCO are all on one HTML page, they all get the window load event at once. NWTP's SCORM player sends a special event to each virtual page when it is being displayed, so the Kuda asset can key off of that instead of the window load event. The event is named "kuda-display". It is important to only key off of this event once, since it can be sent multiple times if a user navigates away from a page and then back to it.

### Example ###

This is how a Kuda asset might be initialized normally:
```
jQuery(window).load(function() {
   o3djs.webgl.makeClients(initStep);
});
```
To use the lazy loading, that piece of code would be changed to this:
```
jQuery(window).bind('kuda-display', function() {
   jQuery(window).unbind('kuda-display');
   o3djs.webgl.makeClients(initStep);
});
```
Note that you need to unbind from the event so that the Kuda asset does not try to initialize again if the user navigates away from the page and then back to it.

Also, changing your code this way means that it will only load in the context of an NWTP SCORM player. If you want your asset to lazy load in NWTP but load normally in other contexts, you can check for the Runtime property as shown below:
```
if (window.top.Runtime) {
   jQuery(window).bind('kuda-display', function() {
      jQuery(window).unbind('kuda-display');
      o3djs.webgl.makeClients(initStep);
   });
} else {
   jQuery(window).load(function() {
      o3djs.webgl.makeClients(initStep);
   });
}
```