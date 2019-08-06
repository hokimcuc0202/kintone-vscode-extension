
# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-text-area</td>
<td>
<pre>
var textArea = new kintoneUIComponent.TextArea({value: 'textarea'});
</pre>
</td>
<td>Construtor</td>
</tr>

<tr>
<td>kuc-text-area-render</td>
<td>
<pre>
var textArea = new kintoneUIComponent.TextArea({value: 'textarea'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(textArea.render());
</pre>
</td>
<td>Get dom element of component.</td>
</tr>

<tr>
<td>kuc-text-area-set-value</td>
<td>
<pre>
var textArea = new kintoneUIComponent.TextArea({value: 'textarea'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(textArea.render());
 
textArea.setValue('set value into textarea');
</pre>
</td>
<td>Set the value of textarea field.</td>
</tr>

<tr>
<td>kuc-text-area-get-value</td>
<td>
<pre>
var textArea = new kintoneUIComponent.TextArea({value: 'textarea'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(textArea.render());
 
textArea.getValue();
</pre>
</td>
<td>Get the value of textarea field.</td>
</tr>

<tr>
<td>kuc-text-area-on</td>
<td>
<pre>
var textArea = new kintoneUIComponent.TextArea({value: 'textarea'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(textArea.render());
 
textArea.on('click', function(event) {
    console.log('on click');
});
</pre>
</td>
<td>Register callback for a event of component</td>
</tr>

<tr>
<td>kuc-text-area-show</td>
<td>
<pre>	
var textArea = new kintoneUIComponent.TextArea({value: 'textarea'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(textArea.render());
 
textArea.show();
</pre>
</td>
<td>Display the TextArea field.</td>
</tr>

<tr>
<td>kuc-text-area-hide</td>
<td>
<pre>
var textArea = new kintoneUIComponent.TextArea({value: 'textarea'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(textArea.render());
 
textArea.hide();
</pre>
</td>
<td>Hide the TextArea field.</td>
</tr>

<tr>
<td>kuc-text-area-disable</td>
<td>
<pre>
var textArea = new kintoneUIComponent.TextArea({value: 'textarea'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(textArea.render());
 
textArea.disable();
</pre>
</td>
<td>Disabled the TextArea field.</td>
</tr>

<tr>
<td>kuc-text-area-enable</td>
<td>
<pre>
var textArea = new kintoneUIComponent.TextArea({value: 'textarea'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(textArea.render());
 
textArea.enable();
</pre>
</td>
<td>Enabled the TextArea field.</td>
</tr>
</table>