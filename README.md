Polyinstant
==========

Polymer elements for connecting and manipulating data from goinstant.
Give your account number and app name. If no room is given the 'lobby' will be joined.

Give the desired key and query parameters. If not query parameters are given all data from the specified key will be retrieved.

```HTML
<go-connect account="773bb51eb592" app="WebComponentTest" room="lobby"></go-connect>

<go-data key="/test2" query="{'author': 'Stan Lee'}" order="{'title': 'asc'}"></go-data>
```

```JS
var data = document.querySelector('go-data');

data.addEventListener('gotData', function(res) {
    console.log(res.detail.data);
});
```

To trigger a new query simply change the query value. (and likewise for key)
The change will trigger the same 'gotData' event. The query parameter MUST be a string and is parsed before being sent to goinstant.
```JS
data.query = "{'author': 'Robert Kirkman'}"
```
NOTE: look at the goinstant documentation on [filtering](https://developers.goinstant.com/v1/javascript_api/query/filtering.html) to see more details on how to structure your query.
