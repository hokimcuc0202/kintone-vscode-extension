# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-dialog</td>
<td>
<pre>
var myDialog = new kintoneUIComponent.Dialog({
    header: "Dialog header",
    content: "This is content",
    footer: "Footer",
    isVisible: true,
    showCloseButton: true
});
</pre>
</td>
<td>Constructor of Dialog</td>
</tr>

<tr>
<td>kuc-dialog-render</td>
<td>
<pre>
var myDialog = new kintoneUIComponent.Dialog({
    header: "Dialog header",
    content: "This is content",
    footer: "Footer",
    isVisible: true,
    showCloseButton: true
});
 
var body = document.getElementsByTagName("BODY")[0];
    body.appendChild(myDialog.render());
</pre>
</td>
<td>Get dom element of component.</td>
</tr>

<tr>
<td>kuc-dialog-show</td>
<td>
<pre>
var myDialog = new kintoneUIComponent.Dialog({
    header: "Dialog header",
    content: "This is content",
    footer: "Footer",
    isVisible: false,
    showCloseButton: true
});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(myDialog.render());
myDialog.show();
</pre>
</td>
<td>Display the Dialog.</td>
</tr>

<tr>
<td>kuc-dialog-hide</td>
<td>
<pre>
var myDialog = new kintoneUIComponent.Dialog({
    header: "Dialog header",
    content: "This is content",
    footer: "Footer",
    isVisible: true,
    showCloseButton: true
});
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(myDialog.render());
myDialog.hide();
</pre>
</td>
<td>Hide the Dialog.</td>
</tr>

<tr>
<td>kuc-dialog-set-header</td>
<td>
<pre>
var myDialog = new kintoneUIComponent.Dialog();
var elements = 'Announcement'
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(myDialog.render());
myDialog.setHeader(elements);
myDialog.show();
</pre>
</td>
<td>Set header for Dialog.</td>
</tr>

<tr>
<td>kuc-dialog-get-header</td>
<td>
<pre>

var myDialog = new kintoneUIComponent.Dialog({
    header: "Dialog header",
    content: "This is content",
    footer: "Footer",
    isVisible: true,
    showCloseButton: true
});
 
document.body.append(myDialog.render());
 
myDialog.getHeader();
</pre>
</td>
<td>Get header for Dialog.</td>
</tr>

<tr>
<td>kuc-dialog-set-content</td>
<td>
<pre>
var myDialog = new kintoneUIComponent.Dialog();
var elements = 'Content'
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(myDialog.render());
myDialog.setContent(elements);
myDialog.show();
</pre>
</td>
<td>Set content for Dialog.</td>
</tr>

<tr>
<td>kuc-dialog-get-content</td>
<td>
<pre>
var myDialog = new kintoneUIComponent.Dialog({
    header: "Dialog header",
    content: "This is content",
    footer: "Footer",
    isVisible: false,
    showCloseButton: true
});
 
document.body.append(myDialog.render());
 
myDialog.getContent();
</pre>
</td>
<td>Get content for Dialog.</td>
</tr>

<tr>
<td>kuc-dialog-set-footer</td>
<td>
<pre>
var myDialog = new kintoneUIComponent.Dialog();
var elements = 'Footer'
var body = document.getElementsByTagName("BODY")[0];
body.appendChild(myDialog.render());
myDialog.setFooter(elements);
myDialog.show();
</pre>
</td>
<td>Set footer for Dialog.</td>
</tr>

<tr>
<td>kuc-dialog-get-footer</td>
<td>
<pre>
var myDialog = new kintoneUIComponent.Dialog({
    header: "Dialog header",
    content: "This is content",
    footer: "Footer",
    isVisible: true,
    showCloseButton: true
});
 
document.body.append(myDialog.render());
 
myDialog.getFooter();
</pre>
</td>
<td>Get footer for Dialog.</td>
</tr>
</table>