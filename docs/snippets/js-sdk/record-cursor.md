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
const recordCursor= new kintone.RecordCursor(kintoneConn);
</pre>
</td>
<td>The constructor of record cursor</td>
</tr>

<tr>
<td>kjs-cursor-createCursor</td>
<td>
<pre>
const option = {
       app: appID,
       fields: [],
       query: '',
       size: 2
}
 
recordCursor.createCursor(option ).then(function(creatCursorResponse){
     const myCursor = creatCursorResponse;
     console.log('Cursor ID: ' + myCursor.id );
     console.log('Total Count: ' + myCursor.totalCount );
})
</pre>
</td>
<td>Create a cursor.</td>
</tr>

<tr>
<td>kjs-cursor-getRecords</td>
<td>
<pre>
const cursorID = 'your_cursorID'
recordCursor.getRecords(cursorID)
        .then(function(getRecordsResponse){
            console.log('RecordCursor result: ');
            console.log(getRecordsResponse);
        })
</pre>
</td>
<td>Get one block of records.</td>
</tr>

<tr>
<td>kjs-cursor-getAllRecords</td>
<td>
<pre>
const cursorID = 'your_cursorID'
recordCursor.getAllRecords(cursorID)
        .then(function(getRecordsResponse){
            console.log('RecordCursor result: ');
            console.log(getRecordsResponse);
        })
</pre>
</td>
<td>Get all records</td>
</tr>

<tr>
<td>kjs-cursor-deleteCursor</td>
<td>
<pre>
const cursorID = 'your_cursorID'
recordCursor.deleteCursor(cursorID)
        .then(function(getRecordsResponse){
            console.log('RecordCursor result: ');
            console.log(getRecordsResponse);
        })
</pre>
</td>
<td>Delete a cursor</td>
</tr>
</table>