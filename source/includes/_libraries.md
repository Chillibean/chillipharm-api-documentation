# Libraries

## Get All Libraries

```shell
curl -X GET "https://api.chillipharm.dev/libraries" -H "Authorization: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE1MTM0MjI1OTcsInN1YiI6MX0.GsAxGOkUzTNANYfcvT1OM1xxCxIndmXjw-2OkJgXO4a"
```

> The above command returns JSON structured like this:

```json
[  
   {  
      "id":2,
      "name":"Another Client Library",
      "account_id":1,
      "created_at":"2017-12-08T12:14:22.849Z",
      "updated_at":"2017-12-08T12:14:22.849Z",
      "assets_count":0,
      "creator_id":2,
      "deleted_at":null
   },
   {  
      "id":1,
      "name":"My First Library!",
      "account_id":1,
      "created_at":"2017-12-08T12:14:22.797Z",
      "updated_at":"2017-12-11T15:18:07.063Z",
      "assets_count":4,
      "creator_id":2,
      "deleted_at":null
   }
]
```

This endpoint retrieves a list of all Libraries within the specified Account that the logged-in User has been given access to.

### HTTP Request

`GET https://chillipharm.com/api/v1/accounts/<Account_ID>/libraries`

### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_deleted | false | If set to true, the result will also include deleted Libraries.

## Get a Specific Library

```shell
curl -X GET "https://api.chillipharm.dev/libraries/123" -H "Authorization: eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJleHAiOjE1MTM0MjI1OTcsInN1YiI6MX0.GsAxGOkUzTNANYfcvT1OM1xxCxIndmXjw-2OkJgXO4a"
```

> The above command returns JSON structured like this:

```json
{  
   "id":2,
   "name":"Another Client Library",
   "account_id":1,
   "created_at":"2017-12-08T12:14:22.849Z",
   "updated_at":"2017-12-08T12:14:22.849Z",
   "assets_count":0,
   "creator_id":2,
   "deleted_at":null
}
```

This endpoint retrieves a specific Library within the specified Account.

### HTTP Request

`GET https://chillipharm.com/api/v1/accounts/<Account_ID>/libraries/<Library_ID>`

### URL Parameters

Parameter | Default | Description
--------- | ------- | -----------
ID |  | The ID of the library to retrieve
include_deleted | false | If set to true, the result will also include deleted Libraries.