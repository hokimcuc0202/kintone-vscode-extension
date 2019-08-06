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
const kintoneApp = new kintone.App(connection);
</pre>
</td>
<td>Constructor for App module</td>
</tr>

<tr>
<td>kjs-app-getApp</td>
<td>
<pre>
const appId = 'your_app_id';
  kintoneApp.getApp(appId).then((rsp) => {
    console.log(rsp);
  }).catch((err) => {
    // This SDK return err with KintoneAPIExeption
    console.log(err.get());
  });
</pre>
</td>
<td>Get single app</td>
</tr>

<tr>
<td>kjs-app-getApps</td>
<td>
<pre>
const limit = 'your_limit_number';
const offset = 'your_offset_number';
kintoneApp.getApps(offset, limit).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Get multiple apps</td>
</tr>

<tr>
<td>kjs-app-getAppsByIDs</td>
<td>
<pre>
const appIDs = ['YOUR_APP_ID_1', 'YOUR_APP_ID_2', 'YOUR_APP_ID_n'];
const limit = 'your_limit_number';
const offset = 'your_offset_number';
kintoneApp.getAppsByIDs(appIDs, offset, limit).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Get multiple apps by list of ids</td>
</tr>

<tr>
<td>kjs-app-getAppsByCodes </td>
<td>
<pre>
const codes = ['YOUR_APP_CODE_1', 'YOUR_APP_CODE_2'];
const limit = 'your_limit_number';
const offset = 'your_offset_number';
kintoneApp.getAppsByCodes(codes, offset, limit).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Get multiple apps by a list of codes name</td>
</tr>

<tr>
<td>kjs-app-getAppsByName </td>
<td>
<pre>
const name = 'your app name';
const limit = /*{your_limit_number}*/;
const offset = /*{your_offset_number}*/;
kintoneApp.getAppsByName(name, offset, limit).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Get multiple apps by name</td>
</tr>

<tr>
<td>kjs-app-getAppsBySpaceIDs </td>
<td>
<pre>
const spaceIds = [];
const limit = /*{your_limit_number}*/;
const offset = /*{your_offset_number}*/;
kintoneApp.getAppsBySpaceIDs(spaceIds, offset, limit).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Get multiple apps by list of space's ids </td>
</tr>

<tr>
<td>kjs-app-getAppsBySpaceIDs </td>
<td>
<pre>
const spaceIds = [];
const limit = /*{your_limit_number}*/;
const offset = /*{your_offset_number}*/;
kintoneApp.getAppsBySpaceIDs(spaceIds, offset, limit).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Get multiple apps by list of space's ids </td>
</tr>

<tr>
<td>kjs-app-addPreviewApp</td>
<td>
<pre>
const name = {your_app_name};
const space = {space_of_app};
const thread = {thread_id_in_space};
kintoneApp.addPreviewApp(name, space, thread).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Creates a preview App.</td>
</tr>

<tr>
<td>kjs-app-deployAppSettings</td>
<td>
<pre>
const apps = [
    appPreview
    // Another app preview here
];
const revert = false;
kintoneApp.deployAppSettings(apps, revert).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Updates the settings of a pre-live App to the live App.</td>
</tr>

<tr>
<td>kjs-app-getAppDeployStatus</td>
<td>
<pre>
const apps = [
    'your_app_id'
    // Another app id here
];
kintoneApp.getAppDeployStatus(apps).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Gets the deployment status of the App settings for multiple Apps.</td>
</tr>

<tr>
<td>kjs-app-getViews</td>
<td>
<pre>
const app = {your_app_id};
const lang = {language_code}; // Ex: JA
kintoneApp.getViews(app, lang).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
 
// Get a pre-live (preview) views
const app = {your_app_id};
const lang = {language_code}; // Ex: JA
const isPreview = true;
kintoneApp.getViews(app, lang, isPreview).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Gets the View settings of a an App.</td>
</tr>

<tr>
<td>kjs-app-updateViews</td>
<td>
<pre>
const app = {your_app_id};
const views = {
    "Your_view_name": {
      "index": 0,
      "type": "your_view_type", // Default: 'LIST', 'CALENDAR', 'CUSTOM'
      "name": "Your_view_name",
      "fields": [
        "your_field_code"
        // Another field code here
      ],
      "filterCond": "your_query",
      "sort": "your_sort"     
    }
    // Another view here
};
const revision: 'settings_revision';
 
kintoneApp.updateViews(app, views, revision).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Updates views in kintone app</td>
</tr>

<tr>
<td>kjs-app-getGeneralSettings</td>
<td>
<pre>
const app = {your_app_id};
const lang = {language_code}; // Ex: JA
kintoneApp.getGeneralSettings(app, lang).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
 
// Get a pre-live (preview) general settings
const app = {your_app_id};
const lang = {language_code}; // Ex: JA
const isPreview = true;
kintoneApp.getGeneralSettings(app, lang, isPreview).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Gets the description, name, icon, revision and color theme of an App.</td>
</tr>

<tr>
<td>kjs-app-updateGeneralSettings</td>
<td>
<pre>
const app = {your_app_id};
const generalSettings = {
  'name': 'APP_NAME',
  'description': 'Here is app description.',
  'icon': {
    'type': 'icon_type', // specified: FILE, PRESET
    'key': 'icon_key'
  },
  'theme': 'your_theme' // specified: WHITE, RED, BLUE, GREEN, YELLOW, BLACK
};
const revision = 'settings_revision';
 
kintoneApp.updateGeneralSettings(app, generalSettings, revision).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Update the description, name, icon, revision and color theme of an App.</td>
</tr>

<tr>
<td>kjs-app-getFormFields</td>
<td>
<pre>
const app = {your_app_id};
const lang = {language_code}; // Ex: JA
kintoneApp.getFormFields(app, lang).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
 
// Get a pre-live (preview) form fields
const app = {your_app_id};
const lang = {language_code}; // Ex: JA
const isPreview = true;
kintoneApp.getFormFields(app, lang, isPreview).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Get field of form in kintone app</td>
</tr>

<tr>
<td>kjs-app-addFormFields</td>
<td>
<pre>
const app = {your_app_id};
const fields = {
  YourFieldCode: {
    'type': 'SINGLE_LINE_TEXT',
    'code': 'YourFieldCode',
    'label': 'Text (single-line)',
    'noLabel': false,
    'required': true,
    'unique': true
  }
  // Another field here
};
const revision = 'the_revision_of_the_settings ';
kintoneApp.addFormFields(app, fields, revision).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Adds fields to a form of an App.</td>
</tr>

<tr>
<td>kjs-app-updateFormFields</td>
<td>
<pre>
const app = {your_app_id};
const fields = {
  YourFieldCode: {
    'type': 'SINGLE_LINE_TEXT',
    'code': 'YourFieldCode',
    'label': 'Text (single-line)',
    'noLabel': false,
    'required': true,
    'unique': true
  }
  // Another field here
};
const revision = 'the_revision_of_the_settings ';
kintoneApp.updateFormFields(app, fields, revision).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Updates the field settings of fields in a form of an App.</td>
</tr>

<tr>
<td>kjs-app-deleteFormFields</td>
<td>
<pre>
const app = {your_app_id};
const fields = [
  'your_field_cde'
  // Another field code here
];
const revision = 'revision_of_the_Settings ';
kintoneApp.deleteFormFields(app, fields, revision).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Deletes the field settings of fields in a form of an App.</td>
</tr>

<tr>
<td>kjs-app-getFormLayout</td>
<td>
<pre>	
const app = {your_app_id};
// Get form layout
kintoneApp.getFormLayout(app).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
 
// Get a preview (pre-live) form layout
const isPreview = true;
kintoneApp.getFormLayout(app, isPreview).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Get layout of form in kintone app</td>
</tr>

<tr>
<td>kjs-app-updateFormLayout</td>
<td>
<pre>
const app = {your_app_id};
const fisrtRowLayout = {
  'type': 'kintone_layout_type',
  'fields': [
    {
      'type': 'kintone_field_type',
      'code': 'your_field_code',
      'size': {
        'width': 'your_field_width'
      }
    }
  ]
};
const layout = [
  fisrtRowLayout
// Another row layout here
];
const revision = 'settings_revision';
 
// Update form layout
kintoneApp.updateFormLayout(app, layout, revision).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
// This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Updates the field layout info of a form in an App.</td>
</tr>
</table>