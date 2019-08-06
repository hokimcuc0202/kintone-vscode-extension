# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>ka-app-get</td>
<td>
<pre>
var body = {
    "id": 1
};
kintone.api(kintone.api.url('/k/v1/app', true), 'GET', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Gets general information of an App, including the name, description, related Space, creator and updater information.</td>
</tr>
<tr>
<td>ka-apps-get</td>
<td>
<pre>
kintone.api(kintone.api.url('/k/v1/apps', true), 'GET', {}, function(resp) {
// success
console.log(resp);
}, function(error) {
// error
console.log(error);
});
</pre>
</td>
<td>Gets general information of multiple Apps, including the name, description, related Space, creator and updater information.</td>
</tr>
<tr>
<td>ka-app-add_preview</td>
<td>
<pre>

var body = {
    "name": "APP_NAME",
    "space": 10,
    "thread": 11
}
 
kintone.api(kintone.api.url('/k/v1/preview/app', true), 'POST', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Creates a preview App.</td>
</tr>
<tr>
<td>ka-app-get</td>
<td>
<pre>

</pre>
</td>
<td></td>
</tr>
<tr>
<td>ka-app-add_preview</td>
<td>
<pre>
var body = {
    "name": "APP_NAME",
    "space": 10,
    "thread": 11
}
 
kintone.api(kintone.api.url('/k/v1/preview/app', true), 'POST', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Creates a preview App.</td>
</tr>
<tr>
<td>ka-app-deploy</td>
<td>
<pre>
var body = {
    "apps": [
        {
            "app": 1,
            "revision": 57
        },
        {
            "app": 1001,
            "revision": 22
        }
    ],
    "revert": true
};
 
kintone.api(kintone.api.url('/k/v1/preview/app/deploy', true), 'POST', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Updates the settings of a pre-live App to the live App.</td>
</tr>
<tr>
<td>ka-app-get-deploy </td>
<td>
<pre>
var body = {
    "apps": [1, 1001]
};
 
kintone.api(kintone.api.url('/k/v1/preview/app/deploy', true), 'GET', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Gets the deployment status of the App settings for multiple Apps.</td>
</tr>
<tr>
<td>ka-app-get-formFields</td>
<td>
<pre>
var body = {
    "app": 1
};
 
kintone.api(kintone.api.url('/k/v1/app/form/fields', true), 'GET', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Gets the list of fields and field settings of an App.</td>
</tr>
<tr>
<td>ka-app-add-formFields</td>
<td>
<pre>
var body = {
  "app": 1,
  "properties": {
    "Text__single_line_1": {
      "type": "SINGLE_LINE_TEXT",
      "code": "Text__single_line_1",
      "label": "Text (single-line)",
      "noLabel": false,
      "required": true,
      "unique": true,
      "maxLength": 64,
      "minLength": 0,
      "defaultValue": "",
      "expression": "",
      "hideExpression": false
    },
    "Number": {
      "type": "NUMBER",
      "code": "Number",
      "label": "Number",
      "noLabel": true,
      "required": false,
      "unique": false,
      "maxValue": 64,
      "minValue": 0,
      "defaultValue": "12345",
      "expression": "",
      "digit": true,
      "displayScale": "",
      "unit": "$",
      "unitPosition": "BEFORE"
    }
  }
};
 
kintone.api(kintone.api.url('/k/v1/preview/app/form/fields', true), 'POST', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Adds fields to a form of an App.</td>
</tr>
<tr>
<td>ka-app-update-formFields</td>
<td>
<pre>
var body = {
  "app": 1,
  "properties": {
    "Text__single_line_1": {
      "type": "SINGLE_LINE_TEXT",
      "code": "Text__single_line_1",
      "label": "Text (single-line)",
      "noLabel": false,
      "required": true,
      "unique": true,
      "maxLength": 64,
      "minLength": 0,
      "defaultValue": "",
      "expression": "",
      "hideExpression": false
    },
    "Number": {
      "type": "NUMBER",
      "code": "Number",
      "label": "Number",
      "noLabel": true,
      "required": false,
      "unique": false,
      "maxValue": 64,
      "minValue": 0,
      "defaultValue": "12345",
      "digit": true,
      "displayScale": "",
      "expression": "",
      "unit": "$",
      "unitPosition": "BEFORE"
    }
  }
};
 
kintone.api(kintone.api.url('/k/v1/preview/app/form/fields', true), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Updates the field settings of fields in a form of an App.</td>
</tr>
<tr>
<td>ka-app-delete-formFields</td>
<td>
<pre>
var body = {
    "app": 1,
    "fields": [
        "Text__single_line_1",
        "Number"
    ]
}
 
kintone.api(kintone.api.url('/k/v1/preview/app/form/fields', true), 'DELETE', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Deletes fields from a form of an App.</td>
</tr>
<tr>
<td>ka-app-get-formLayout</td>
<td>
<pre>
var body = {
    "app": 1
};
 
kintone.api(kintone.api.url('/k/v1/app/form/layout', true), 'GET', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Gets the field layout info of a form in an App.</td>
</tr>
<tr>
<td>ka-app-update-formLayout</td>
<td>
<pre>
var body = {
  "app": 1,
  "layout": [
        {
            "type": "ROW",
            "fields": [
                {
                    "type": "SINGLE_LINE_TEXT",
                    "code": "Text__single_line_",
                    "size": {
                        "width": "200"
                    }
                }
            ]
        },
        {
            "type": "SUBTABLE",
            "code": "Table",
            "fields": [
                {
                    "type": "SINGLE_LINE_TEXT",
                    "code": "Text2__single_line_",
                    "size": {
                        "width": "193"
                    }
                },
                {
                    "type": "MULTI_LINE_TEXT",
                    "code": "Text_Box__multi_line_",
                    "size": {
                        "width": "315",
                        "innerHeight": "125"
                    }
                }
            ]
        },
        {
            "type": "ROW",
            "fields": [
                {
                    "type": "NUMBER",
                    "code": "Number",
                    "size": {
                        "width": "193"
                    }
                }
            ]
        },
        {
            "type": "ROW",
            "fields": [
                {
                    "type": "RECORD_NUMBER",
                    "code": "Record_number",
                    "size": {
                        "width": "141"
                    }
                },
                {
                    "type": "CREATOR",
                    "code": "Created_by",
                    "size": {
                        "width": "136"
                    }
                }
            ]
        }
    ]
};
 
kintone.api(kintone.api.url('/k/v1/preview/app/form/layout', true), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Updates the field layout info of a form in an App.</td>
</tr>
<tr>
<td>ka-app-get-views</td>
<td>
<pre>
var body = {
    "app": 1,
    "lang": "en"
};
 
kintone.api(kintone.api.url('/k/v1/app/views', true), 'GET', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Gets the View settings of an App.</td>
</tr>
<tr>
<td>ka-app-update-views</td>
<td>
<pre>
var body = {
  "app": 1,
  "views": {
    "My List View": {
      "index": 0,
      "type": "LIST",
      "name": "My List View",
      "fields": [
        "Record_number",
        "Text_single_line"
      ],
      "filterCond": "Updated_datetime > LAST_WEEK()",
      "sort": "Record_number asc"     
    },
    "My Calendar View": {
      "index": 1,
      "type": "CALENDAR",
      "name": "My Calendar View",
      "date": "Updated_datetime",
      "title": "Rich_text",
      "filterCond": "",
      "sort": "Record_number asc"
    },
    "My Custom View": {
      "index": 2,
      "type": "CUSTOM",
      "html": "<div>Custom View HTML</div>",
      "filterCond": "Updated_datetime >= LAST_WEEK() and Updated_datetime <= TODAY()",
      "sort": "Record_number asc"
    },
    "(Assigned to me)": {
      "index": 3,
      "type": "LIST"
    }
  }
};
 
kintone.api(kintone.api.url('/k/v1/preview/app/views', true), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Updates the View settings of an App.</td>
</tr>
<tr>
<td>ka-app-get-generalSettings</td>
<td>
<pre>
var body = {
    "app": 1,
    "lang": "en"
};
 
kintone.api(kintone.api.url('/k/v1/app/settings', true), 'GET', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Gets the description, name, icon, revision and color theme of an App.</td>
</tr>
<tr>
<td>ka-app-update-generalSettings</td>
<td>
<pre>
var body = {
    "app": 1,
    "name": "APP_NAME",
    "description": "Here is app description.",
    "icon": {
      "type": "PRESET",
      "key": "APP72"
    },
    "theme": "WHITE"
}
 
kintone.api(kintone.api.url('/k/v1/preview/app/settings', true), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Updates the description, name, icon, revision and color theme of an App.</td>
</tr>
<tr>
<td>ka-app-get-processManagementSettings</td>
<td>
<pre>
var body = {
    "app": 1
};
 
kintone.api(kintone.api.url('/k/v1/app/status', true), 'GET', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Gets the process management settings of an App.</td>
</tr>

<tr>
<td>ka-app-update-processManagementSettings</td>
<td>
<pre>
var body = {
    "app": "5",
    "enable": true,
    "states": {
        "Not started": {
            "name": "Not started",
            "index": "0",
            "assignee": {
                "type": "ONE",
                "entities": [
                ]
            }
        },
        "In progress": {
            "name": "In progress",
            "index": "1",
            "assignee": {
                "type": "ALL",
                "entities": [
                    {
                        "entity": {
                            "type": "USER",
                            "code": "user1"
                        },
                        "includeSubs": false
                    },
                    {
                        "entity": {
                            "type": "FIELD_ENTITY",
                            "code": "creator"
                        },
                        "includeSubs": false
                    },
                    {
                        "entity": {
                            "type": "CUSTOM_FIELD",
                            "code": "Boss"
                        },
                        "includeSubs": false
                    }
                ]
            }
        },
        "Completed": {
            "name": "Completed",
            "index": "2",
            "assignee": {
                "type": "ONE",
                "entities": [
                ]
            }
        }
    },
    "actions": [
        {
            "name": "Start",
            "from": "Not started",
            "to": "In progress",
            "filterCond": "Record_number = \"1\""
        },
        {
            "name": "Complete",
            "from": "In progress",
            "to": "Completed",
            "filterCond": ""
        }
    ]
};
 
kintone.api(kintone.api.url('/k/v1/preview/app/status', true), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Updates the process management settings of an App.</td>
</tr>
</table>

<tr>
<td>ka-app-get-customization</td>
<td>
<pre>
var body = {
    "app": 1
};
 
kintone.api(kintone.api.url('/k/v1/app/customize', true), 'GET', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Gets the JavaScript and CSS Customization settings of an App.</td>
</tr>
</table>

<tr>
<td>ka-app-update-customization</td>
<td>
<pre>
var body = {
    "app": 1,
    "scope": "ALL",
    "desktop": {
        "js": [
            {
                "type": "URL",
                "url": "https://www.example.com/example.js"
            },
            {
                "type": "FILE",
                "file": {
                    "fileKey": "ddfc8e89-7aa3-4350-b9ab-3a75c9cf46b3"
                }
            }
        ],
        "css": []
    },
    "mobile": {
        "js": [
            {
                "type": "FILE",
                "file": {
                    "fileKey": "20150519023802B3EB762E870645F889B22F9D4F1F3059023"
                }
            },
            {
                "type": "URL",
                "url": "https://www.example.com/example-mobile.js"
            }
        ]
    }
}
 
kintone.api(kintone.api.url('/k/v1/preview/app/customize', true), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Updates the JavaScript and CSS Customization settings of an App.</td>
</tr>
</table>

<tr>
<td>ka-app-get-appPermissions</td>
<td>
<pre>
var body = {
    "app": 1
};
 
kintone.api(kintone.api.url('/k/v1/app/acl', true), 'GET', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Gets the App permissions of an app.</td>
</tr>
</table>

<tr>
<td>ka-app-update-appPermissions</td>
<td>
<pre>
var body = {
    "app": 1,
    "rights": [
        {
            "entity": {
                "type": "USER",
                "code": "user1"
            },
            "appEditable": true,
            "recordViewable": true,
            "recordAddable": true,
            "recordEditable": true,
            "recordDeletable": true,
            "recordImportable": true,
            "recordExportable": true
        },
        {
            "entity": {
                "type": "GROUP",
                "code": "everyone"
            },
            "includeSubs": true,
            "appEditable": true,
            "recordViewable": true,
            "recordAddable": true,
            "recordEditable": true,
            "recordDeletable": true,
            "recordImportable": false,
            "recordExportable": false
        },
        {
            "entity": {
                "type": "CREATOR"
            },
            "appEditable": true,
            "recordViewable": true,
            "recordAddable": true,
            "recordEditable": true,
            "recordDeletable": true,
            "recordImportable": true,
            "recordExportable": true
        }
    ]
};
 
kintone.api(kintone.api.url('/k/v1/app/acl', true), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Updates the App permissions of an App.</td>
</tr>
</table>

<tr>
<td>ka-app-get-recordPermissions</td>
<td>
<pre>
var body = {
    "app": 1
};
 
kintone.api(kintone.api.url('/k/v1/record/acl', true), 'GET', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Gets the Record permission settings of an App.</td>
</tr>
</table>

<tr>
<td>ka-app-update-recordPermissions</td>
<td>
<pre>
var body = {
    "app": 1,
    "rights": [
        {
            "filterCond": "Updated_datetime > \"2012-02-03T09:00:00Z\" and Updated_datetime < \"2012-02-03T10:00:00Z\"",
            "entities": [
                {
                    "entity": {
                        "type": "ORGANIZATION",
                        "code": "org1"
                    },
                    "viewable": false,
                    "editable": false,
                    "deletable": false,
                    "includeSubs": true
                },
                {
                    "entity": {
                        "type": "FIELD_ENTITY",
                        "code": "Updated_by"
                    },
                    "viewable": true,
                    "editable": true,
                    "deletable": true
                }
            ]
        }
    ]
};
 
kintone.api(kintone.api.url('/k/v1/record/acl', true), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Updates the Record permission settings of an App.</td>
</tr>

<tr>
<td>ka-app-get-fieldPermissions</td>
<td>
<pre>

var body = {
    "app": 1
};
 
kintone.api(kintone.api.url('/k/v1/field/acl', true), 'GET', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Gets the Field permission settings of an App.</td>
</tr>

<tr>
<td>ka-app-update-fieldPermissions</td>
<td>
<pre>
var body = {
    "app": 1,
    "rights": [
        {
            "code": "Text__single_line_",
            "entities": [
                {
                    "accessibility": "WRITE",
                    "entity": {
                        "type": "USER",
                        "code": "user1"
                    }
                },
                {
                    "accessibility": "READ",
                    "entity": {
                        "type": "GROUP",
                        "code": "group1"
                    }
                }
            ]
        },
        {
            "code": "Number",
            "entities": [
                {
                    "accessibility": "NONE",
                    "entity": {
                        "type": "ORGANIZATION",
                        "code": "org1"
                    },
                    "includeSubs": true
                }
            ]
        }
    ]
};
 
kintone.api(kintone.api.url('/k/v1/field/acl', true), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Updates the Field permission settings of an App.</td>
</tr>

<tr>
<td>ka-app-evaluate-recordPermission</td>
<td>
<pre>
var body = {
    "app": 1,
    "ids": [1, 2]
};
 
kintone.api(kintone.api.url('/k/v1/records/acl/evaluate', true), 'GET', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Evaluates the API user's permissions for records and fields within an App.</td>
</tr>
</table>