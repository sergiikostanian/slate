# Upload File

To upload file you need make multipart form data HTTP request using URL from [Get File Upload URL](#get-file-upload-url) response. Once you got your upload URL, follow next steps:

* If it's image, create thumbnail and preview of yours image with smaller sizes.

| Name         | Data                  | File Name | Mime Type              |
|--------------|-----------------------|-----------|------------------------|
| preview_size | Preview size in bytes |           |                        |
| preview      | Preview data          | preview   | Preview file mime type |

| Name           | Data                    | File Name | Mime Type                |
|----------------|-------------------------|-----------|--------------------------|
| thumbnail_size | Thumbnail size in bytes |           |                          |
| thumbnail      | Thumbnail data          | thumbnail | Thumbnail file mime type |

* Prepare metadata. Metadata is an encrypted JSON with following parameters:

If it's image

| Parameter | Type                  | Description |
|-----------|-----------------------|-------------|
| name      | String                | File name   |
| metadata  | [Metadata](#metadata) | File info   |

If it's any file

| Parameter | Type   | Description |
|-----------|--------|-------------|
| name      | String | File name   |

Encrypted metadata in request form:

| Name                           | Data              |
|--------------------------------|-------------------|
| crypto_key_id                  | Encrypted key ID  |
| target_pub_key                 | Public key        |
| metadata_crypto_payload        | Payload data      |
| metadata_crypto_sign           | Signature         |
| metadata_crypto_signer_pub_key | Signer public key |

* Separate file to chunks

* Encrypt all chunks using binary data encryption

* Upload first chunk. You should include metadata, thumbnail and preview (if it's image) data to form. You will receive uploading file ID in response, add this ID to form for next chunks.

| Name          | Data                   | File Name | Mime Type                |
|---------------|------------------------|-----------|--------------------------|
| file_size     | File size in bytes     |           |                          |
| last_modified | Last modified date     |           |                          |
| chunk_index   | Chunk sequential index |           |                          |
| chunk_size    | Chunk size in bytes    |           |                          |
| upload        | Chunk data             | file      | Uploading file mime type |


* Upload next chunks

| Name        | Data                   | File Name | Mime Type                |
|-------------|------------------------|-----------|--------------------------|
| file_id     | Uploading file ID      |           |                          |
| chunk_index | Chunk sequential index |           |                          |
| chunk_size  | Chunk size in bytes    |           |                          |
| upload      | Chunk data             | file      | application/octet-stream |
