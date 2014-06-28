Polyinstant
==========

Polymer elements for connecting and manipulating data from goinstant.
Give your account number and app name. If no room is given the 'lobby' will be joined.

```HTML
<go-connect account="MY_ACCOUNT" app="MY_APP" room="ROOM_NAME"></go-connect>
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
