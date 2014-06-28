Polyinstant
==========

Polymer elements for connecting and manipulating data from goinstant

```HTML
<go-connect account="MY_ACCOUNT" app="MY_APP"></go-connect>
```

```JS
window.addEventListener('polymer-ready', function(e) {
  // Get reference of the connection element
  var goConnect = document.querySelector('go-connect');

  // call connect from api
  goConnect.connect().then(function(res) {
    goConnect.getAllData(res, '/test', function(data) {
      console.log(data);
    });
  });
});
```
