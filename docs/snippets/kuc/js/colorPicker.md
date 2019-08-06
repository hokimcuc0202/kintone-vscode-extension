# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-color-picker</td>
<td>
<pre>
var colorPicker = new kintoneUIComponent.ColorPicker({color: '#FF0000'});
</pre>
</td>
<td>Constructor of ColorPicker</td>
</tr>

<tr>
<td>kuc-color-picker-set-color</td>
<td>
<pre>
var colorPicker = new kintoneUIComponent.ColorPicker({color: '#FF0000'});
kintone.events.on('app.record.index.show', function(event) {
    var el = kintone.app.getHeaderSpaceElement();
    el.appendChild(colorPicker.render());
});
</pre>
</td>
<td>Get dom element of component.</td>
</tr>

<tr>
<td>kuc-color-picker-get-color</td>
<td>
<pre>
var colorPicker = new kintoneUIComponent.ColorPicker({color: '#FF0000'});
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(colorPicker.render());
colorPicker.setColor('#666666');
</pre>
</td>
<td>Set the color of colorpicker .</td>
</tr>

<tr>
<td>kuc-color-picker-on</td>
<td>
<pre>
var colorPicker = new kintoneUIComponent.ColorPicker({color: '#FF0000'});
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(colorPicker.render());
colorPicker.getColor();
</pre>
</td>
<td>Get the color of colorpicker.</td>
</tr>

<tr>
<td>kuc-color-picker-show</td>
<td>
<pre>
var colorPicker = new kintoneUIComponent.ColorPicker({color: '#FF0000'});
colorPicker.on('change', function(color) {
    console.log(color);
});
 
kintone.events.on('app.record.index.show', function(event) {
    var el = kintone.app.getHeaderSpaceElement();
    el.appendChild(colorPicker.render());
});
</pre>
</td>
<td>Register callback for click event</td>
</tr>

<tr>
<td>kuc-color-picker-hide</td>
<td>
<pre>
var myColorPicker = new kintoneUIComponent.ColorPicker({color: '#FF0000'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(myColorPicker.render());
myColorPicker.show();
</pre>
</td>
<td>Display ColorPicker.</td>
</tr>

<tr>
<td>kuc-color-picker-disable</td>
<td>
<pre>
var myColorPicker = new kintoneUIComponent.ColorPicker({color: '#FF0000'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(myColorPicker.render());
myColorPicker.hide();
</pre>
</td>
<td>Hide ColorPicker.</td>
</tr>

<tr>
<td>kuc-color-picker-enable</td>
<td>
<pre>
var myColorPicker = new kintoneUIComponent.ColorPicker({color: '#FF0000'});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(myColorPicker.render());
myColorPicker.disable();
</pre>
</td>
<td>Disable ColorPicker.</td>
</tr>
</table>