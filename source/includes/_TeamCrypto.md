# Team Crypto

## Encrypt Team

> Success Response Example

```json
  {
      "revision": "347802063547138049",
  }
```

### URL

    `TEAM.CRYPTO#ENCRYPTED_KEY.PRIMARY.SET`

### URL Params

| Parameter        |  Type                                |  Required |
|------------------|--------------------------------------|-----------|
| team_id          |  String                              |  yes      |
| crypto_container |  [CryptoContainer](#cryptocontainer) |  yes      |


## Grant Access

> Empty Response

### URL

    `TEAM.CRYPTO#ENCRYPTED_KEY.PRIMARY.SET`

### URL Params

| Parameter        |  Type                                |  Required |
|------------------|--------------------------------------|-----------|
| team_id          |  String                              |  yes      |
| target_user_id   |  String                              |  yes      |
| target_pub_key   |  String                              |  yes      |
| crypto_container |  [CryptoContainer](#cryptocontainer) |  yes      |
