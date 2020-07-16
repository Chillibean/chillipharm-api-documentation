# Uploading

## Request Upload Permission
```shell
curl -X GET "https://api.chillipharm.dev/libraries/<Library_ID>/upload_permission" -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{  
  "presigned_url":"xyz",
  "asset_token": "xyz"
}
```

This endpoint requests permission to upload a file to an AWS S3 bucket and create an asset.

Returns an object containing: 
- a presigned URL for uploading directly to an AWS S3 bucket
- a unique token required when creating an Asset, which links the upload to the Asset

### HTTP Request

`GET https://chillipharm.com/api/v1/accounts/<Account_ID>/libraries/<Library_ID>/upload_permission`