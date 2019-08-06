# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-label</td>
<td>
<pre>
var label = new kintoneUIComponent.Label({
    text: 'Name',
    textColor: '#e74c3c',
    backgroundColor: 'yellow',
    isRequired: true
});
</pre>
</td>
<td>Constructor</td>
</tr>

<tr>
<td>kuc-label-render</td>
<td>
<pre>
var label = new kintoneUIComponent.Label({text: 'label'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(label.render());
</pre>
</td>
<td>Get dom element of component.</td>
</tr>

<tr>
<td>kuc-label-set-text</td>
<td>
<pre>
var label = new kintoneUIComponent.Label({text: 'label'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(label.render());
label.setText('Name');
</pre>
</td>
<td>Set the value of text field.</td>
</tr>

<tr>
<td>kuc-label-text-color</td>
<td>
<pre>
var label = new kintoneUIComponent.Label({text: 'label'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(label.render());
label.setTextColor('#e74c3c');
</pre>
</td>
<td>Set color of caption.</td>
</tr>

<tr>
<td>kuc-label-background-color</td>
<td>
<pre>
var label = new kintoneUIComponent.Label({text: 'label'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(label.render());
label.setBackgroundColor('#e74c3c');
</pre>
</td>
<td>Set color of background.</td>
</tr>

<tr>
<td>kuc-label-required</td>
<td>
<pre>
var label = new kintoneUIComponent.Label({text: 'label'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(label.render());
label.setRequired(true);
</pre>
</td>
<td>Set the required for the label.</td>
</tr>

<tr>
<td>kuc-label-on</td>
<td>
<pre>
var label = new kintoneUIComponent.Label({text: 'label'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(label.render());
label.on('click', function(event) {
    console.log('on click');
});
</pre>
</td>
<td>Register callback for click event</td>
</tr>

<tr>
<td>kuc-label-show</td>
<td>
<pre>
var label = new kintoneUIComponent.Label({text: 'label'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(label.render());
label.show();
</pre>
</td>
<td>Display the Label.</td>
</tr>

<tr>
<td>kuc-label-hide</td>
<td>
<pre>
var label = new kintoneUIComponent.Label({text: 'label'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(label.render());
label.hide();
</pre>
</td>
<td>Hide the Label.</td>
</tr>

<tr>
<td>kuc-label-disable</td>
<td>
<pre>
var label = new kintoneUIComponent.Label({text: 'label'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(label.render());
label.disable();
</pre>
</td>
<td>Disabled the Label.</td>
</tr>

<tr>
<td>kuc-label-enable</td>
<td>
<pre>
var label = new kintoneUIComponent.Label({text: 'label'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(label.render());
label.enable();
</pre>
</td>
<td>Enabled the Label.</td>
</tr>
</table>