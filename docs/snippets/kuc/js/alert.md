# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-alert</td>
<td>
<pre>
var alert = new kintoneUIComponent.Alert({text: 'Network error', type: 'error'});
</pre>
</td>
<td>Initialize a KUC Alert</td>
</tr>

<tr>
<td>kuc-alert-set-render</td>
<td>
<pre>
var alert = new kintoneUIComponent.Alert({text: 'Network error', type: 'error'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(alert.render());
</pre>
</td>
<td>Get dom element of component.</td>
</tr>

<tr>
<td>kuc-alert-set-text</td>
<td>
<pre>
var alert = new kintoneUIComponent.Alert({text: 'Network error', type: 'error'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(alert.render());
alert.setText('Network error');
</pre>
</td>
<td>Set the content of alert.</td>
</tr>

<tr>
<td>kuc-alert-set-type</td>
<td>
<pre>
var alert = new kintoneUIComponent.Alert({text: 'Network error', type: 'error'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(alert.render());
alert.setType('success');
</pre>
</td>
<td>Set the type of alert.</td>
</tr>

<tr>
<td>kuc-alert-on</td>
<td>
<pre>
var alert = new kintoneUIComponent.Alert({text: 'Network error', type: 'error'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(alert.render());
alert.on('click', function(event) {
    console.log('on click');
});
</pre>
</td>
<td>The callBack function will be execute after user click the alert.</td>
</tr>

<tr>
<td>kuc-alert-show</td>
<td>
<pre>
var alert = new kintoneUIComponent.Alert({text: 'Network error', type: 'error'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(alert.render());
alert.show();
</pre>
</td>
<td>Display the Alert.</td>
</tr>

<tr>
<td>kuc-alert-hide</td>
<td>
<pre>
var alert = new kintoneUIComponent.Alert({text: 'Network error', type: 'error'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(alert.render());
alert.hide();
</pre>
</td>
<td>Hide the Alert.</td>
</tr>

<tr>
<td>kuc-alert-disable</td>
<td>
<pre>
var alert = new kintoneUIComponent.Alert({text: 'Network error', type: 'error'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(alert.render());
alert.disable();
</pre>
</td>
<td>Disable the Alert.</td>
</tr>

<tr>
<td>kuc-alert-enable</td>
<td>
<pre>
var alert = new kintoneUIComponent.Alert({text: 'Network error', type: 'error'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(alert.render());
alert.enable();
</pre>
</td>
<td>Enable the Alert.</td>
</tr>

</table>