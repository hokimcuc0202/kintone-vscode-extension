# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-text</td>
<td>
<pre>
var text= new kintoneUIComponent.Text({value: '12345'});
</pre>
</td>
<td>Constructor</td>
</tr>

<tr>
<td>kuc-text-render</td>
<td>
<pre>
var text = new kintoneUIComponent.Text({value: 'input text'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(text.render());
</pre>
</td>
<td>Get dom element of component.</td>
</tr>

<tr>
<td>kuc-text-set-value</td>
<td>
<pre>
var text = new kintoneUIComponent.Text({value: 'input text'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(text.render());
 
text.setValue('input text');
</pre>
</td>
<td>Set the value of text field.</td>
</tr>

<tr>
<td>kuc-text-get-value</td>
<td>
<pre>
var text = new kintoneUIComponent.Text({value: 'input text'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(text.render());
 
text.getValue();
</pre>
</td>
<td>Get the value of text field.</td>
</tr>

<tr>
<td>kuc-text-on</td>
<td>
<pre>	
var text = new kintoneUIComponent.Text({value: 'input text'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(text.render());
 
text.on('click', function(event) {
    console.log('on click');
    console.log('value: ' + event.target.value);
});
</pre>
</td>
<td>Register callback for a event of component</td>
</tr>

<tr>
<td>kuc-text-show</td>
<td>
<pre>	
var text = new kintoneUIComponent.Text({value: 'input text'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(text.render());
 
text.show();
</pre>
</td>
<td>Display the Text field.</td>
</tr>

<tr>
<td>kuc-text-hide</td>
<td>
<pre>
var text = new kintoneUIComponent.Text({value: 'input text'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(text.render());
 
text.hide();
</pre>
</td>
<td>Hide the Text field.</td>
</tr>

<tr>
<td>kuc-text-disable</td>
<td>
<pre>
var text = new kintoneUIComponent.Text({value: 'input text'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(text.render());
 
text.disable();
</pre>
</td>
<td>Disabled the Text field.</td>
</tr>

<tr>
<td>kuc-text-enable</td>
<td>
<pre>
var text = new kintoneUIComponent.Text({value: 'input text'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(text.render());
 
text.enable();
</pre>
</td>
<td>Enabled the Text field.</td>
</tr>
</table>