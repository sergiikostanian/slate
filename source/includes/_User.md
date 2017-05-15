# User

## Check User Availability

> Success Response Example

```json
  {
    "available": true
  }
```

### URL

    `USER#CHECK.AVAILABILITY`

### URL Params

| Parameter |  Type   |  Required |
|-----------|---------|-----------|
| user_id   |  String |  yes      |

## Create User

> Success Response Example

```json
  {
    "session_id": "y3GSL3ONP38lfFRhZiCA1w",
    "user_id": "vasia_pupkin",
    "salt": "y1H3gF0ZraklErj683dbpA",
    "pin_code": "iJOHdrZ2aG4tFgle4y32kw",
    "ttl": 0
  }
```

### URL

    `USER#CREATE`

### URL Params

| Parameter  |  Type   |  Required |
|------------|---------|-----------|
| user_id    |  String |  yes      |
| email      |  String |           |
| first_name |  String |           |
| last_name  |  String |           |
| password   |  String |           |

## Update User

> Success Response Example

```json
  {
    "revision": "y3GSL3ONP38lfFRhZiCA1w"
  }
```

### URL

    `USER#UPDATE`

### URL Params

| Parameter     |  Type     |  Required |
|---------------|-----------|-----------|
| email         |  String   |           |
| first_name    |  String   |           |
| last_name     |  String   |           |
| delete_avatar |  Bool     |           |
| presence      |  [Presence](#presence) |           |

## Get User

> Success Response Example

```json
{
    "user_id": "vasia_pupkin",
    "email": "vasia@pupkin.com",
    "last_name": "Pupkin",
    "first_name": "Vasia",
    "avatar": "http://path/to/avatar.jpg",
    "gravatar": "0bc83cb571cd1c50ba6f3e8a78ef1346",
    "presence": "ACTIVE",
    "created_at": "2017-04-03T12:02:26.548Z",
    "revision": "763h387348g638g76"
}
```

### URL

    `USER#GET`

### URL Params

| Parameter |  Type   |  Required |
|-----------|---------|-----------|
| user_id   |  String |  yes      |


## Search User

> Success Response Example

```json
{
    "users": [
      {
        "user_id": "vasia_pupkin",
        "email": "vasia@pupkin.com",
        "last_name": "Pupkin",
        "first_name": "Vasia",
        "avatar": "http://path/to/avatar.jpg",
        "gravatar": "0bc83cb571cd1c50ba6f3e8a78ef1346",
        "presence": "ACTIVE",
        "created_at": "2017-04-03T12:02:26.548Z",
        "revision": "763h387348g638g76",
      },
    ],
    "revision": "763h387348g638g76"
}
```

### URL

    `USER#SEARCH`

### URL Params

| Parameter |  Type   |  Required |
|-----------|---------|-----------|
| search    |  String |  yes      |
