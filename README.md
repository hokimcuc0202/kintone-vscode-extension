# kintone extension
Extension for kintone javascript api.
Support for the Javascript, React, Typescript. Including features such as auto-completion, snippets.

## Feature details

### Auto-completion
This extension support [kintone javascript api auto-complete](https://developer.kintone.io/hc/en-us/articles/360009339614)

### Snippet

#### Snippet for [kintone-js-sdk](https://github.com/hokimcuc0202/kintone-vscode-extension/blob/master/docs/snippets/js-sdk/index.md)
#### Snippet for [kintone-ui-component](https://github.com/hokimcuc0202/kintone-vscode-extension/blob/master/docs/snippets/kuc/index.md)
#### Snippet for js API
* [JS API](https://github.com/hokimcuc0202/kintone-vscode-extension/blob/master/docs/snippets/rest-api/index.md)
* Event

    |Shortcut|Code generator|Description|
    |---|---|---|
    |ke|<pre>kintone.events.on('app.record.index.show', function(event) { <br>   return event; <br>});</pre>|Handle Event on kintone|
    |kepromise|<pre>kintone.events.on('app.record.create.submit', function(event) {<br>  return new kintone.Promise(function(resolve, reject) {<br>    // resolve a promise function handler <br>    kintone.api(pathOrUrl, method, params, function(resp) {<br>      resolve(resp);<br>    });<br>  }).then(function(resp) {<br>    //handle response from above promise here<br>  });<br>  return event;<br>});</pre>|Handle Event on kintone using promise|

* proxy

    |Shortcut|Code generator|Description|
    |---|---|---|
    |kapipromise|<pre>kintone.api(pathOrUrl, method, params).then(function(resp) {<br>  //This should resolve first<br>}).catch(function(error) {<br>  //If an error is included in the response message, show it<br>});</pre>|Send kintone REST API request using promise|
    |kproxyuploadpromise|<pre>kintone.proxy.upload('url', 'POST', {} /* headers \*/, {} /* data \*/).then(function(args) {<br>  /*  args[0] -> body(string)<br>  /*  args[1] -> status(number)<br>  /*  args[2] -> headers(object)<br>  \*/<br>}, function(error) {<br>  //Display the response body (string) from the proxy API<br>});</pre>|Use kintone proxy to upload|
    |kplproxypromise|<pre>kintone.plugin.app.proxy('pluginId', 'url', 'GET', {} /* headers \*/, {} /* data \*/).then(function(args) {<br>  /*  args[0] -> body(string)<br>  /*  args[1] -> status(number)<br>  /*  args[2] -> headers(object)<br>  \*/<br>}, function(error) {<br>  //Display the response body (string) from the proxy API<br>});</pre>|Use kintone proxy to send external request in plugin|
    |kplproxyuploadpromise|<pre>kintone.plugin.app.proxy.upload('pluginId', 'url', 'POST', {} /* headers \*/, {} /* data \*/).then(function(args) {<br>  /*  args[0] -> body(string)<br>  /*  args[1] -> status(number)<br>  /*  args[2] -> headers(object)<br>  \*/<br>}, function(error) {<br>  //Display the response body (string) from the proxy API <br>});</pre>|Use kintone proxy to upload|