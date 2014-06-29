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
  var goConnect = document.querySelector('go-connect'),
      goData = document.querySelector('go-data');

  /* Connect to goinstant */
  goConnect.go().then(function(connection) {
    /* Gets all data from key */
    goData.getAllData(connection, function(connection) {
      console.log(data);
    });

    /* Query data for matches */
    goData.find(connection, {name: 'Danny'}, function(data) {
      console.log(data);
    });
  });
});
```
