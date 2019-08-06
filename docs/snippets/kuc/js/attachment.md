# Snippet
<table>
<tr>
<th>Shortcut</th>
<th>Code generator</th>
<th>Description</th>
</tr>

<tr>
<td>kuc-attachment</td>
<td>
<pre>
var alert = new kintoneUIComponent.Alert({text: 'Network error', type: 'error'});
</pre>
</td>
<td>Initialize a KUC attachment</td>
</tr>

<tr>
<td>kuc-attachment-render</td>
<td>
<pre>
const attachment = new kintoneUIComponent.Attachment({files: [{name: 'test_1', size: 12345}]});
const body = document.getElementsByTagName('BODY')[0];
body.appendChild(attachment.render());
</pre>
</td>
<td>Get dom element of component.</td>
</tr>

<tr>
<td>kuc-attachment-set-files</td>
<td>
<pre>
const body = document.getElementsByTagName("BODY")[0];
 
const attachment = new kintoneUIComponent.Attachment();
body.appendChild(attachment.render());
 
const button = new kintoneUIComponent.Button({text: 'Set Files'});
body.appendChild(button.render());
button.on('click', () => {
    attachment.setFiles([{name: 'test_1', size: 12345}]);
});
</pre>
</td>
<td>Set the files of attachment field.</td>
</tr>

<tr>
<td>kuc-alert-get-files</td>
<td>
<pre>	
const body = document.getElementsByTagName("BODY")[0];
 
const attachment = new kintoneUIComponent.Attachment();
body.appendChild(attachment.render());
 
const button = new kintoneUIComponent.Button({text: 'Set Files'});
body.appendChild(button.render());
button.on('click', () => {
    attachment.setFiles([{name: 'test_1', size: 12345}]);
});
</pre>
</td>
<td>Get all files information of attachment field.</td>
</tr>

<tr>
<td>kuc-attachment-set-dropzone-text</td>
<td>
<pre>
const body = document.getElementsByTagName("BODY")[0];
const attachment = new kintoneUIComponent.Attachment();
body.appendChild(attachment.render());
attachment.setDropZoneText('Drop files here.');
</pre>
</td>
<td>Set the text of the drop zone</td>
</tr>

<tr>
<td>kuc-alert-set-browse-button-text</td>
<td>
<pre>
const body = document.getElementsByTagName("BODY")[0];
const attachment = new kintoneUIComponent.Attachment();
body.appendChild(attachment.render());
attachment.setBrowseButtonText('Browse');
</pre>
</td>
<td>Set the text of the browse button</td>
</tr>

<tr>
<td>kuc-alert-set-file-limit-text</td>
<td>
<pre>
const body = document.getElementsByTagName("BODY")[0];
const attachment = new kintoneUIComponent.Attachment();
body.appendChild(attachment.render());
attachment.setFileLimitText('Maximum: 1 GB');
</pre>
</td>
<td>Set the text of the file limit warn part.</td>
</tr>

<tr>
<td>kuc-alert-set-error-message</td>
<td>
<pre>
const body = document.getElementsByTagName("BODY")[0];
const attachment = new kintoneUIComponent.Attachment();
body.appendChild(attachment.render());
attachment.setErrorMessage('Error message');
</pre>
</td>
<td>Set the error message.</td>
</tr>

<tr>
<td>kuc-alert-show-error</td>
<td>
<pre>
const body = document.getElementsByTagName("BODY")[0];
 
const attachment = new kintoneUIComponent.Attachment({errorMessage: 'Error message'});
body.appendChild(attachment.render());
 
const showButton = new kintoneUIComponent.Button({text: 'Show Error'});
body.appendChild(showButton.render());
showButton.on('click', () => {
    attachment.showError();
});
</pre>
</td>
<td>Show the error message</td>
</tr>

<tr>
<td>kuc-attachment-hide-error</td>
<td>
<pre>
const body = document.getElementsByTagName("BODY")[0];
 
const attachment = new kintoneUIComponent.Attachment({errorMessage: 'Error message'});
body.appendChild(attachment.render());
 
const showButton = new kintoneUIComponent.Button({text: 'Show Error'});
body.appendChild(showButton.render());
showButton.on('click', () => {
    attachment.showError();
});
 
const hideButton = new kintoneUIComponent.Button({text: 'Hide Error'});
body.appendChild(hideButton.render());
hideButton.on('click', () => {
    attachment.hideError();
});
</pre>
</td>
<td>Hide the error message</td>
</tr>

<tr>
<td>kuc-attachment-on</td>
<td>
<pre>
const body = document.getElementsByTagName("BODY")[0];
 
const attachment = new kintoneUIComponent.Attachment();
body.appendChild(attachment.render());
 
attachment.on('filesAdd', (files) => {
    console.log('files:', files);
});
 
attachment.on('fileRemove', (files) => {
    console.log('files:', files);
});
</pre>
</td>
<td>Register callback for change event</td>
</tr>

<tr>
<td>kuc-attachment-show</td>
<td>
<pre>	
const attachment = new kintoneUIComponent.Attachment({files: [{name: 'test_1', size: 12345}]});
const body = document.getElementsByTagName('BODY')[0];
body.appendChild(attachment.render());
attachment.show();
</pre>
</td>
<td>Display the attachment component.</td>
</tr>

<tr>
<td>kuc-attachment-hide	
</td>
<td>
<pre>	
const attachment = new kintoneUIComponent.Attachment({files: [{name: 'test_1', size: 12345}]});
const body = document.getElementsByTagName('BODY')[0];
body.appendChild(attachment.render());
attachment.hide();
</pre>
</td>
<td>Hide the the attachment component.</td>
</tr>

</table>