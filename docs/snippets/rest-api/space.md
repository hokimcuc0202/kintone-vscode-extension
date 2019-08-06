# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>ka-space-get-space</td>
<td>
<pre>
var body = {
    "id": 1
};
 
kintone.api(kintone.api.url('/k/v1/space', true), 'GET', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Gets information of a Space.</td>
</tr>

<tr>
<td>ka-space-add-space</td>
<td>
<pre>
	
var body = {
    "id": 1001,
    "name": "Sample Space Name",
    "members": [
        {
            "entity": {
                "type": "USER",
                "code": "user1"
            },
            "isAdmin": true
        },
        {
            "entity": {
                "type": "GROUP",
                "code": "group1"
            },
            "isAdmin": false
        },
        {
            "entity": {
                "type": "ORGANIZATION",
                "code": "org1"
            },
            "isAdmin": false,
            "includeSubs": true
        }
    ]
};
 
kintone.api(kintone.api.url('/k/v1/template/space', true), 'POST', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Creates a Space from a Space template</td>
</tr>

<tr>
<td>ka-space-update-space</td>
<td>
<pre>
var body = {
    "id": 1001,
    "body": "<b>Sample Space Description</b>"
};
 
kintone.api(kintone.api.url('/k/v1/space/body', true), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Updates the body of a Space</td>
</tr>

<tr>
<td>ka-space-delete-space</td>
<td>
<pre>
var body = {
    "id": 1001
};
 
kintone.api(kintone.api.url('/k/v1/space', true), 'DELETE', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Deletes a Space</td>
</tr>

<tr>
<td>ka-space-get-spaceMembers</td>
<td>
<pre>
var body = {
    "id": 1
};
 
kintone.api(kintone.api.url('/k/v1/space/members', true), 'GET', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Gets the list of Space Members of a Space.</td>
</tr>

<tr>
<td>ka-space-update-spaceMembers</td>
<td>
<pre>
var body = {
    "id": "1001",
    "members": [
        {
            "entity": {
                "type": "USER",
                "code": "user1"
            },
            "isAdmin": true
        },
        {
            "entity": {
                "type": "GROUP",
                "code": "group1"
            },
            "isAdmin": false
        },
        {
            "entity": {
                "type": "ORGANIZATION",
                "code": "org1"
            },
            "isAdmin": false,
            "includeSubs": true
        }
    ]
};
 
kintone.api(kintone.api.url('/k/v1/space/members', true), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Updates the Members of a Space</td>
</tr>

<tr>
<td>ka-space-add-threadComment</td>
<td>
<pre>
var body = {
    "space": 1001,
    "thread": 1001,
    "comment": {
        "text": "This is the Golden Gate Bridge in San Francisco. \nIsn't it gorgeous?",
        "mentions": [
            {
                "code": "john",
                "type": "USER"
            },
            {
                "code": "HR_EBbG2z",
                "type": "ORGANIZATION"
            },
            {
                "code": "Travel Club_9mhZNJ",
                "type": "GROUP"
            }
        ],
        "files": [
            {
                "fileKey": "a8c5360e-e919-4ac6-a300-b24fbc9ee1ec",
                "width": 400
            }
        ]
    }
};
 
kintone.api(kintone.api.url('/k/v1/space/thread/comment', true), 'POST', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Adds a comment to a Thread of a Space.</td>
</tr>

<tr>
<td>ka-space-update-thread</td>
<td>
<pre>
var body = {
    "id": 1001,
    "name": "Thread Name",
    "body": "<b>Thread Body</b>"
};
 
kintone.api(kintone.api.url('/k/v1/space/thread', true), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Updates a Thread of a Space.</td>
</tr>

<tr>
<td>ka-space-add-guests</td>
<td>
<pre>

var body = {
    "guests": [
        {
            "code": "guest1@example.com",
            "password": "password",
            "timezone": "America/Los_Angeles",
            "locale": "en",
            "image": "78a586f2-e73e-4a70-bec2-43976a60746e",
            "name": "John Doe",
            "company": "Company Name",
            "division": "Sales",
            "phone": "999-456-7890",
            "callto": "skypecallto"
        }
    ]
};
 
kintone.api(kintone.api.url('/k/v1/guests', true), 'POST', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Adds Guest users to kintone.</td>
</tr>

<tr>
<td>ka-space-update-guestMembers</td>
<td>
<pre>
var body = {
    "id": 1001,
    "guests": [
        "guest1@example.com"
    ]
};
 
kintone.api(kintone.api.url('/k/guest/{guestspaceId}/v1/space/guests', false), 'PUT', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Updates the Guest Members of a Space.</td>
</tr>

<tr>
<td>ka-space-delete-guests</td>
<td>
<pre>
var body = {
    "guests": [
            "guest1@example.com"
    ]
};
 
kintone.api(kintone.api.url('/k/v1/guests', true), 'DELETE', body, function(resp) {
    // success
    console.log(resp);
}, function(error) {
    // error
    console.log(error);
});
</pre>
</td>
<td>Deletes a Guest user from kintone.</td>
</tr>
</table>