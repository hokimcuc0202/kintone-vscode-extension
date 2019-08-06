# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-tabs</td>
<td>
<pre>
var spinner = new kintoneUIComponent.Spinner();
</pre>
</td>
<td>Constructor</td>
</tr>

<tr>
<td>kuc-tabs-render</td>
<td>
<pre>
var button = new kintoneUIComponent.Button({
    text: 'Hello',
    type: 'submit'
});
button.on('click',function(e){
    alert('hello')
})
var tab = new kintoneUIComponent.Tabs({
    items: [
        {
            tabName: "Tab1",
            tabContent: button.render()
        },
        {
            tabName: "Tab2",
            tabContent: "This is Tab2"
        },
    　  {
            tabName: "Tab3",
            tabContent: "This is Tab3"
        }
　  ]
});
 
kintone.events.on('app.record.index.show', function(event) {
    var el = kintone.app.getHeaderSpaceElement()
    el.appendChild(tab.render());
});
</pre>
</td>
<td>Get dom element of component.</td>
</tr>

<tr>
<td>kuc-tabs-add-item</td>
<td>
<pre>	
var tab = new kintoneUIComponent.Tabs({
    items: [
        {
            tabName: "Tab1",
            tabContent: 'This is Tab1'
        },
        {
            tabName: "Tab2",
            tabContent: "This is Tab2"
        },
    　  {
            tabName: "Tab3",
            tabContent: "This is Tab3"
        }
    ]
});
kintone.events.on('app.record.index.show', function(event) {
    var el = kintone.app.getHeaderSpaceElement();
    var item = { tabName: "Tab4", tabContent: "This is Tab4", isDisabled: true };
 
    el.appendChild(tab.render());
    tab.addItem(item);
});
</pre>
</td>
<td>Add an item to end of the tab list.</td>
</tr>

<tr>
<td>kuc-tabs-remove-item</td>
<td>
<pre>
var tab = new kintoneUIComponent.Tabs({
    items: [
        {
            tabName: "Tab1",
            tabContent: 'This is Tab1'
        },
        {
            tabName: "Tab2",
            tabContent: "This is Tab2"
        },
    　  {
            tabName: "Tab3",
            tabContent: "This is Tab3"
        }
    ]
});
kintone.events.on('app.record.index.show', function(event) {
    var el = kintone.app.getHeaderSpaceElement();
 
    el.appendChild(tab.render());
    tab.removeItem(0);
});
</pre>
</td>
<td>Remove item at specific index of tab list.</td>
</tr>

<tr>
<td>kuc-tabs-get-items</td>
<td>
<pre>
</pre>
</td>
<td></td>
</tr>

<tr>
<td>kuc-tabs-render</td>
<td>
<pre>
var tab = new kintoneUIComponent.Tabs({
    items: [
        {
            tabName: "Tab1",
            tabContent: 'This is Tab1'
        },
        {
            tabName: "Tab2",
            tabContent: "This is Tab2"
        },
        　{
            tabName: "Tab3",
            tabContent: "This is Tab3"
        }
    ]
});
 
kintone.events.on('app.record.index.show', function(event) {
    var el = kintone.app.getHeaderSpaceElement();
    el.appendChild(tab.render());
 
    var items = tab.getItems();
    items.forEach(function(item) {
        console.log(item);
    });
});
</pre>
</td>
<td>Get all tabs.</td>
</tr>

<tr>
<td>kuc-tabs-get-value</td>
<td>
<pre>	
var tab = new kintoneUIComponent.Tabs({
    items: [
        {
            tabName: "Tab1",
            tabContent: 'This is Tab1'
        },
        {
            tabName: "Tab2",
            tabContent: "This is Tab2"
        },
    　  {
            tabName: "Tab3",
            tabContent: "This is Tab3"
        }
    ]
});
 
kintone.events.on('app.record.index.show', function(event) {
    var el = kintone.app.getHeaderSpaceElement();
    el.appendChild(tab.render());
 
    console.log(tab.getValue());
});
</pre>
</td>
<td>Get index of selected item.</td>
</tr>

<tr>
<td>kuc-tabs-set-value</td>
<td>
<pre>	
var tab = new kintoneUIComponent.Tabs({
    items: [
        {
            tabName: "Tab1",
            tabContent: 'This is Tab1'
        },
        {
            tabName: "Tab2",
            tabContent: "This is Tab2"
        },
    　  {
            tabName: "Tab3",
            tabContent: "This is Tab3"
        }
    ]
});
kintone.events.on('app.record.index.show', function(event) {
    var el = kintone.app.getHeaderSpaceElement();
    el.appendChild(tab.render());
 
    tab.setValue(1);
});
</pre>
</td>
<td>Set the selected value for the tab.</td>
</tr>

<tr>
<td>kuc-tabs-disable-item</td>
<td>
<pre>
var tab = new kintoneUIComponent.Tabs({
    items: [
        {
            tabName: "Tab1",
            tabContent: 'This is Tab1'
        },
        {
            tabName: "Tab2",
            tabContent: "This is Tab2"
        },
    　  {
            tabName: "Tab3",
            tabContent: "This is Tab3"
        }
    ]
});
kintone.events.on('app.record.index.show', function(event) {
    var el = kintone.app.getHeaderSpaceElement();
    el.appendChild(tab.render());
 
    tab.disableItem('Tab2');
});
</pre>
</td>
<td>Disable a tab.</td>
</tr>

<tr>
<td>kuc-tabs-enable-item</td>
<td>
<pre>
var tab = new kintoneUIComponent.Tabs({
    items: [
        {
            tabName: "Tab1",
            tabContent: 'This is Tab1'
        },
        {
            tabName: "Tab2",
            tabContent: "This is Tab2",
            isDisabled: true
        },
    　  {
            tabName: "Tab3",
            tabContent: "This is Tab3"
        }
    ]
});
kintone.events.on('app.record.index.show', function(event) {
    var el = kintone.app.getHeaderSpaceElement();
    el.appendChild(tab.render());
 
    tab.enableItem('Tab2');
});
</pre>
</td>
<td>Enable a tab.</td>
</tr>
</table>