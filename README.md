Polyinstant
==========

Polymer elements for connecting and manipulating data from goinstant.
Give your account number and app name. If no room is given the 'lobby' will be joined.

```HTML
<go-connect account="MY_ACCOUNT" app="MY_APP" room="ROOM_NAME"></go-connect>

<go-data key="KEY_NAME"></go-data>
```

```JS
window.addEventListener('polymer-ready', function(e) {
  /*
   * Get reference to the connection element
   * Get reference to the data connection
   */
  var goConnect = document.querySelector('go-connect');
  var goData = document.querySelector('go-data');

  /*
   * Connect to goinstant
   * returns promise and fires callback
   */
  goConnect.go(function() {
    alert('connected! look at console to see data');
  })
  .then(function(res) {
    // pass the result to the goData api and return the results
    goData.getAllData(res, function(data) {
      console.log(data);
    });

    goData.find(res, {name: 'Danny'}, function(data) {
      console.log(data);
    });
  });
});
```
