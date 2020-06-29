# Folders & Collections
Folders and Collections are further ways to organise Assets inside a Library.  
Folders and Collections are structured as a nested tree of <strong>Nodes</strong> with a type (either collection or folder).  

<aside class="notice">Collections contain Assets, and Folders contain Collections.</aside>

## Get all root level Nodes

```shell
curl -X GET "https://api.chillipharm.dev/libraries/<Library_ID>/nodes" -H "Authorization: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE1MTM0MjI1OTcsInN1YiI6MX0.GsAxGOkUzTNANYfcvT1OM1xxCxIndmXjw-2OkJgXO4a"
```

> The above command returns JSON structured like this:

```json
[  
   {  
      "id":2,
      "name":"Collection 1",
      "account_id":1,
      "created_at":"2017-12-08T12:14:22.849Z",
      "updated_at":"2017-12-08T12:14:22.849Z",
      "type":"collection"
   },
   {  
      "id":2,
      "name":"Folder 1",
      "account_id":1,
      "created_at":"2017-12-08T12:14:22.849Z",
      "updated_at":"2017-12-08T12:14:22.849Z",
      "type":"folder"
   }
]
```

This endpoint retrieves a list of all Folders & Collections at the root level of a Library.

### HTTP Request

`GET https://chillipharm.com/api/v1/accounts/<Account_ID>/libraries/<Library_ID>/nodes`

## Get a Specific Node

```shell
curl -X GET "https://api.chillipharm.dev/libraries/<Library_ID>/nodes/<Node_ID>" -H "Authorization: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE1MTM0MjI1OTcsInN1YiI6MX0.GsAxGOkUzTNANYfcvT1OM1xxCxIndmXjw-2OkJgXO4a"
```

> The above command returns JSON structured like this:

```json
{  
  "id":2,
  "name":"Collection 1",
  "account_id":1,
  "created_at":"2017-12-08T12:14:22.849Z",
  "updated_at":"2017-12-08T12:14:22.849Z",
  "type":"collection"
}
```

This endpoint retrieves a specific Node within the specified Library.

### HTTP Request

`GET https://chillipharm.com/api/v1/accounts/<Account_ID>/libraries/<Library_ID>/nodes/<Node_ID>`

## Get all children of a Specific Node

```shell
curl -X GET "https://api.chillipharm.dev/libraries/<Library_ID>/nodes/<Node_ID>/children" -H "Authorization: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE1MTM0MjI1OTcsInN1YiI6MX0.GsAxGOkUzTNANYfcvT1OM1xxCxIndmXjw-2OkJgXO4a"
```

> The above command returns JSON structured like this:

```json
[  
   {  
      "id":3,
      "name":"Collection 3",
      "account_id":1,
      "created_at":"2017-12-08T12:14:22.849Z",
      "updated_at":"2017-12-08T12:14:22.849Z",
      "type":"collection"
   },
   {  
      "id":3,
      "name":"Folder 3",
      "account_id":1,
      "created_at":"2017-12-08T12:14:22.849Z",
      "updated_at":"2017-12-08T12:14:22.849Z",
      "type":"folder",
   },
   {  
      "id":4,
      "name":"Folder 4",
      "account_id":1,
      "created_at":"2017-12-08T12:14:22.849Z",
      "updated_at":"2017-12-08T12:14:22.849Z",
      "type":"folder",
   }
]
```

This endpoint retrieves all children of a specific Node within the specified Library.

### HTTP Request

`GET https://chillipharm.com/api/v1/accounts/<Account_ID>/libraries/<Library_ID>/nodes/<Node_ID>/children`