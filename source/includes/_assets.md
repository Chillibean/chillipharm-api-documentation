# Assets

## Get all Assets
```shell
curl -X GET "https://api.chillipharm.dev/libraries/<Library_ID>/assets" -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[  
   {  
      "id":2,
      "filename": "file.mp4",
      "filesize": 500,
      "file_type": "video",
      "s3_name": "example/path/to/file.mp4",
      "library_id": 31,
      "collection_ids": [],
      "uploader_id": 1715,
      "account_id":1,
      "asset_infos": [
        {
          "info_field_id": 1519,
          "value": "file.mp4"
        },
        {
          "info_field_id": 1520,
          "value": "0"
        }
      ]
      "created_at":"2017-12-08T12:14:22.849Z",
      "updated_at":"2017-12-08T12:14:22.849Z",
      "deleted_at":null
   },
   {  
      "id":3,
      "filename": "file.mp4",
      "filesize": 500,
      "file_type": "video",
      "s3_name": "example/path/to/file.mp4",
      "library_id": 31,
      "collection_ids": [],
      "uploader_id": 1715,
      "account_id":1,
      "asset_infos": [
        {
          "info_field_id": 1519,
          "value": "file.mp4"
        },
        {
          "info_field_id": 1520,
          "value": "0"
        }
      ]
      "created_at":"2017-12-08T12:14:22.849Z",
      "updated_at":"2017-12-08T12:14:22.849Z",
      "deleted_at":null
   }
]
```

This endpoint retrieves a list of all Assets within the specified Library.

### HTTP Request

`GET https://chillipharm.com/api/v1/accounts/<Account_ID>/libraries/<Library_ID>/assets`

## Get a Specific Asset
```shell
curl -X GET "https://api.chillipharm.dev/libraries/<Library_ID>/assets/<Asset_ID>" -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
  {  
    "id":3,
    "filename": "file.mp4",
    "filesize": 500,
    "file_type": "video",
    "s3_name": "example/path/to/file.mp4",
    "library_id": 31,
    "collection_ids": [],
    "uploader_id": 1715,
    "account_id":1,
    "asset_infos": [
      {
        "info_field_id": 1519,
        "value": "file.mp4"
      },
      {
        "info_field_id": 1520,
        "value": "0"
      }
    ]
    "created_at":"2017-12-08T12:14:22.849Z",
    "updated_at":"2017-12-08T12:14:22.849Z",
    "deleted_at":null
  }
```

This endpoint retrieves a specific Asset within the specified Library.

### HTTP Request

`GET https://chillipharm.com/api/v1/accounts/<Account_ID>/libraries/<Library_ID>/assets/<Asset_ID>`

## Create an Asset
This endpoint creates an Asset within the specified Library.

<aside class="warning">An upload token must be provided</aside>