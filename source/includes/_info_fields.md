# Info Fields
Info Fields are user-defined fields that have a title and a type that allow custom data of a type to be attached to Assets.

## Get all Info Fields

```shell
curl -X GET "https://api.chillipharm.dev/accounts/<Account_ID>/info_fields" -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[  
   {  
      "id":1,
      "name":"Title",
      "type":"string"
   },
   {  
      "id":2,
      "name":"Reviewed",
      "type":"boolean"
   }
]
```

This endpoint retrieves a list of all Folders & Collections at the root level of a Library.

### HTTP Request

`GET https://chillipharm.com/api/v1/accounts/<Account_ID>/info_fields`