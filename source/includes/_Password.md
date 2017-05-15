# Password

## Update Password

> Success Response Example

```json
  {
    "revision": "y3GSL3ONP38lfFRhZiCA1w"
  }
```

### URL

    `USER#PASSWORD.UPDATE`

### URL Params

| Parameter    |  Type   |  Required |
|--------------|---------|-----------|
| user_id      |  String |  yes      |
| new_password |  String |  yes      |
| old_password |  String |  yes      |


## Reset Password

> Empty Response

### URL

    `USER#REQUEST_PASSWORD_RESET`

### URL Params

| Parameter    |  Type   |  Required |
|--------------|---------|-----------|
| email_or_login |  String |  yes      |
