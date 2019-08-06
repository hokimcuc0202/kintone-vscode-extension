# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-icon-button</td>
<td>
<pre>
var insertBtn = new kintoneUIComponent.IconButton({type: 'insert',color:'blue', size: 'small'});
</pre>
</td>
<td>Constructor</td>
</tr>

<tr>
<td>kuc-icon-button-render</td>
<td>
<pre>
var iconBtn = new kintoneUIComponent.IconButton({type: 'insert'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(iconBtn.render());
</pre>
</td>
<td>Get dom element of component.</td>
</tr>

<tr>
<td>kuc-icon-button-render</td>
<td>
<pre>
</pre>
</td>
<td></td>
</tr>

<tr>
<td>kuc-icon-button-set-color</td>
<td>
<pre>
var iconBtn = new kintoneUIComponent.IconButton({type: 'insert'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(iconBtn.render());
iconBtn.setColor('green');
</pre>
</td>
<td>Change color of icon button.</td>
</tr>

<tr>
<td>kuc-icon-button-render</td>
<td>
<pre>
</pre>
</td>
<td></td>
</tr>

<tr>
<td>kuc-icon-button-set-shape</td>
<td>
<pre>
var iconBtn = new kintoneUIComponent.IconButton({type: 'insert'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(iconBtn.render());
iconBtn.setShape('normal');
</pre>
</td>
<td>Change shape of icon button.</td>
</tr>

<tr>
<td>kuc-icon-button-set-type</td>
<td>
<pre>
var iconBtn = new kintoneUIComponent.IconButton({type: 'insert'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(iconBtn.render());
 
iconBtn.setType('remove');
</pre>
</td>
<td>Set the type of the button.</td>
</tr>

<tr>
<td>kuc-icon-button-on</td>
<td>
<pre>
var iconBtn = new kintoneUIComponent.IconButton({type: 'insert'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(iconBtn.render());
 
iconBtn.on('click', function(event) {
    console.log('on click');
});
</pre>
</td>
<td>Register callback for click event</td>
</tr>

<tr>
<td>kuc-icon-button-show</td>
<td>
<pre>
var iconBtn = new kintoneUIComponent.IconButton({type: 'insert'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(iconBtn.render());
 
iconBtn.show();
</pre>
</td>
<td>Display the icon button.</td>
</tr>

<tr>
<td>kuc-icon-button-hide</td>
<td>
<pre>
var iconBtn = new kintoneUIComponent.IconButton({type: 'insert'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(iconBtn.render());
 
iconBtn.hide();
</pre>
</td>
<td>Hide the icon button.</td>
</tr>

<tr>
<td>kuc-icon-button-disable</td>
<td>
<pre>
var iconBtn = new kintoneUIComponent.IconButton({type: 'insert'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(iconBtn.render());
 
iconBtn.disable();
</pre>
</td>
<td>Disabled the icon button.</td>
</tr>

<tr>
<td>kuc-icon-button-enable</td>
<td>
<pre>
var iconBtn = new kintoneUIComponent.IconButton({type: 'insert'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(iconBtn.render());
 
iconBtn.enable();
</pre>
</td>
<td>Enabled the icon button.</td>
</tr>
</table>