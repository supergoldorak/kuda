## <font color='#336699'>SCORM API</font> ##

### Why ###

Media and content authors may need direct access the SCORM API for SCORM tracking from their content. In SCORM learning modules on NWTP the SCORM tracking is automatically handled by NWTP authored modules within the system. This is done at authoring time using the insert question operation.

Access to the SCORM API is done using JavaScript. An NWTP authored module with an html media item can directly access the API from included scripts. This includes Kuda media assets.

### How ###

The NWTP (ILIAS) environment loads the SCORM JavaScript RTE and a scorm.js light wrapper. The SCORM JavaScript RTE is a top level object "ScormApi" and scorm.js adds top level functions matching most of the SCORM API. Media assets inside a SCO authored by NWTP are placed inside an IFRAME. Access the api through the window.parent namespace.

The SCORM datamodel CMI elements such as cmi.score.raw, cmi.success\_status, cmi.completion\_status, and cmi.location can be accessed through the API's GetValue and SetValue functions.

NOTE: Use of the cmi.location element should be tested in a published SCO.

### Example ###

This shows how to immediately set the completion status to completed:
```
var ScormApi = window.parent.ScormApi;

ScormApi.SetValue('cmi.completion_status', 'completed');
```

NOTE: Make sure the SCORM RTE has loaded using lazy loading or timer.