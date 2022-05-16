# How to create modules?

### How to get json response?

```json
{
    ...
    "responseType": "json",
    "mainBody": "getJSON(\"response.body\").json"
    ...
}
- The first element inside "getJSON" (ie: response) is always ignored
- "responseType" has to be of type "json" for the compiler to use "getJson" to find the json elements
- "getJSON(\"response.body\")" must end with ".json" in order to tell the compiler "getJSON" returns a json object, if ".json" is not found then the compiler will automatically assume a "html" object is being returned.
```

### How to convert json response to json list?

```json
{
    ...
    "itemSelector": "json.list()"
    ...
}
- json.list() tells the compiler, the "mainBody" returns a json list object and should be treated as such
```
