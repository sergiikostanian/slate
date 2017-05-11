# Session

## Create Session

> Success Response Example

```json
	{
		"session_id": "y3GSL3ONP38lfFRhZiCA1w",
		"user_id": "vasia_pupkin",
		"salt": "y1H3gF0ZraklErj683dbpA",
		"pin_code": "iJOHdrZ2aG4tFgle4y32kw",
		"ttl": 0,
	}
```

### URL

    `USER.SESSION#CREATE`

### URL Params

| Parameter |  Type   |  Required |
|-----------|---------|-----------|
| login     |  String |  yes      |
| password  |  String |  yes      |
| ttl       |  Int    |           |


## Auth Session

> Success Response Example

```json
	{
		"user_id": "vasia_pupkin",
		"salt": "y1H3gF0ZraklErj683dbpA",
		"pin_code": "qId2ZoBICtkVv201Trph4g",
		"ttl": 0,
	}
```

### URL

    `USER.SESSION#AUTH`

### URL Params

| Parameter  |  Type   |  Required |
|------------|---------|-----------|
| session_id |  String |  yes      |
| ttl        |  Int    |           |

## Close Session

> Empty Response

### URL

    `USER.SESSION#CLOSE`

### URL Params

Without parameters
