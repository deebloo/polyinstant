Polyinstant
==========

Polymer element for connecting and manipulating data from goinstant.
Give your account number and app name. If no room is given the 'lobby' will be joined.

```HTML
<go-connect account="773bb51eb592" app="WebComponentTest" room="lobby"></go-connect>

<go-data key="/test2" query={'author': 'Stan Lee'}></go-data>
```

```JS
var data = document.querySelector('go-data');

data.addEventListener('gotData', function(res) {
    console.log(res.detail.data);
});

```
