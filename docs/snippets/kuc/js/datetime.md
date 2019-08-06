# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-date-time</td>
<td>
<pre>
var dateTime = new kintoneUIComponent.DateTime({value: date, type: 'datetime', locale: 'en'});
</pre>
</td>
<td>Constructor of DateTime component</td>
</tr>

<tr>
<td>kuc-date-time-render</td>
<td>
<pre>

const date = new Date();
var dateTime = new kintoneUIComponent.DateTime({value: date, type: 'datetime', locale: 'en'});
const space = kintone.app.getHeaderSpaceElement();
space.appendChild(dateTime.render());
</pre>
</td>
<td>Get dom element of component.</td>
</tr>

<tr>
<td>kuc-date-time-get-value</td>
<td>
<pre>

const date = new Date();
var dateTime = new kintoneUIComponent.DateTime({value: date, type: 'datetime', locale: 'en'});
const space = kintone.app.getHeaderSpaceElement();
space.appendChild(dateTime.render());
dateTime.getValue();
</pre>
</td>
<td>Get the value of datetime field.</td>
</tr>

<tr>
<td>kuc-date-time-set-value</td>
<td>
<pre>
var dateTime = new kintoneUIComponent.DateTime({type: 'datetime', locale: 'en'});
const space = kintone.app.getHeaderSpaceElement();
space.appendChild(dateTime.render());
dateTime.setValue(new Date());
</pre>
</td>
<td>Set the value of datetime field.</td>
</tr>

<tr>
<td>kuc-date-time-get-locale</td>
<td>
<pre>
const date = new Date();
var dateTime = new kintoneUIComponent.DateTime({value: date, type: 'datetime', locale: 'en'});
const space = kintone.app.getHeaderSpaceElement();
space.appendChild(dateTime.render());
dateTime.getLocale();
</pre>
</td>
<td>Get the setting of language.</td>
</tr>

<tr>
<td>kuc-date-time-set-locale</td>
<td>
<pre>
const date = new Date();
var dateTime = new kintoneUIComponent.DateTime({value: date, type: 'datetime'});
const space = kintone.app.getHeaderSpaceElement();
space.appendChild(dateTime.render());
dateTime.setLocale('en');
</pre>
</td>
<td>Set the language setting.</td>
</tr>

<tr>
<td>kuc-date-time-time-show</td>
<td>
<pre>
var container = kintone.app.getHeaderSpaceElement();
container.appendChild(myDateTime.render());
myDateTime.show();
</pre>
</td>
<td>Display DateTime.</td>
</tr>

<tr>
<td>kuc-date-time-time-hide</td>
<td>
<pre>
var myDateTime = new kintoneUIComponent.DateTime({value: new Date()});
 
kintone.events.on('app.record.index.show', function(event) {
    var container = kintone.app.getHeaderSpaceElement();
    container.appendChild(myDateTime.render());
    myDateTime.show();
});
</pre>
</td>
<td>Hide DateTime.</td>
</tr>

<tr>
<td>kuc-date-time-time-disable</td>
<td>
<pre>
var myDateTime = new kintoneUIComponent.DateTime({value: new Date()});
 
kintone.events.on('app.record.index.show', function(event) {
    var container = kintone.app.getHeaderSpaceElement();
    container.appendChild(myDateTime.render());
    myDateTime.disable();
});
</pre>
</td>
<td>Disable DateTime.</td>
</tr>

<tr>
<td>kuc-date-time-time-enable</td>
<td>
<pre>
var myDateTime = new kintoneUIComponent.DateTime({value: new Date(), isDisabled: false});
 
kintone.events.on('app.record.index.show', function(event) {
    var container = kintone.app.getHeaderSpaceElement();
    container.appendChild(myDateTime.render());
    myDateTime.enable();
});
</pre>
</td>
<td>Enable DateTime.</td>
</tr>
</table>