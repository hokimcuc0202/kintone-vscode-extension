# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>ka-record-get-record</td>
<td>
<pre>
kintone.api(kintone.api.url('/k/v1/record', true) + '?app=20&id=100', 'GET', {}, function(resp) {
    // success
    console.log(resp)
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Retrieves details of 1 record from an App by specifying the App ID and Record ID.</td>
</tr>

<tr>
<td>ka-record-get-records</td>
<td>
<pre>
var query = 'Created_by in (LOGINUSER()) and Created_datetime = TODAY() order by $id asc limit 100 offset 0'
var fields = '&fields[0]=$id&fields[1]=Created_by&fields[2]=Created_datetime'
kintone.api(kintone.api.url('/k/v1/records', true) + '?app=8&query=' + query + fields, 'GET', {}, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Retrieves details of multiple records from an App by specifying the App ID and a query string.</td>
</tr>

<tr>
<td>ka-record-add-record</td>
<td>
<pre>

var body = {
    'app': 1,
    'record': {
        'Text': {
            'value': 'Sample'
        },
        'Number': {
            'value': 1
       }
    }
}
 
kintone.api(kintone.api.url('/k/v1/record', true), 'POST', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Adds 1 record to an App.</td>
</tr>

<tr>
<td>ka-record-add-records</td>
<td>
<pre>

var body = {
    "app": 1,
    "records": [
        {
            "Text": {
                "value": 'Sample001'
            },
            "Number": {
                "value": 1
            }
        },
        {
            "Text": {
                "value": 'Sample002'
            },
            "Number": {
                "value": 2
            }
        }
    ]
}
 
kintone.api(kintone.api.url('/k/v1/records', true), 'POST', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Adds multiple records to an App.</td>
</tr>

<tr>
<td>ka-record-update-record</td>
<td>
<pre>
var body = {
    "app": 1,
    "id": 1,
    "record": {
        "Text": {
            "value": "ABC"
        }
    }
};
   
kintone.api(kintone.api.url('/k/v1/record', true), 'PUT', body, function(resp) {
   // success
    console.log(resp);
}, function(error) {
     // error
    console.log(error);
});
</pre>
</td>
<td>Updates details of 1 record in an App by specifying its record number, or a different unique key.</td>
</tr>

<tr>
<td>ka-record-update-records</td>
<td>
<pre>
var body = {
    "app": 1,
    "records": [
        {
            "id": 1,
            "record": {
                "Text": {
                    "value": "Silver plates"
                }
            }
        },
        {
            "id": 2,
            "record": {
                "Text": {
                    "value": "The quick brown fox."
                }
            }
        }
    ]
};
   
kintone.api(kintone.api.url('/k/v1/records', true), 'PUT', body, function(resp) {
   // success
    console.log(resp);
}, function(error) {
     // error
    console.log(error);
});
</pre>
</td>
<td>Updates details of multiple records in an App, by specifying their record numbers, or their unique keys.</td>
</tr>

<tr>
<td>ka-record-delete-records</td>
<td>
<pre>
var body = {
    'app': 1,
    'ids': [100,80],
    'revisions': [1,4]
}
 
kintone.api(kintone.api.url('/k/v1/records', true), 'DELETE', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Deletes multiple records in an app.</td>
</tr>

<tr>
<td>ka-record-get-cursor</td>
<td>
<pre>
var body = {
  'id': '9a9716fe-1394-4677-a1c7-2199a5d28215'
};
kintone.api(kintone.api.url('/k/v1/records/cursor', true), 'GET', body, function(resp) {
  // success
  console.log(resp);
}, function(error) {
  // error
  console.log(error);
});
</pre>
</td>
<td>Retrieves multiple records from an App by specifying the cursor ID.</td>
</tr>

<tr>
<td>ka-record-add-cursor</td>
<td>
<pre>
var body = {
  'app': 1,
  'fields': ['$id', 'Created_by', 'Created_datetime'],
  'query': 'Created_by in (LOGINUSER()) and Created_datetime = TODAY() order by $id asc',
  'size': 500
};
kintone.api(kintone.api.url('/k/v1/records/cursor', true), 'POST', body, function(resp) {
  // success
  console.log(resp);
}, function(error) {
  // error
  console.log(error);
});
</pre>
</td>
<td>Adds a cursor so that large amount of records can be obtained from an App.</td>
</tr>

<tr>
<td>ka-record-delete-cursor</td>
<td>
<pre>
var body = {
  'id': '9a9716fe-1394-4677-a1c7-2199a5d28215'
};
kintone.api(kintone.api.url('/k/v1/records/cursor', true), 'DELETE', body, function(resp) {
  // success
  console.log(resp);
}, function(error) {
  // error
  console.log(error);
});
</pre>
</td>
<td>Deletes a cursor by specifying the cursor ID.</td>
</tr>

<tr>
<td>ka-record-get-comments</td>
<td>
<pre>
var body = {
    'app': 1,
    'record': 1,
    'order': 'desc',
    'offset': 0,
    'limit': 10
}
kintone.api(kintone.api.url('/k/v1/record/comments', true), 'GET', body, function(resp) {
  // success
  console.log(resp);
}, function(error) {
  // error
  console.log(error);
});
</pre>
</td>
<td>Retrieves multiple comments from a record in an app.</td>
</tr>

<tr>
<td>ka-record-add-comment</td>
<td>
<pre>

var body = {
    'app': 43,
    'record': 1,
    'comment': {
            'text': 'This comment is from the Administrator. \nPlease check!',
            'mentions': [
                {
                    'code': 'user16',
                    'type': 'USER'
                },
                {
                    'code': 'Global Sales_1BNZeQ',
                    'type': 'ORGANIZATION'
                },
                {
                    'code': 'APAC Taskforce_DJrvzu',
                    'type': 'GROUP'
                }
            ]
    }
}
kintone.api(kintone.api.url('/k/v1/record/comment', true), 'POST', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
console.log(error);
});
</pre>
</td>
<td>Retrieves multiple comments from a record in an app.</td>
</tr>

<tr>
<td>ka-record-delete-comment</td>
<td>
<pre>
var body = {
    'app': 1,
    'record': 1,
    'comment': 1
}
kintone.api(kintone.api.url('/k/v1/record/comment', true), 'DELETE', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Delete a comment in a record in an app.</td>
</tr>

<tr>
<td>ka-bulk-request</td>
<td>
<pre>
var body = {
    'requests': [
        {
            'method': 'POST',
            'api': '/k/v1/record.json',
            'payload': {
                'app':1690,
                'record': {
                    'Single_line_text': {
                        'value': 'New text'
                    }
                }
            }
        }
    ]
};
 
kintone.api(kintone.api.url('/k/v1/bulkRequest', true), 'POST', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>The Bulk Request API allows multiple API requests to run on multiple kintone apps. </td>
</tr>

<tr>
<td>ka-record-update-status</td>
<td>
<pre>

var body = {
    'app': 4,
    'id': 1,
    'action': 'Submit',
    'assignee': 'user2',
    'revision': 1
}
 
kintone.api(kintone.api.url('/k/v1/record/status', true), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>This API updates the Status of one or multiple records.</td>
</tr>

<tr>
<td>ka-record-update-multi-status</td>
<td>
<pre>
var body = {
    'app': 4,
    'records': [
            {
                    'id': 1,
                    'action': 'Submit',
                    'assignee': 'user2',
                    'revision': 1
            },
            {
                    'id': 2,
                    'action': 'Confirm'
            },
            {
                    'id': 3,
                    'action': 'Decline',
                    'revision': 5
            }
    ]
}
 
kintone.api(kintone.api.url('/k/v1/records/status', true), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>This API updates the Status of multiple records.</td>
</tr>

<tr>
<td>ka-record-update-assignees</td>
<td>
<pre>
var body = {
    'app': 1,
    'id': 1,
    'assignees': ['user2'],
    'revision': 1
}
 
kintone.api(kintone.api.url('/k/v1/record/assignees', true), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Update assignees of a record.</td>
</tr>
</table>