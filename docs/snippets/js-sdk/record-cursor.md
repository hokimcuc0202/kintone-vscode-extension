# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kjs-cursor</td>
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
var kintoneRC = new kintoneJSSDK.RecordCursor({connection});
 
// without connection, module will use session authentication of kintone
var kintoneRC = new kintoneJSSDK.RecordCursor();
</pre>
</td>
<td>The constructor of record cursor</td>
</tr>

<tr>
<td>kjs-cursor-createCursor</td>
<td>
<pre>
var rcOption = {
    app: YOUR_APP_ID,
    fields: ['YOUR_FIELD_CODE'],
    query: 'YOUR_QUERY',
    size: YOUR_SIZE
}
 
kintoneRC.createCursor(rcOption).then(function(creatCursorResponse){
    var myCursor = creatCursorResponse;
    console.log('Cursor ID: ' + myCursor.id );
    console.log('Total Count: ' + myCursor.totalCount );
}).catch((err) => {
    // This SDK return err with KintoneAPIException
    console.log(err);
});
</pre>
</td>
<td>Create a cursor.</td>
</tr>

<tr>
<td>kjs-cursor-getRecords</td>
<td>
<pre>
var rcOption = {
    app: YOUR_APP_ID,
    fields: ['YOUR_FIELD_CODE'],
    query: 'YOUR_QUERY',
    size: YOUR_SIZE
}
 
kintoneRC.createCursor(rcOption).then(function(creatCursorResponse){
    var myCursor = creatCursorResponse;
    return kintoneRC.getRecords({id: myCursor.id})
}).then(function (getRecordsResponse) {
    console.log('Records result: ');
    console.log(getRecordsResponse);
}).catch((err) => {
    // This SDK return err with KintoneAPIException
    console.log(err);
});
</pre>
</td>
<td>Get one block of records.</td>
</tr>

<tr>
<td>kjs-cursor-getAllRecords</td>
<td>
<pre>
var rcOption = {
    app: YOUR_APP_ID,
    fields: ['YOUR_FIELD_CODE'],
    query: 'YOUR_QUERY',
    size: YOUR_SIZE
}
 
kintoneRC.createCursor(rcOption).then(function(creatCursorResponse){
    var myCursor = creatCursorResponse;
    return kintoneRC.getAllRecords({id: myCursor.id})
}).then(function (getAllRecordsResponse) {
    console.log('All records result: ');
    console.log(getAllRecordsResponse);
}).catch((err) => {
    // This SDK return err with KintoneAPIException
    console.log(err);
});
</pre>
</td>
<td>Get all records</td>
</tr>

<tr>
<td>kjs-cursor-deleteCursor</td>
<td>
<pre>
var rcOption = {
    app: YOUR_APP_ID,
    fields: ['YOUR_FIELD_CODE'],
    query: 'YOUR_QUERY',
    size: YOUR_SIZE
}
 
kintoneRC.createCursor(rcOption).then(function(creatCursorResponse){
    var myCursor = creatCursorResponse;
    return kintoneRC.deleteCursor({id: myCursor.id})
}).then(function (getAllRecordsResponse) {
    console.log('Cursor Deleted');
}).catch((err) => {
    // This SDK return err with KintoneAPIException
    console.log(err);
});
</pre>
</td>
<td>Delete a cursor</td>
</tr>
</table>