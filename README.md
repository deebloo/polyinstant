Polyinstant
==========

Polymer element for connecting and manipulating data from goinstant.
Give your account number and app name. If no room is given the 'lobby' will be joined.

```HTML
<go-instant account="773bb51eb592" app="WebComponentTest" room="lobby" key="/test"></go-instant>
```

```JS
window.addEventListener('polymer-ready', function(e) {

    var goInstant =  document.querySelector('go-instant');
  
    goInstant.findAll(function(res) { console.log(res); });
  
    goInstant.find({name: 'Danny'}, function(res) { console.log(res); });
  
    // goInstant.add({name: 'Paul', title: 'Genius'});
    // goInstant.remove('id-146f98e95e2-000-0');
    
});
```
