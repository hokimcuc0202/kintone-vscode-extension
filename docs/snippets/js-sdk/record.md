# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kjs-record</td>
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
var kintoneRecord = new kintoneJSSDK.Record({connection});
 
// without connection, module will use session authentication of kintone
var kintoneRecord = new kintoneJSSDK.Record();
</pre>
</td>
<td>The constructor of Record module</td>
</tr>

<tr>
<td>kjs-record-getRecord</td>
<td>
<pre>	
var app = YOUR_APP_ID;
var id = YOUR_RECORD_ID;
kintoneRecord.getRecord({app, id}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Retrieves details of 1 record from an app.</td>
</tr>

<tr>
<td>kjs-record-getRecords</td>
<td>
<pre>	
var app = YOUR_APP_ID;
var query = 'YOUR_QUERY_STRING';
var fields = [
    'YOUR_FIELD_CODE',
    // another fieldCode
]
var totalCount = 'YOUR_DECIDE_TRUE_OR_FALSE';
kintoneRecord.getRecords({app, query, fields, totalCount}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Retrieves details of multiple records from an app using a query string.</td>
</tr>

<tr>
<td>kjs-record-getAllRecordsByQuery</td>
<td>
<pre>	
var app = YOUR_APP_ID;
var query = 'YOUR_QUERY_STRING';
var fields = [
    'YOUR_FIELD_CODE',
    // another fieldCode
]
var totalCount = 'YOUR_DECIDE_TRUE_OR_FALSE';
var seek = 'YOUR_DECIDE_TRUE_OR_FALSE';
kintoneRecord.getAllRecordsByQuery({app, query, fields, totalCount, seek}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Retrieves details of all records from an app using a query string.</td>
</tr>

<tr>
<td>kjs-record-getAllRecordsByCursor</td>
<td>
<pre>
const rcOption = {
  app: {your_app_id},
  fields: [
    '{your_field_code}',
    // another fieldCode
  ],
  query: '{your_query_string}'
};
 
kintoneRecord.getAllRecordsByCursor(rcOption).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err.get());
});
</pre>
</td>
<td>Retrieves details of all records from an app using a cursor.</td>
</tr>

<tr>
<td>kjs-record-addRecord</td>
<td>
<pre>
var app = YOUR_APP_ID;
var record = {
  YOUR_FIELD_CODE: {
    value: 'VALUE_OF_YOUR_FIELD_CODE'
  },
  // Another fieldcode here
};
kintoneRecord.addRecord({app, record}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Add one record to an app.</td>
</tr>

<tr>
<td>kjs-record-addRecords</td>
<td>
<pre>		
var app = YOUR_APP_ID;
var record = {
    YOUR_FIELD_CODE: {
        value: 'VALUE_OF_YOUR_FIELD_CODE'
    },
    // Another fieldcode here
};
var records = [
    record,
    // another record
];
kintoneRecord.addRecords({app, records}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Add multiple records to an app.</td>
</tr>

<tr>
<td>kjs-record-addAllRecords</td>
<td>
<pre>	
var app = YOUR_APP_ID;
var record = {
    YOUR_FIELD_CODE: {
        value: 'VALUE_OF_YOUR_FIELD_CODE'
    },
    // Another fieldcode here
};
var records = [
    record,
    // another record
];
kintoneRecord.addAllRecords({app, records}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  console.log(err)
});
</pre>
</td>
<td>Add multiple records to an app.</td>
</tr>

<tr>
<td>kjs-record-updateRecordByID</td>
<td>
<pre>
var app = YOUR_APP_ID;
var id = YOUR_RECORD_ID;
var record = {
    YOUR_FIELD_CODE: {
        value: 'VALUE_OF_YOUR_FIELD_CODE'
    },
    // Another fieldcode here
};
var revision = REVISION_OF_RECORD;
kintoneRecord.updateRecordByID({app, id, record, revision}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Updates details of 1 record in an app by specifying its record number.</td>
</tr>

<tr>
<td>kjs-record-updateRecordByUpdateKey</td>
<td>
<pre>
var app = YOUR_APP_ID;
var updateKey = {
  field: 'YOUR_FIELD_CODE',
  value: 'YOUR_FIELD_CODE_VALUE'
};
var record = {
  YOUR_FIELD_CODE: {
    value: 'VALUE_OF_YOUR_FIELD_CODE'
  },
  // Another fieldcode here
};
var revision = REVISION_OF_RECORD;
kintoneRecord.updateRecordByUpdateKey({app, updateKey, record, revision}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Updates details of 1 record in an app by unique key.</td>
</tr>

<tr>
<td>kjs-record-updateRecords</td>
<td>
<pre>
var app = YOUR_APP_ID;
var record = {
  YOUR_FIELD_CODE: {
    value: 'VALUE_OF_YOUR_FIELD_CODE'
  },
  // Another fieldcode here
};
 
// This object can not have both "id" and "updateKey" keys at the same time.
var recordUpdate = {
  // Required, if updateKey will not be specified.
  id: YOUR_RECORD_ID,
  // Required, if id will not be specified.
  updateKey: {
    field: 'YOUR_FIELD_CODE',
    value: 'YOUR_FIELD_CODE_VALUE'
  },
  record: record,
  revision: RECORD_REVISION_NUMBER
};
var records= [
  recordUpdate,
  // Another recordUpdate
]
kintoneRecord.updateRecords({app, records}).then((rsp) => {
    console.log(rsp);
  }).catch((err) => {
    // This SDK return err with KintoneAPIException
    console.log(err);
  });
</pre>
</td>
<td>Updates details of multiple records in an app, by specifying their record number, or a different unique key.</td>
</tr>

<tr>
<td>kjs-record-updateAllRecords</td>
<td>
<pre>
var app = YOUR_APP_ID;
var record = {
  YOUR_FIELD_CODE: {
    value: 'VALUE_OF_YOUR_FIELD_CODE'
  },
  // Another fieldcode here
};
 
// This object can not have both "id" and "updateKey" keys at the same time.
var recordUpdate = {
  // Required, if updateKey will not be specified.
  id: YOUR_RECORD_ID,
  // Required, if id will not be specified.
  updateKey: {
    field: 'YOUR_FIELD_CODE',
    value: 'YOUR_FIELD_CODE_VALUE'
  },
  record: record,
  revision: RECORD_REVISION_NUMBER
};
var records = [
  recordUpdate,
  // Another recordUpdate
]
kintoneRecord.updateAllRecords({app, records}).then((rsp) => {
    console.log(rsp);
  }).catch((err) => {
  console.log(err)
  });
</pre>
</td>
<td>Updates details of multiple records in an app, by specifying their record number, or a different unique key.</td>
</tr>

<tr>
<td>kjs-record-deleteRecords</td>
<td>
<pre>
var app = YOUR_APP_ID;
var ids = [YOUR_RECORD_ID]
kintoneRecord.deleteRecords({app, ids}).then((rsp) => {
   console.log(rsp);
}).catch((err) => {
   // This SDK return err with KintoneAPIException
   console.log(err);
});
</pre>
</td>
<td>Deletes multiple records in an app.</td>
</tr>

<tr>
<td>kjs-record-deleteRecordsWithRevision</td>
<td>
<pre>
var app = YOUR_APP_ID;
var idsWithRevision = {
  YOUR_RECORD_ID: REVISION_OF_RECORD
}
kintoneRecord.deleteRecordsWithRevision({app, idsWithRevision}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Deletes all records in an app by query string</td>
</tr>

<tr>
<td>kjs-record-deleteAllRecordsByQuery</td>
<td>
<pre>
var app = YOUR_APP_ID;
 var query = 'YOUR_QUERY_STRING';
 kintoneRecord.deleteAllRecordsByQuery({app, query}).then((rsp) => {
     console.log(rsp);
 })
 .catch((err) => {
   console.log(err)
 });
</pre>
</td>
<td>Deletes all records in an app by query string</td>
</tr>

<tr>
<td>kjs-record-upsertRecord</td>
<td>
<pre>		
var app = YOUR_APP_ID;
var updateKey = {
  field: 'YOUR_FIELD_CODE',
  value: 'YOUR_FIELD_CODE_VALUE'
};
var record = {
  YOUR_FIELD_CODE: {
    value: 'VALUE_OF_YOUR_FIELD_CODE'
  },
  // Another fieldcode here
};
var revision = REVISION_OF_RECORD;
kintoneRecord.upsertRecord({app, updateKey, record, revision}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Insert or update a record to kintone app. Insert the record if the updateKey doesn't exists and update the record if the updateKey exists.</td>
</tr>

<tr>
<td>kjs-record-upsertRecords</td>
<td>
<pre>	
var app = YOUR_APP_ID;
var records = [
  {
    updateKey: {
      field: 'YOUR_FIELD_CODE',
      value: 'YOUR_FIELD_CODE_VALUE_1'
    },
    record: {
      YOUR_FIELD_CODE: {
        value: 'VALUE_OF_YOUR_FIELD_CODE 1'
      },
    }
  }
];
kintoneRecord.upsertRecords({app, records}).then((resp) => {
  console.log(resp);
}).catch((err) => {
  console.log(err);
});
</pre>
</td>
<td>Insert or update up to 1500 records to kintone app. If the records are over 1500, It is thrown Error. Insert the records if the updateKey doesn't exists and update the records if the updateKey exists.</td>
</tr>

<tr>
<td>kjs-record-updateRecordAssignees</td>
<td>
<pre>
var app = YOUR_APP_ID;
var id = YOUR_RECORD_ID;
var assignees = ['YOUR_ASSIGNEE'];
var revision = REVISION_OF_RECORD;
 
kintoneRecord.updateRecordAssignees({app, id, assignees, revision}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Update assignees of a record.</td>
</tr>

<tr>
<td>kjs-record-updateRecordStatus</td>
<td>
<pre>	
var app = YOUR_APP_ID;
var id = YOUR_RECORD_ID;
var action = 'YOUR_ACTION_NAME';
var assignee = 'YOUR_ASSIGNEE';
var revision = REVISION_OF_RECORD;
 
kintoneRecord.updateRecordStatus({app, id, action, assignee, revision}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Updates the Status of a record of an app.</td>
</tr>

<tr>
<td>kjs-recordupdateRecordsStatus</td>
<td>
<pre>
var app = YOUR_APP_ID;
var recordStatusUpdateItem = {
  id: YOUR_RECORD_ID,
  action: 'YOUR_ACTION_NAME',
  assignee: 'YOUR_ASSIGNEE',
  revision: 'YOUR_RECORD_REVISION'
}
var records = [
  recordStatusUpdateItem,
  // another data like recordStatusUpdateItem
];
kintoneRecord.updateRecordsStatus({app, records}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Updates the Status of multiple records of an app.</td>
</tr>

<tr>
<td>kjs-record-getComments</td>
<td>
<pre>
var app = YOUR_APP_ID;
var record = YOUR_RECORD_ID;
var order = 'YOUR_ORDER_TYPE'; // asc or desc
var offset = YOUR_OFFSET_NUMBER;
var limit = YOUR_LIMIT_NUMBER;
kintoneRecord.getComments({app, record, order, offset, limit}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Get comments of the record</td>
</tr>

<tr>
<td>kjs-record-addComment</td>
<td>
<pre>	
var app = YOUR_APP_ID;
var record = YOUR_RECORD_ID;
var comment = {
  text: 'YOUR_COMMENT_CONTENT',
  mentions: [
    {
      code: 'YOUR_MEMBER_CODE',
      type: 'YOUR_MEMBER_TYPE' // either `USER` or `GROUP` or `ORGANIZATION`
    },
    // another mention here
  ]
};
kintoneRecord.addComment({app, record, comment}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Add the record comment</td>
</tr>

<tr>
<td>kjs-record-deleteComment</td>
<td>
<pre>
var app = YOUR_APP_ID;
var record = YOUR_RECORD_ID;
var comment = YOUR_COMMENT_ID;
kintoneRecord.deleteComment({app, record, comment}).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err);
});
</pre>
</td>
<td>Delete the comment</td>
</tr>
</table>