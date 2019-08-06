# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-check-box</td>
<td>
<pre>
var checkbox = new kintoneUIComponent.CheckBox ({
       items: [
            {
                label: 'Orange',
                value: 'Orange',
                isDisabled: false
            },
            {
                label: 'Banana',
                value: 'Banana',
                isDisabled: true
            },
            {
                label: 'Lemon',
                value: 'Lemon',
                isDisabled: true
            },
     ],
     value: ['Orange', 'Banana']
});
</pre>
</td>
<td>Constructor of CheckBox</td>
</tr>

<tr>
<td>kuc-check-box-render</td>
<td>
<pre>
var checkbox = new kintoneUIComponent.CheckBox ({
       items: [
            {
                label: 'Orange',
                value: 'Orange',
                isDisabled: false
            },
            {
                label: 'Banana',
                value: 'Banana',
                isDisabled: true
            },
            {
                label: 'Lemon',
                value: 'Lemon',
                isDisabled: true
            },
     ],
     value: ['Orange', 'Banana']
});
 
var body = document.getElementsByTagName('BODY')[0];
body.appendChild(checkbox.render());
</pre>
</td>
<td>Dom element</td>
</tr>

<tr>
<td>kuc-check-box-add-item</td>
<td>
<pre>
var checkbox = new kintoneUIComponent.CheckBox ({
       items: [
            {
                label: 'Orange',
                value: 'Orange',
                isDisabled: false
            },
            {
                label: 'Banana',
                value: 'Banana',
                isDisabled: true
            },
            {
                label: 'Lemon',
                value: 'Lemon',
                isDisabled: true
            },
     ],
     value: ['Orange', 'Banana']
});
 
var body = document.getElementsByTagName('BODY')[0];
body.appendChild(checkbox.render());
 
checkbox.addItem({
    label: 'Grape',
    value: 'grape',
    isDisabled: false
});
</pre>
</td>
<td>Add an item to the end of checkbox list.</td>
</tr>

<tr>
<td>kuc-check-box-get-item</td>
<td>
<pre>
var checkbox = new kintoneUIComponent.CheckBox ({
       items: [
            {
                label: 'Orange',
                value: 'Orange',
                isDisabled: false
            },
            {
                label: 'Banana',
                value: 'Banana',
                isDisabled: true
            },
            {
                label: 'Lemon',
                value: 'Lemon',
                isDisabled: true
            },
     ],
     value: ['Orange', 'Banana']
});
 
var body = document.getElementsByTagName('BODY')[0];
body.appendChild(checkbox.render());
 
var firstItem = checkbox.getItem(0);
console.log(firstItem);
</pre>
</td>
<td>Get the value of specific position in checkbox list.</td>
</tr>

<tr>
<td>kuc-check-box-remove-item</td>
<td>
<pre>
var checkbox = new kintoneUIComponent.CheckBox ({
       items: [
            {
                label: 'Orange',
                value: 'Orange',
                isDisabled: false
            },
            {
                label: 'Banana',
                value: 'Banana',
                isDisabled: true
            },
            {
                label: 'Lemon',
                value: 'Lemon',
                isDisabled: true
            },
     ],
     value: ['Orange', 'Banana']
});

var body = document.getElementsByTagName('BODY')[0];
body.appendChild(checkbox.render());

checkbox.removeItem(0);
</pre>
</td>
<td>Remove the specific item from checkbox list.</td>
</tr>

<tr>
<td>Get all items from the checkbox</td>
<td>
<pre>
var checkbox = new kintoneUIComponent.CheckBox ({
       items: [
            {
                label: 'Orange',
                value: 'Orange',
                isDisabled: false
            },
            {
                label: 'Banana',
                value: 'Banana',
                isDisabled: true
            },
            {
                label: 'Lemon',
                value: 'Lemon',
                isDisabled: true
            },
     ],
     value: ['Orange', 'Banana']
});
 
var body = document.getElementsByTagName('BODY')[0];
body.appendChild(checkbox.render());
 
var items = checkbox.getItems();
items.forEach(function(item) {
    console.log(item.value + ':' + item.isDisabled);
});
</pre>
</td>
<td>kuc-check-box-get-items</td>
</tr>

<tr>
<td>kuc-check-box-get-value</td>
<td>
<pre>
var checkbox = new kintoneUIComponent.CheckBox ({
       items: [
            {
                label: 'Orange',
                value: 'Orange',
                isDisabled: false
            },
            {
                label: 'Banana',
                value: 'Banana',
                isDisabled: true
            },
            {
                label: 'Lemon',
                value: 'Lemon',
                isDisabled: true
            },
     ],
     value: ['Orange', 'Banana']
});
 
var body = document.getElementsByTagName('BODY')[0];
body.appendChild(checkbox.render());
 
var value = checkbox.getValue();
value.forEach(function(item) {
    console.log(item);
});
</pre>
</td>
<td>Get the checked values of the checkbox.</td>
</tr>

<tr>
<td>kuc-check-box-set-value</td>
<td>
<pre>	
var checkbox = new kintoneUIComponent.CheckBox ({
       items: [
            {
                label: 'Orange',
                value: 'Orange',
                isDisabled: false
            },
            {
                label: 'Banana',
                value: 'Banana',
                isDisabled: true
            },
            {
                label: 'Lemon',
                value: 'Lemon',
                isDisabled: true
            },
     ],
     value: ['Orange', 'Banana']
});
 
var body = document.getElementsByTagName('BODY')[0];
body.appendChild(checkbox.render());
 
checkbox.setValue(['Lemon']);
</pre>
</td>
<td>Set the checked value of checkbox.</td>
</tr>

<tr>
<td>kuc-check-box-disable-item</td>
<td>
<pre>
var checkbox = new kintoneUIComponent.CheckBox ({
       items: [
            {
                label: 'Orange',
                value: 'Orange',
                isDisabled: false
            },
            {
                label: 'Banana',
                value: 'Banana',
                isDisabled: true
            },
            {
                label: 'Lemon',
                value: 'Lemon',
                isDisabled: true
            },
     ],
     value: ['Orange', 'Banana']
});
 
var body = document.getElementsByTagName('BODY')[0];
body.appendChild(checkbox.render());
 
checkbox.disableItem('Orange');
</pre>
</td>
<td>Set the disabled item of checkbox.</td>
</tr>

<tr>
<td>kuc-check-box-enable-item</td>
<td>
<pre>
var checkbox = new kintoneUIComponent.CheckBox ({
       items: [
            {
                label: 'Orange',
                value: 'Orange',
                isDisabled: false
            },
            {
                label: 'Banana',
                value: 'Banana',
                isDisabled: true
            },
            {
                label: 'Lemon',
                value: 'Lemon',
                isDisabled: true
            },
     ],
     value: ['Orange', 'Banana']
});
 
var body = document.getElementsByTagName('BODY')[0];
body.appendChild(checkbox.render());
 
checkbox.enableItem('Banana');
</pre>
</td>
<td>Set the enable item of checkbox.</td>
</tr>

<tr>
<td>kuc-check-box-on</td>
<td>
<pre>
var checkbox = new kintoneUIComponent.CheckBox ({
       items: [
            {
                label: 'Orange',
                value: 'Orange',
                isDisabled: false
            },
            {
                label: 'Banana',
                value: 'Banana',
                isDisabled: true
            },
            {
                label: 'Lemon',
                value: 'Lemon',
                isDisabled: true
            },
     ],
     value: ['Orange', 'Banana']
});
 
var body = document.getElementsByTagName('BODY')[0];
body.appendChild(checkbox.render());
 
checkbox.on('change', function(value) {
    console.log('on change');
});
</pre>
</td>
<td>Register callback for change event</td>
</tr>

<tr>
<td>kuc-check-box-show</td>
<td>
<pre>
var checkbox = new kintoneUIComponent.CheckBox ({
       items: [
            {
                label: 'Orange',
                value: 'Orange',
                isDisabled: false
            },
            {
                label: 'Banana',
                value: 'Banana',
                isDisabled: true
            },
            {
                label: 'Lemon',
                value: 'Lemon',
                isDisabled: true
            },
     ],
     value: ['Orange', 'Banana']
});
 
var body = document.getElementsByTagName('BODY')[0];
body.appendChild(checkbox.render());
 
checkbox.show();
</pre>
</td>
<td>Display the checkbox.</td>
</tr>

<tr>
<td>kuc-check-box-hide</td>
<td>
<pre>
var checkbox = new kintoneUIComponent.CheckBox ({
       items: [
            {
                label: 'Orange',
                value: 'Orange',
                isDisabled: false
            },
            {
                label: 'Banana',
                value: 'Banana',
                isDisabled: true
            },
            {
                label: 'Lemon',
                value: 'Lemon',
                isDisabled: true
            },
     ],
     value: ['Orange', 'Banana']
});
 
var body = document.getElementsByTagName('BODY')[0];
body.appendChild(checkbox.render());
 
checkbox.hide();
</pre>
</td>
<td>Hide the checkbox.</td>
</tr>

<tr>
<td>kuc-check-box-disable</td>
<td>
<pre>
var checkbox = new kintoneUIComponent.CheckBox ({
       items: [
            {
                label: 'Orange',
                value: 'Orange',
                isDisabled: false
            },
            {
                label: 'Banana',
                value: 'Banana',
                isDisabled: true
            },
            {
                label: 'Lemon',
                value: 'Lemon',
                isDisabled: true
            },
     ],
     value: ['Orange', 'Banana']
});
 
var body = document.getElementsByTagName('BODY')[0];
body.appendChild(checkbox.render());
 
checkbox.disable();
</pre>
</td>
<td>Disabled the checkbox.</td>
</tr>

<tr>
<td>kuc-check-box-enable</td>
<td>
<pre>
var checkbox = new kintoneUIComponent.CheckBox ({
       items: [
            {
                label: 'Orange',
                value: 'Orange',
                isDisabled: false
            },
            {
                label: 'Banana',
                value: 'Banana',
                isDisabled: true
            },
            {
                label: 'Lemon',
                value: 'Lemon',
                isDisabled: true
            },
     ],
     value: ['Orange', 'Banana']
});
 
var body = document.getElementsByTagName('BODY')[0];
body.appendChild(checkbox.render());
 
checkbox.enable();
</pre>
</td>
<td>Enabled the checkbox.</td>
</tr>
</table>