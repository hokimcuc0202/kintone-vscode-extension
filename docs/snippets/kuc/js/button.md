# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-button</td>
<td>
<pre>
var button = new kintoneUIComponent.Button({
    text: 'Submit',
    type: 'submit'
});
</pre>
</td>
<td>constructor of Button component </td>
</tr>

<tr>
<td>kuc-button-render</td>
<td>
<pre>	
var button = new kintoneUIComponent.Button({text: 'button'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(button.render());
</pre>
</td>
<td>Get dom element of component.</td>
</tr>

<tr>
<td>kuc-button-set-text</td>
<td>
<pre>
var button = new kintoneUIComponent.Button({text: 'button'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(button.render());
button.setText('submit');
</pre>
</td>
<td>Set displayed text in button.</td>
</tr>

<tr>
<td>kuc-button-set-type</td>
<td>
<pre>
var button = new kintoneUIComponent.Button({text: 'button'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(button.render());
button.setType('normal');
</pre>
</td>
<td>Set the displayed type for button.</td>
</tr>

<tr>
<td>kuc-button-on</td>
<td>
<pre>
var button = new kintoneUIComponent.Button({text: 'button'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(button.render());
button.on('click', function(event) {
    console.log('on click');
});
</pre>
</td>
<td>Register callback for click event</td>
</tr>

<tr>
<td>kuc-button-show</td>
<td>
<pre>
var button = new kintoneUIComponent.Button({text: 'button'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(button.render());
button.show();
</pre>
</td>
<td>Display button.</td>
</tr>

<tr>
<td>kuc-button-hide</td>
<td>
<pre>
var button = new kintoneUIComponent.Button({text: 'button'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(button.render());
button.hide();
</pre>
</td>
<td>Hide button.</td>
</tr>

<tr>
<td>kuc-button-disable</td>
<td>
<pre>
var button = new kintoneUIComponent.Button({text: 'button'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(button.render());
button.disable();
</pre>
</td>
<td>Disable button.</td>
</tr>

<tr>
<td>kuc-button-enable</td>
<td>
<pre>
var button = new kintoneUIComponent.Button({text: 'button'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(button.render());
button.enable();
</pre>
</td>
<td>Enable button.</td>
</tr>
</table>
