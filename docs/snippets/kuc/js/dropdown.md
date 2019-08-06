# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-dropdown</td>
<td>
<pre>
var dropdown = new kintoneUIComponent.Dropdown({
    items: [
        {
            label: 'Orange',
            value: 'Orange',
            isDisabled: true
        },
        {
            label: 'Banana',
            value: 'Banana',
            isDisabled: false
        }
    ],
    value: 'Banana'
});
</pre>
</td>
<td>Constructor of dropdown</td>
</tr>

<tr>
<td>kuc-dropdown-render</td>
<td>
<pre>
var dropdown = new kintoneUIComponent.Dropdown({
    items: [
        {
            label: 'Orange',
            value: 'Orange',
            isDisabled: true
        },
        {
            label: 'Banana',
            value: 'Banana',
            isDisabled: false
        }
    ],
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(dropdown.render());
</pre>
</td>
<td>Get dom element of component.</td>
</tr>

<tr>
<td>kuc-dropdown-add-item</td>
<td>
<pre>
var dropdown = new kintoneUIComponent.Dropdown({
    items: [
        {
            label: 'Orange',
            value: 'Orange',
            isDisabled: true
        },
        {
            label: 'Banana',
            value: 'Banana',
            isDisabled: false
        }
    ],
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(dropdown.render());
 
dropdown.addItem({label: 'Lemon', value: 'Lemon', isDisabled: true});
</pre>
</td>
<td>Add an item to dropdown list.</td>
</tr>

<tr>
<td>kuc-dropdown-remove-item</td>
<td>
<pre>
var dropdown = new kintoneUIComponent.Dropdown({
    items: [
        {
            label: 'Orange',
            value: 'Orange',
            isDisabled: true
        },
        {
            label: 'Banana',
            value: 'Banana',
            isDisabled: false
        }
    ],
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(dropdown.render());
var firstItem = dropdown.getItems()[0];
dropdown.removeItem(0);
console.log(firstItem);
</pre>
</td>
<td>Remove an item at specific position in dropdown's list.</td>
</tr>

<tr>
<td>kuc-dropdown-get-items</td>
<td>
<pre>

var dropdown = new kintoneUIComponent.Dropdown({
    items: [
        {
            label: 'Orange',
            value: 'Orange',
            isDisabled: true
        },
        {
            label: 'Banana',
            value: 'Banana',
            isDisabled: false
        }
    ],
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(dropdown.render());
 
var list = dropdown.getItems();
list.forEach(function(item) {
    console.log(item);
});
</pre>
</td>
<td>The list contains all items of dropdown.</td>
</tr>

<tr>
<td>kuc-dropdown-get-value</td>
<td>
<pre>
var dropdown = new kintoneUIComponent.Dropdown({
    items: [
        {
            label: 'Orange',
            value: 'Orange',
            isDisabled: true
        },
        {
            label: 'Banana',
            value: 'Banana',
            isDisabled: false
        }
    ],
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(dropdown.render());
 
var selectedItem = dropdown.getValue();
console.log(selectedItem);
</pre>
</td>
<td>Get value of the selected item</td>
</tr>

<tr>
<td>kuc-dropdown-set-value</td>
<td>
<pre>
var dropdown = new kintoneUIComponent.Dropdown({
    items: [
        {
            label: 'Orange',
            value: 'Orange',
            isDisabled: true
        },
        {
            label: 'Banana',
            value: 'Banana',
            isDisabled: false
        }
    ],
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(dropdown.render());
 
dropdown.setValue('Orange');
</pre>
</td>
<td>Set the selected value for dropdown.</td>
</tr>

<tr>
<td>kuc-dropdown-disable-item</td>
<td>
<pre>
var dropdown = new kintoneUIComponent.Dropdown({
    items: [
        {
            label: 'Orange',
            value: 'Orange',
            isDisabled: true
        },
        {
            label: 'Banana',
            value: 'Banana',
            isDisabled: false
        }
    ],
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(dropdown.render());
 
dropdown.disableItem('Orange');
</pre>
</td>
<td>Set the disabled item for dropdown.</td>
</tr>

<tr>
<td>kuc-dropdown-enable-item</td>
<td>
<pre>
var dropdown = new kintoneUIComponent.Dropdown({
    items: [
        {
            label: 'Orange',
            value: 'Orange',
            isDisabled: true
        },
        {
            label: 'Banana',
            value: 'Banana',
            isDisabled: false
        }
    ],
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(dropdown.render());
 
dropdown.enableItem('Banana');
</pre>
</td>
<td>Set the enabled item for dropdown.</td>
</tr>

<tr>
<td>kuc-dropdown-on</td>
<td>
<pre>
var dropdown = new kintoneUIComponent.Dropdown({
    items: [
        {
            label: 'Orange',
            value: 'Orange',
            isDisabled: true
        },
        {
            label: 'Banana',
            value: 'Banana',
            isDisabled: false
        }
    ],
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(dropdown.render());
 
dropdown.on('change', function(value) {
    console.log('on change');
});
</pre>
</td>
<td>	Register callback for change event</td>
</tr>

<tr>
<td>kuc-dropdown-show</td>
<td>
<pre>
var dropdown = new kintoneUIComponent.Dropdown({
    items: [
        {
            label: 'Orange',
            value: 'Orange',
            isDisabled: true
        },
        {
            label: 'Banana',
            value: 'Banana',
            isDisabled: false
        }
    ],
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(dropdown.render());
 
dropdown.show();
</pre>
</td>
<td>Display the dropdown.</td>
</tr>

<tr>
<td>kuc-dropdown-hide</td>
<td>
<pre>
var dropdown = new kintoneUIComponent.Dropdown({
    items: [
        {
            label: 'Orange',
            value: 'Orange',
            isDisabled: true
        },
        {
            label: 'Banana',
            value: 'Banana',
            isDisabled: false
        }
    ],
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(dropdown.render());
 
dropdown.hide();
</pre>
</td>
<td>Hide the dropdown.</td>
</tr>

<tr>
<td>kuc-dropdown-disable</td>
<td>
<pre>
var dropdown = new kintoneUIComponent.Dropdown({
    items: [
        {
            label: 'Orange',
            value: 'Orange',
            isDisabled: true
        },
        {
            label: 'Banana',
            value: 'Banana',
            isDisabled: false
        }
    ],
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(dropdown.render());
 
dropdown.disable();
</pre>
</td>
<td>Disabled the dropdown.</td>
</tr>

<tr>
<td>kuc-dropdown-enable</td>
<td>
<pre>
var dropdown = new kintoneUIComponent.Dropdown({
    items: [
        {
            label: 'Orange',
            value: 'Orange',
            isDisabled: true
        },
        {
            label: 'Banana',
            value: 'Banana',
            isDisabled: false
        }
    ],
    value: 'Banana'
});
 
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(dropdown.render());
 
dropdown.enable();
</pre>
</td>
<td>Enabled the dropdown.</td>
</tr>
</table>