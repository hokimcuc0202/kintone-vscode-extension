# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kjs-app</td>
<td>
<pre>
var kintoneAuth = new kintoneJSSDK.Auth();
var paramsAuth = {
    username: 'YOUR_USER_NAME',
    password: 'YOUR_PASSWORD'
};
kintoneAuth.setPasswordAuth(paramsAuth);
 
var paramsConnection = {
    domain: 'YOUR_DOMAIN',
    auth: kintoneAuth
};
var connection = new kintoneJSSDK.Connection(paramsConnection);
 
// with connection
var kintoneApp = new kintoneJSSDK.App({connection});
 
// without connection, module will use session authentication of kintone
var kintoneApp = new kintoneJSSDK.App();
</pre>
</td>
<td>Constructor for App module</td>
</tr>

<tr>
<td>kjs-app-getApp</td>
<td>
<pre>
var id = YOUR_APP_ID;
kintoneApp.getApp({id}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Get single app</td>
</tr>

<tr>
<td>kjs-app-getApps</td>
<td>
<pre>
var limit = YOUR_LIMIT_NUMBER;
var offset = YOUR_OFFSET_NUMBER;
kintoneApp.getApps({offset, limit}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Get multiple apps</td>
</tr>

<tr>
<td>kjs-app-getAppsByIDs</td>
<td>
<pre>
var ids = [YOUR_APP_ID_1, YOUR_APP_ID_2, YOUR_APP_ID_n];
var limit = YOUR_LIMIT_NUMBER;
var offset = YOUR_OFFSET_NUMBER;
kintoneApp.getAppsByIDs({ids, offset, limit}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Get multiple apps by list of ids</td>
</tr>

<tr>
<td>kjs-app-getAppsByCodes </td>
<td>
<pre>
var codes = ['YOUR_APP_CODE_1', 'YOUR_APP_CODE_2'];
var limit = YOUR_LIMIT_NUMBER;
var offset = YOUR_OFFSET_NUMBER;
kintoneApp.getAppsByCodes({codes, offset, limit}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Get multiple apps by a list of codes name</td>
</tr>

<tr>
<td>kjs-app-getAppsByName </td>
<td>
<pre>
var name = 'YOUR_APP_NAME';
var limit = YOUR_LIMIT_NUMBER;
var offset = YOUR_OFFSET_NUMBER;
kintoneApp.getAppsByName({name, offset, limit}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Get multiple apps by name</td>
</tr>

<tr>
<td>kjs-app-getAppsBySpaceIDs </td>
<td>
<pre>
var spaceIds = [];
var limit = YOUR_LIMIT_NUMBER;
var offset = YOUR_OFFSET_NUMBER;
kintoneApp.getAppsBySpaceIDs({spaceIds, offset, limit}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Get multiple apps by list of space's ids </td>
</tr>

<tr>
<td>kjs-app-addPreviewApp</td>
<td>
<pre>
var name = 'YOUR_APP_NAME';
var space = YOUR_APP_SPACE_ID;
var thread = YOUR_THREAD_ID_OF_SPACE;
kintoneApp.addPreviewApp({name, space, thread}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Creates a preview App.</td>
</tr>

<tr>
<td>kjs-app-deployAppSettings</td>
<td>
<pre>
var apps = [
  {
    revision: YOUR_REVISION,
    app: YOUR_APP_ID
  }
// Another app preview here
];
var revert = false;
kintoneApp.deployAppSettings({apps, revert}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Updates the settings of a pre-live App to the live App.</td>
</tr>

<tr>
<td>kjs-app-getAppDeployStatus</td>
<td>
<pre>
var apps = [
  YOUR_APP_ID
// Another app id here
];
kintoneApp.getAppDeployStatus({apps}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Gets the deployment status of the App settings for multiple Apps.</td>
</tr>

<tr>
<td>kjs-app-getViews</td>
<td>
<pre>
var previewApp = YOUR_APP_ID;
var previewLang = 'LANGUAGE_CODE'; // Ex: JA
var isPreview = true;
kintoneApp.getViews({app: previewApp, lang: previewLang, isPreview}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Gets the View settings of a an App.</td>
</tr>

<tr>
<td>kjs-app-updateViews</td>
<td>
<pre>
var app = YOUR_APP_ID;
var views = {
  'YOUR_VIEW_NAME': {
    'index': 0,
    'type': 'YOUR_VIEW_TYPE', // Default: 'LIST', 'CALENDAR', 'CUSTOM'
    'name': 'YOUR_VIEW_NAME',
    'fields': [
      'YOUR_FIELD_CODE'
      // Another field code here
    ],
    'filterCond': 'YOUR_QUERY',
    'sort': 'YOUR_SORT'
  }
  // Another view here
};
var revision = 'YOUR_SETTINGS_REVISION';
 
kintoneApp.updateViews({app, views, revision}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Updates views in kintone app</td>
</tr>

<tr>
<td>kjs-app-getGeneralSettings</td>
<td>
<pre>	
var app = YOUR_APP_ID;
var lang = 'LANGUAGE_CODE'; // Ex: JA
kintoneApp.getGeneralSettings({app, lang}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
 
// Get a pre-live (preview) general settings
var app = YOUR_APP_ID;
var lang = 'LANGUAGE_CODE'; // Ex: JA
var isPreview = true;
kintoneApp.getGeneralSettings({app, lang, isPreview}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Gets the description, name, icon, revision and color theme of an App.</td>
</tr>

<tr>
<td>kjs-app-updateGeneralSettings</td>
<td>
<pre>
var params= {
  app: YOUR_APP_ID,
  name: 'YOUR_APP_NAME',
  description: 'YOUR_COOL_DESCRIPTION',
  icon: {
    type: 'YOUR_ICON_TYPE', // specified: FILE, PRESET
    key: 'YOUR_ICON_KEY'
  },
  theme: 'YOUR_THEME', // specified: WHITE, RED, BLUE, GREEN, YELLOW, BLACK
  revision: 'YOUR_SETTINGS_REVISION'
};
 
kintoneApp.updateGeneralSettings(params).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Update the description, name, icon, revision and color theme of an App.</td>
</tr>

<tr>
<td>kjs-app-getFormFields</td>
<td>
<pre>	
var app = YOUR_APP_ID;
var lang = 'LANGUAGE_CODE'; // Ex: JA
kintoneApp.getFormFields({app, lang}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
 
// Get a pre-live (preview) form fields
var app = YOUR_APP_ID;
var lang = 'LANGUAGE_CODE'; // Ex: JA
var isPreview = true;
kintoneApp.getFormFields({app, lang, isPreview}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Get field of form in kintone app</td>
</tr>

<tr>
<td>kjs-app-addFormFields</td>
<td>
<pre>
var app = YOUR_APP_ID;
var fields = {
  'YOUR_FIELD_CODE': {
    'type': 'SINGLE_LINE_TEXT',
    'code': 'YOUR_FIELD_CODE',
    'label': 'Text (single-line)',
    'noLabel': false,
    'required': true,
    'unique': true
  }
  // Another field here
};
var revision = 'YOUR_SETTINGS_REVISION';
kintoneApp.addFormFields({app, fields, revision}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Adds fields to a form of an App.</td>
</tr>

<tr>
<td>kjs-app-updateFormFields</td>
<td>
<pre>
var app = YOUR_APP_ID;
var fields = {
  'YOUR_FIELD_CODE': {
    'type': 'SINGLE_LINE_TEXT',
    'code': 'YOUR_FIELD_CODE',
    'label': 'Text (single-line)',
    'noLabel': false,
    'required': true,
    'unique': true
  }
  // Another field here
};
var revision = 'the_revision_of_the_settings ';
kintoneApp.updateFormFields({app, fields, revision}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Updates the field settings of fields in a form of an App.</td>
</tr>

<tr>
<td>kjs-app-deleteFormFields</td>
<td>
<pre>
var app = YOUR_APP_ID;
var fields = [
  'YOUR_FIELD_CODE'
  // Another field code here
];
var revision = 'YOUR_SETTINGS_REVISION';
kintoneApp.deleteFormFields({app, fields, revision}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Deletes the field settings of fields in a form of an App.</td>
</tr>

<tr>
<td>kjs-app-getFormLayout</td>
<td>
<pre>	
var isPreview = true;
kintoneApp.getFormLayout({app, isPreview}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Get layout of form in kintone app</td>
</tr>

<tr>
<td>kjs-app-updateFormLayout</td>
<td>
<pre>	
var app = YOUR_APP_ID;
var firstRowLayout = {
  'type': 'YOUR_LAYOUT_TYPE',
  'fields': [
    {
      'type': 'YOUR_FIELD_TYPE',
      'code': 'YOUR_FIELD_CODE',
      'size': {
        'width': 'YOUR_FIELD_WIDTH'
      }
    }
  ]
};
var layout = [
  firstRowLayout
  // Another row layout here
];
var revision = 'YOUR_SETTINGS_REVISION';
 
// Update form layout
kintoneApp.updateFormLayout({app, layout, revision}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Updates the field layout info of a form in an App.</td>
</tr>
</table>