# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-field-group</td>
<td>
<pre>
const text = new kintoneUIComponent.Text({ value: "12345" });
 
const fieldGroup = new kintoneUIComponent.FieldGroup({
      content: text.render(),
      name: 'Group',
      toggle: 'expand'
    })
</pre>
</td>
<td>Constructor</td>
</tr>

<tr>
<td>kuc-field-group-render</td>
<td>
<pre>
</pre>
</td>
<td></td>
</tr>

<tr>
<td>kuc-field-group-render</td>
<td>
<pre>	
const text = new kintoneUIComponent.Text({ value: "12345" });
 
const fieldGroup = new kintoneUIComponent.FieldGroup({
      content: text.render(),
      name: 'Group',
      toggle: 'expand'
    })
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(fieldGroup.render());
</pre>
</td>
<td>Get dom element of component.</td>
</tr>

<tr>
<td>kuc-field-group-set-content</td>
<td>
<pre>
const radioBtn = new kintoneUIComponent.RadioButton({
      items: [{ label: 'Orange', value: 'orange' }, { label: 'Banana', value: 'banana' }],
      value: 'orange',
      name: 'Fruit'
});
 
const fieldGroup = new kintoneUIComponent.FieldGroup({
      content: radioBtn.render(),
      name: 'Group',
      toggle: 'expand'
    })
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(fieldGroup.render());
 
const text = new kintoneUIComponent.Text({ value: "12345" });
fieldGroup.setContent(text.render());
</pre>
</td>
<td>Add an item to end of the field group.</td>
</tr>

<tr>
<td>kuc-field-group-get-content</td>
<td>
<pre>

</pre>
</td>
<td></td>
</tr>

<tr>
<td>kuc-field-group-render</td>
<td>
<pre>
const radioBtn = new kintoneUIComponent.RadioButton({
      items: [{ label: 'Orange', value: 'orange' }, { label: 'Banana', value: 'banana' }],
      value: 'orange',
      name: 'Fruit'
});
 
const fieldGroup = new kintoneUIComponent.FieldGroup({
      content: radioBtn.render(),
      name: 'Group',
      toggle: 'expand'
    })
 
fieldGroup.getContent();
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(fieldGroup.render());
</pre>
</td>
<td>Get content of field group</td>
</tr>

<tr>
<td>kuc-field-group-set-name</td>
<td>
<pre>

</pre>
</td>
<td></td>
</tr>

<tr>
<td>kuc-field-group-render</td>
<td>
<pre>
const text = new kintoneUIComponent.Text({ value: "12345" });
 
const fieldGroup = new kintoneUIComponent.FieldGroup({
      content: text.render(),
      name: 'Group',
      toggle: 'expand'
    })
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(fieldGroup.render());
 
fieldGroup.setName('New Group Name');
</pre>
</td>
<td>Set the name for the field group.</td>
</tr>

<tr>
<td>kuc-field-group-get-name</td>
<td>
<pre>
const text = new kintoneUIComponent.Text({ value: "12345" });
 
const fieldGroup = new kintoneUIComponent.FieldGroup({
      content: text.render(),
      name: 'Group',
      toggle: 'expand'
    })
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(fieldGroup.render());
 
fieldGroup.getName();
</pre>
</td>
<td>Get name of field group</td>
</tr>

<tr>
<td>kuc-field-group-set-toggle</td>
<td>
<pre>
const text = new kintoneUIComponent.Text({ value: "12345" });
 
const fieldGroup = new kintoneUIComponent.FieldGroup({
      items: text.render(),
      name: 'Group',
      toggle: 'expand'
    })
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(fieldGroup.render());
 
fieldGroup.setToggle('collapse');
</pre>
</td>
<td>Set the toggle state for the field group.</td>
</tr>

<tr>
<td>kuc-field-group-render</td>
<td>
<pre>

</pre>
</td>
<td>get-toggle</td>
</tr>

<tr>
<td>kuc-field-group-render</td>
<td>
<pre>
const text = new kintoneUIComponent.Text({ value: "12345" });
 
const fieldGroup = new kintoneUIComponent.FieldGroup({
      content: text.render(),
      name: 'Group',
      toggle: 'expand'
    })
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(fieldGroup.render());
 
fieldGroup.getToggle();
</pre>
</td>
<td>Get toggle state of the field group.</td>
</tr>
</table>