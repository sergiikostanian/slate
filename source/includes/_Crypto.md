# Crypto

## Get Primary Public Key

> Success Response Example

```json
  {
    "pub_key": "W9JyHNLpYKPDM3Bwr87GQEjaar2n3LEDJ8PgdHZ9xgvHwkxq2stM"
  }
```

### URL

    `USER.CRYPTO#PUB_KEY.PRIMARY.GET`

### URL Params

| Parameter |  Type   |  Required |
|-----------|---------|-----------|
| user_id   |  String |  yes      |


## Encrypted Keys List By ID

> Success Response Example

```json
  {
    "encrypted_keys": [
      {
        "created_at": "2017-04-12T13:42:26.000Z",
        "crypto_container": {
            "key_id": "uoPxD3tXnKHi",
            "payload": "/JEJg3Le79c4svjYhbgyeM1vN7ylYbCGv+5eJmjJ292yQXpaL2PaGOa/FgTok7qE1DTT6O8dJlLvcSEM5STj6DQ2BdPJ/C02kzxNsQGs7EXR1FHnYqlvMKDBxHHPRyAM9w5YEdre",
            "sign": "wabgAnD4vWfCsiP6Rvx6PYhf3FMRhH7W2mVUrcXMLHqYeKhwqMCRhz3NHrF8Q65w7TUnoaFegsSUdww9PYTFbtyD7n",
            "signer_pub_key": "W9LKc4f7NEaKzgNaUQV8YzSMf3AgtuPrE4T8gpDfAYDgstzjs2CS",
        },
        "signer_user_id": "pupkin",
        "target_pub_key": "W9JyHNLpYKPDM3Bwr87GQEjaar2n3LEDJ8PgdHZ9xgvHwkxq2stM",
      },
    ]
  }
```

### URL

    `USER.CRYPTO#ENCRYPTED_KEY.LIST`

### URL Params

| Parameter     |  Type   |  Required |
|---------------|---------|-----------|
| crypto_key_id |  String |  yes      |


## Encrypted Keys List By Public Key

> Success Response Example

```json
  {
    "chained_encrypted_keys": [
      {
        "created_at": "2017-04-12T13:42:26.000Z",
        "crypto_container": {
            "key_id": "uoPxD3tXnKHi",
            "payload": "/JEJg3Le79c4svjYhbgyeM1vN7ylYbCGv+5eJmjJ292yQXpaL2PaGOa/FgTok7qE1DTT6O8dJlLvcSEM5STj6DQ2BdPJ/C02kzxNsQGs7EXR1FHnYqlvMKDBxHHPRyAM9w5YEdre",
            "sign": "wabgAnD4vWfCsiP6Rvx6PYhf3FMRhH7W2mVUrcXMLHqYeKhwqMCRhz3NHrF8Q65w7TUnoaFegsSUdww9PYTFbtyD7n",
            "signer_pub_key": "W9LKc4f7NEaKzgNaUQV8YzSMf3AgtuPrE4T8gpDfAYDgstzjs2CS",
        },
        "signer_user_id": "pupkin",
        "target_pub_key": "W9JyHNLpYKPDM3Bwr87GQEjaar2n3LEDJ8PgdHZ9xgvHwkxq2stM",
      },
    ],
    "created_at": "2017-04-12T13:42:26.000Z"
  }
```

### URL

    `USER.CRYPTO#PUB_KEY.GET`

### URL Params

| Parameter |  Type   |  Required |
|-----------|---------|-----------|
| pub_key   |  String |  yes      |


## Publish Public Key

> Empty Response

### URL

    `USER.CRYPTO#PUB_KEY.PUBLISH`

### URL Params

| Parameter             |  Type                          |  Required |
|-----------------------|--------------------------------|-----------|
| pub_key               |  String                        |  yes      |
| sign                  |  String                        |  yes      |
| chained_encrypted_key |  [EncryptedKey](#encryptedkey) |           |
