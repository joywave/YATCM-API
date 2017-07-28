These are the initial "schemas" for objects at various endpoints. For things such as test testcases these shoild be flexible by creating templates at another endpoint.


# projects
```json
{
"id": 0,
"title": "Name of the test plan",
"description": "A simple description",
"created_at": "2015-01-01T12:10:30Z",
"created_by_id": 100
}
```
## projects/history
```json
{
"id": 0,
"modified_by_id": 100,
"action": "add,remove,modify",
"before": "",
"after": ""
}
```

# testsuites
```json
"id": 0,
"title": "Name of the test plan",
"description": "A simple description",
"created_at": "2015-01-01T12:10:30Z",
"created_by_id": 100,


```

# testcases
```json

```

# testplans
```json
{
"id": 0,
"title": "Name of the test plan",
"description": "A simple description",
"created_at": "2015-01-01T12:10:30Z",
"created_by": "User Name"
}
```

# testruns

# users