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
<td>kjs-record</td>
<td>
<pre>
const kintoneRecord = new kintone.Record(connection);
</pre>
</td>
<td>The constructor of Record module</td>
</tr>

<tr>
<td>kjs-record-getRecord</td>
<td>
<pre>	
const app = /*{your_app_id}*/;
const id = {your_record_id};
kintoneRecord.getRecord(app, id).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Retrieves details of 1 record from an app.</td>
</tr>

<tr>
<td>kjs-record-getRecords</td>
<td>
<pre>	
const app = /*{your_app_id}*/;
const query = '{your_query_string}';
const fields = [
    '{your_field_code}',
    // another fieldCode
]
const totalCount = /*{your_decide_true_or_false}*/;
kintoneRecord.getRecords(app, query, fields, totalCount).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Retrieves details of multiple records from an app using a query string.</td>
</tr>

<tr>
<td>kjs-record-getAllRecordsByQuery</td>
<td>
<pre>	
const app = '{your_app_id}';
const query = '{your_query_string}';
const fields = [
    '{your_field_code}',
    // another fieldCode
]
const totalCount = '{your_decide_true_or_false}';
kintoneRecord.getAllRecordsByQuery(app, query, fields, totalCount).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIException
  console.log(err.get());
});
</pre>
</td>
<td>Retrieves details of all records from an app using a query string.</td>
</tr>

<tr>
<td>kjs-record-getAllRecordsByCurso</td>
<td>
<pre>
const app = /*{your_app_id}*/;
const record = {
    YourFieldCode: {
        value: 'Value Of YourFieldCode'
    },
    // Another fieldcode here
};
kintoneRecord.addRecord(app, record).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Add one record to an app.</td>
</tr>


<tr>
<td>kjs-record-getAllRecordsByCurso</td>
<td>
<pre>
const app = /*{your_app_id}*/;
const record = {
    YourFieldCode: {
        value: 'Value Of YourFieldCode'
    },
    // Another fieldcode here
};
kintoneRecord.addRecord(app, record).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Add one record to an app.</td>
</tr>


<tr>
<td>kjs-record-getAllRecordsByCursor</td>
<td>
<pre>
const app = /*{your_app_id}*/;
const record = {
    YourFieldCode: {
        value: 'Value Of YourFieldCode'
    },
    // Another fieldcode here
};
kintoneRecord.addRecord(app, record).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Add one record to an app.</td>
</tr>

<tr>
<td>kjs-record-addRecords</td>
<td>
<pre>	
const app = /*{your_app_id}*/;
const record = {
  YourFieldCode: {
    value: 'Value Of YourFieldCode'
  },
  // Another fieldcode here
};
const records = [
  record
  // another record
];
kintoneRecord.addRecords(app, records).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Add multiple records to an app.</td>
</tr>

<tr>
<td>kjs-record-addAllRecords</td>
<td>
<pre>
const app = '{your_app_id}';
const record = {
  YourFieldCode: {
    value: 'Value Of YourFieldCode'
  },
  // Another fieldcode here
};
const records = [
  record
  // another record
];
kintoneRecord.addAllRecords(app, records).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  console.log(err)
});
</pre>
</td>
<td>Add multiple records to an app.</td>
</tr>

<tr>
<td>kjs-record-updateRecord</td>
<td>
<pre>
const app = /*{your_app_id}*/;
const id = /*{your_record_id}*/;
const record = {
  YourFieldCode: {
    value: 'Value Of YourFieldCode'
  },
  // Another fieldcode here
};
const revision = /*{revision_of_record}*/;
kintoneRecord.updateRecordByID(app, id, record, revision).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Updates details of 1 record in an app by specifying its record number.</td>
</tr>

<tr>
<td>kjs-record-updateRecordByUpdateKey</td>
<td>
<pre>
const app = /*{your_app_id}*/;
const updateKey = {
  field: '{your_fieldcode}',
  value: '{your_fieldcode_value}'
};
const record = {
  YourFieldCode: {
    value: 'Value Of YourFieldCode'
  },
  // Another fieldcode here
};
const revision = /*{revision_of_record}*/;
kintoneRecord.updateRecordByUpdateKey(app, updateKey, record, revision).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Updates details of 1 record in an app by unique key.</td>
</tr>

<tr>
<td>kjs-record-updateRecords</td>
<td>
<pre>
const app = /*{your_app_id}*/;
const record = {
    YourFieldCode: {
        value: 'Value Of YourFieldCode'
    },
    // Another fieldcode here
};
const recordUpdate = {
    id: /*{your_record_id}*/, // Optional. Required, if updateKey will not be specified.
    updateKey: { // Optional. Required, if id will not be specified.
        field: '{your_field_code}',
        value: '{your_field_code_value}'
    },
    record: record,
    revision: /*{record_revision_number}*/ // Optional
};
const recordsUpdate = [
    recordUpdate,
    // Another recordUpdate
]
kintoneRecord.updateRecords(app, recordsUpdate).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Updates details of multiple records in an app, by specifying their record number, or a different unique key.</td>
</tr>

<tr>
<td>kjs-record-updateAllRecords</td>
<td>
<pre>
const app = /*{your_app_id}*/;
const record = {
    YourFieldCode: {
        value: 'Value Of YourFieldCode'
    },
    // Another fieldcode here
};
const recordUpdate = {
    id: /*{your_record_id}*/, // Optional. Required, if updateKey will not be specified.
    updateKey: { // Optional. Required, if id will not be specified.
        field: '{your_field_code}',
        value: '{your_field_code_value}'
    },
    record: record,
    revision: /*{record_revision_number}*/ // Optional
};
const recordsUpdate = [
    recordUpdate,
    // Another recordUpdate
]
kintoneRecord.updateAllRecords(app, recordsUpdate).then((rsp) => {
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
const app = /*{your_app_id}*/;
const ids = [/*your_record_id*/]
kintoneRecord.deleteRecords(app, ids).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Deletes multiple records in an app.</td>
</tr>

<tr>
<td>kjs-record-deleteRecordsWithRevision</td>
<td>
<pre>
const app = 'your_app_id';
const query = 'your_query_string';
kintoneRecord.deleteAllRecordsByQuery(app, query).then((rsp) => {
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
const app = /*{your_app_id}*/;
const updateKey = {
  field: '{your_fieldcode}',
  value: '{your_fieldcode_value}'
};
const record = {
  YourFieldCode: {
    value: 'Value Of YourFieldCode'
  },
  // Another fieldcode here
};
const revision = 'revision_of_record';
kintoneRecord.upsertRecord(app, updateKey, record, revision).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Insert or update a record to kintone app. Insert the record if the updateKey doesn't exists and update the record if the updateKey exists.</td>
</tr>

<tr>
<td>kjs-record-upsertRecords</td>
<td>
<pre>	
const app = 'your_app_id';
  const records = [
    {
      updateKey: {
        field: 'your_fieldcode',
        value: 'your_fieldcode_value_1'
      },
      record: {
        YourFieldCode: {
          value: 'Value Of YourFieldCode 1'
        },
      }
    },
    {
      updateKey: {
        field: 'your_fieldcode',
        value: 'your_fieldcode_value_2'
      },
      record: {
        YourFieldCode: {
          value: 'Value Of YourFieldCode 2'
        },
      }
    },
    {
      updateKey: {
        field: 'your_fieldcode',
        value: 'your_fieldcode_value_3'
      },
      record: {
        YourFieldCode: {
          value: 'Value Of YourFieldCode 3'
        },
      }
    }
  ];
  recordModule.upsertRecords(app, records).then((resp) => {
    console.log(resp);
  }).ca
</pre>
</td>
<td>Insert or update up to 1500 records to kintone app. If the records are over 1500, It is thrown Error. Insert the records if the updateKey doesn't exists and update the records if the updateKey exists.</td>
</tr>

<tr>
<td>kjs-record-updateRecordAssignees</td>
<td>
<pre>
const app = /*{your_app_id}*/;
const id = /*{your_record_id}*/;
const assignees = [/*your_assignee(s)*/];
const revision = /*{revision_of_record}*/;
 
kintoneRecord.updateRecordAssignees(app, id, assignees, revision).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Update assignees of a record.</td>
</tr>

<tr>
<td>kjs-record-updateRecordStatus</td>
<td>
<pre>
const app = /*{your_app_id}*/;
const id = /*{your_record_id}*/;
const action = /*{your_action_name}*/;
const assignee = '/*your_assignee(s)*/';
const revision = /*{revision_of_record}*/;
 
kintoneRecord.updateRecordStatus(app, id, action, assignee, revision).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Updates the Status of a record of an app.</td>
</tr>

<tr>
<td>kjs-recordupdateRecordsStatus</td>
<td>
<pre>
const app = /*{your_app_id}*/;
const recordStatusUpdateItem = {
    id: /*your_record_id*/,
    action: '/*your_action_name*/',
    assignee: '/*your_assignee*/',
    revision: /*your_record_revision*/
}
const records = [
    recordStatusUpdateItem,
    /*another data like recordStatusUpdateItem*/
];
kintoneRecord.updateRecordsStatus(app, records).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Updates the Status of multiple records of an app.</td>
</tr>

<tr>
<td>kjs-record-getComments</td>
<td>
<pre>
const app = /*{your_app_id}*/;
const id = /*{your_record_id}*/;
const order = /*{your_order_type}*/; // asc or desc
const offset = /*{your_offset_number}*/;
const limit = /*{your_limit number}*/;
kintoneRecord.getComments(app, id, order, offset, limit).then((rsp) => {
  console.log(rsp);
}).catch((err) => {
  // This SDK return err with KintoneAPIExeption
  console.log(err.get());
});
</pre>
</td>
<td>Get comments of the record</td>
</tr>

<tr>
<td>kjs-record-addComment</td>
<td>
<pre>
const app = /*{your_app_id}*/;
const record = /*{your_record_id}*/;
const comment = {
  text: '/*your_comment_content*/',
  mentions: [
    {
      code: '/*your_member_code*/',
      type: '/*your_member_type*/' // either `USER` or `GROUP` or `ORGANIZATION`
    },
    // another mention here
  ]
};
kintoneRecord.addComment(app, record, comment).then((rsp) => {
    console.log(rsp);
  }).catch((err) => {
    // This SDK return err with KintoneAPIExeption
    console.log(err.get());
  });
</pre>
</td>
<td>Add the record comment</td>
</tr>

<tr>
<td>kjs-record-deleteComment</td>
<td>
<pre>
const app = /*{your_app_id}*/;
const record = /*{your_record_id}*/;
const comment = /*{your_comment_id}*/;
kintoneRecord.deleteComment(app, record, comment).then((rsp) => {
    console.log(rsp);
  }).catch((err) => {
    // This SDK return err with KintoneAPIExeption
    console.log(err.get());
  });
</pre>
</td>
<td>Delete the comment</td>
</tr>
</table>