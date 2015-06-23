## <font color='#336699'>Shared Model</font> ##

### Why ###

NWTP's SCORM learning modules place Kuda assets inside iframes, which means each asset is its own stand-alone page with its own copy of the kuda hemi library and its own assets. Due to asset size, this can be a big burden on page load in the SCORM player. This becomes a problem when the same asset gets loaded multiple times due to being included in multiple iframes. We created a shared model hext extension to help alleviate this specific instance.

### How ###

When loading an asset, the .json file gets loaded and parsed via an XmlHTTPRequest and then deserialized. The deserialization process needs to occur in each instance in order for loading to properly occur, but the load process need only occur once. The shared model hext extension overrides this process, interjecting a model manager which keeps track of models at the level above the iframe. When a call gets made to load a model in the iframe, the model manager checks against its list of names, and if found, adds the callee to the list of instances to notify when the model has loaded. This way, loading happens only once for a specific model.

### Example ###

This is how loading a model normally gets called:
```
var house = new hemi.model.Model();			  // Create a new Model
house.setFileName('assets/house_v12/scene.json');         // Set the model file, which begins the loading process
```
To use the shared model extension, you only need to add one line:
```
o3djs.require('hext.sharedModel.modelManager');
```
Or you can add this in the html file instead
```
<script type="text/javascript" src="/path/to/hext/sharedModel/modelManager.js">
</script>
```

**Note: This refers to the version available in the upcoming 1.4.1 release since the previous version has a bug**