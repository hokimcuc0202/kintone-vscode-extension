
# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-radio-button</td>
<td>
<pre>
var radioBtn = new kintoneUIComponent.RadioButton({
     name: "fruit",
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
    value: 'Banana'
});
</pre>
</td>
<td>Constructor</td>
</tr>

<tr>
<td>kuc-radio-button-render</td>
<td>
<pre>
</pre>
</td>
<td></td>
</tr>

<tr>
<td>kuc-radio-button-render</td>
<td>
<pre>
var radioBtn = new kintoneUIComponent.RadioButton({
     name: "fruit",
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
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(radioBtn.render());
</pre>
</td>
<td>Get dom element of component.</td>
</tr>

<tr>
<td>kuc-radio-button-add-item</td>
<td>
<pre>
var radioBtn = new kintoneUIComponent.RadioButton({
     name: "fruit",
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
            }
        ],
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(radioBtn.render());
 
radioBtn.addItem({label: 'Lemon', value: 'Lemon', isDisabled: true});
</pre>
</td>
<td>Add an item to end of the radio button list.</td>
</tr>

<tr>
<td>kuc-radio-button-remove-item</td>
<td>
<pre>
var radioBtn = new kintoneUIComponent.RadioButton({
     name: "fruit",
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
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(radioBtn.render());
 
radioBtn.removeItem(0);
</pre>
</td>
<td>Remove item at specific index of radio button list.</td>
</tr>

<tr>
<td>kuc-radio-button-get-items</td>
<td>
<pre>
var radioBtn = new kintoneUIComponent.RadioButton({
     name: "fruit",
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
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(radioBtn.render());
 
var items = radioBtn.getItems();
items.forEach(function(item) {
    console.log(item);
});
</pre>
</td>
<td>Get all items in radio button list.</td>
</tr>

<tr>
<td>kuc-radio-button-get-value</td>
<td>
<pre>
var radioBtn = new kintoneUIComponent.RadioButton({
     name: "fruit",
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
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(radioBtn.render());
 
radioBtn.getValue();
</pre>
</td>
<td>Get the selected item in radio button.</td>
</tr>

<tr>
<td>kuc-radio-button-render</td>
<td>
<pre>
</pre>
</td>
<td></td>
</tr>

<tr>
<td>kuc-radio-button-set-value</td>
<td>
<pre>
</pre>
</td>
<td></td>
</tr>

<tr>
<td>kuc-radio-button-render</td>
<td>
<pre>
var radioBtn = new kintoneUIComponent.RadioButton({
     name: "fruit",
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
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(radioBtn.render());
 
radioBtn.setValue('Lemon');
</pre>
</td>
<td>Set the selected item for radio button.</td>
</tr>

<tr>
<td>kuc-radio-button-disable-item</td>
<td>
<pre>
</pre>
</td>
<td></td>
</tr>

<tr>
<td>kuc-radio-button-render</td>
<td>
<pre>
var radioBtn = new kintoneUIComponent.RadioButton({
     name: "fruit",
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
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(radioBtn.render());
 
radioBtn.disableItem('Orange');
</pre>
</td>
<td>Set the disabled item for the radio button.</td>
</tr>

<tr>
<td>kuc-radio-button-enable-item</td>
<td>
<pre>
var radioBtn = new kintoneUIComponent.RadioButton({
     name: "fruit",
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
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(radioBtn.render());
 
radioBtn.enableItem('Banana');
</pre>
</td>
<td>Set the enabled item for radio button.</td>
</tr>

<tr>
<td>kuc-radio-button-on</td>
<td>
<pre>
var radioBtn = new kintoneUIComponent.RadioButton({
     name: "fruit",
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
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(radioBtn.render());
 
radioBtn.on('change', function(value) {
    console.log('on change');
});
</pre>
</td>
<td>Register callback for change event</td>
</tr>

<tr>
<td>kuc-radio-button-show</td>
<td>
<pre>
</pre>
</td>
<td></td>
</tr>

<tr>
<td>kuc-radio-button-show</td>
<td>
<pre>
var radioBtn = new kintoneUIComponent.RadioButton({
     name: "fruit",
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
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(radioBtn.render());
 
radioBtn.show();
</pre>
</td>
<td>Display the radio button.</td>
</tr>

<tr>
<td>kuc-radio-button-hide</td>
<td>
<pre>
var radioBtn = new kintoneUIComponent.RadioButton({
     name: "fruit",
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
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(radioBtn.render());
 
radioBtn.hide();
</pre>
</td>
<td>Hide the radio button.</td>
</tr>

<tr>
<td>kuc-radio-button-disable</td>
<td>
<pre>
var radioBtn = new kintoneUIComponent.RadioButton({
     name: "fruit",
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
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(radioBtn.render());
 
radioBtn.disable();
</pre>
</td>
<td>Disabled the radio button.</td>
</tr>

<tr>
<td>kuc-radio-button-enable</td>
<td>
<pre>
var radioBtn = new kintoneUIComponent.RadioButton({
     name: "fruit",
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
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(radioBtn.render());
 
radioBtn.enable();
</pre>
</td>
<td>Enabled the radio button.</td>
</tr>
</table>