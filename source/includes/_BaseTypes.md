# Base Types

## CryptoContainer

> Example

```json
  {
    "key_id": "uoPxD3tXnKHi",
    "payload": "/JEJg3Le79c4svjYhbgyeM1vN7ylYbCGv+5eJmjJ292yQXpaL2PaGOa/FgTok7qE1DTT6O8dJlLvcSEM5STj6DQ2BdPJ/C02kzxNsQGs7EXR1FHnYqlvMKDBxHHPRyAM9w5YEdre",
    "sign": "wabgAnD4vWfCsiP6Rvx6PYhf3FMRhH7W2mVUrcXMLHqYeKhwqMCRhz3NHrF8Q65w7TUnoaFegsSUdww9PYTFbtyD7n",
    "signer_pub_key": "W9LKc4f7NEaKzgNaUQV8YzSMf3AgtuPrE4T8gpDfAYDgstzjs2CS",
  }
```

| Parameter      |  Type   |  Description                                                   |
|----------------|---------|----------------------------------------------------------------|
| key_id         |  String |  Encoded access key ID                                         |
| payload        |  String |  Serialized and encoded payload data                           |
| sign           |  String |  Serialized payload signature hash                             |
| signer_pub_key |  String |  Public key of key pair from which the signature has been made |

## Presence

Users presence in app. Can have following values of __String__ type:

`AWAY`

`ACTIVE`

## RoleItem

Users role in app. Can have following values of __String__ type:

`ADMIN`

`COMPLIANCE`

`OWNER`

`RESTRICTED`

`MEMBER`

`GUEST`

`SUPERVISOR`

`MANAGER`

`WORKER`

`OBSERVER`

`PARTICIPANT`

## PayloadFormat

Payload format. Can have following values of __String__ type:

`witcrypt`

`file-attachment`

## SeenBy

> Example

```json
    "pupkin": "2017-05-03T07:32:11.283Z"
```

| Parameter |  Type |  Description                                                                                            |
|-----------|-------|---------------------------------------------------------------------------------------------------------|
| SenderID  |  Date |  This field describes the moment when user has seen some entry, it has user ID as key and date as value |
SenderID is a String

## Attachment

> Example

```json
  {
    "files": [
        {
          "file_id": "349447611987525633"
        },
        {
          "file_id": "349447611985535647"
        },
      ]
  }
```

| Parameter |  Type        |  Description              |
|-----------|--------------|---------------------------|
| files     |  Array[File] |  Array of files structure |


File structure is a JSON that contains following parameter:

| Parameter |  Type   |  Description |
|-----------|---------|--------------|
| file_id   |  String |  ID of file  |


## EncryptedKey

| Parameter        |  Type            |  Description                         |
|------------------|------------------|--------------------------------------|
| target_pub_key   |  String          |  User public key                     |
| crypto_container |  [CryptoContainer](#cryptocontainer) |  Structure of encrypted pice of data |

## Metadata

| Parameter | Type                    | Description          |
|-----------|-------------------------|----------------------|
| animated  | Bool                    |                      |
| preview   | [ImageSize](#imagesize) | Preview image size   |
| thumbnail | [ImageSize](#imagesize) | Thumbnail image size |

## ImageSize

| Parameter | Type | Description  |
|-----------|------|--------------|
| width     | Int  | Image width  |
| height    | Int  | Image height |
