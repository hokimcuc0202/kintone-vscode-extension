# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-notify-popup</td>
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
<td>kuc-notify-popup-render</td>
<td>
<pre>
var notifyPopup = new kintoneUIComponent.NotifyPopup({
    text: 'Submit sucessffully',
    type: 'success'
});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(notifyPopup.render());
</pre>
</td>
<td>Get dom element of component.</td>
</tr>

<tr>
<td>kuc-notify-popup-set-text</td>
<td>
<pre>
var notifyPopup = new kintoneUIComponent.NotifyPopup({
    text: 'Submit sucessffully',
    type: 'success'
});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(notifyPopup.render());
 
notifyPopup.setText('Submit failed');
</pre>
</td>
<td>Setting the displayed text on popup.</td>
</tr>

<tr>
<td>kuc-notify-popup-kuc-notify-popup-set-type</td>
<td>
<pre>
var notifyPopup = new kintoneUIComponent.NotifyPopup({
    text: 'Submit sucessffully',
    type: 'success'
});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(notifyPopup.render());
 
notifyPopup.setType('success');
</pre>
</td>
<td>Setting type for popup.</td>
</tr>

<tr>
<td>kuc-notify-popup-on</td>
<td>
<pre>
var notifyPopup = new kintoneUIComponent.NotifyPopup({
    text: 'Submit sucessffully',
    type: 'success'
});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(notifyPopup.render());
 
notifyPopup.on('click', function(event) {
    console.log('on click');
});
</pre>
</td>
<td>Register callback for click event</td>
</tr>

<tr>
<td>kuc-notify-popup-show</td>
<td>
<pre>
var notifyPopup = new kintoneUIComponent.NotifyPopup({
    text: 'Submit sucessffully',
    type: 'success'
});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(notifyPopup.render());
 
notifyPopup.hide();
</pre>
</td>
<td>Hide the notify popup.</td>
</tr>

<tr>
<td>kuc-notify-popup-disable</td>
<td>
<pre>
var notifyPopup = new kintoneUIComponent.NotifyPopup({
    text: 'Submit sucessffully',
    type: 'success'
});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(notifyPopup.render());
 
notifyPopup.disable();
</pre>
</td>
<td>Disabled the notify popup.</td>
</tr>

<tr>
<td>kuc-notify-popup-enable</td>
<td>
<pre>
var notifyPopup = new kintoneUIComponent.NotifyPopup({
    text: 'Submit sucessffully',
    type: 'success'
});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(notifyPopup.render());
 
notifyPopup.enable();
</pre>
</td>
<td>Enabled the notify popup.</td>
</tr>
</table>