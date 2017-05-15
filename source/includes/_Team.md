# Team

## Team List

> Success Response Example

```json
    {
      "teams": [
        {
          "created_at": "2017-04-03T12:02:26.548Z",
          "crypto_key_id": "ucm7mdETZdX3",
          "description": "",
          "direct": "bohd",
          "name": "",
          "revision": "347802063547138049",
          "team_id": "direct-347802061267533825",
          "unread_message_count": 0,
          "unread_notification_count": 2,
        },
      ],
      "revision": "349648915743637505",
    }
```

### URL

    `TEAM#LIST`

### URL Params

Without parameters


## Team Availability

> Success Response Example

```json
  {
      "available": true
  }
```

### URL

    `TEAM#AVAILABILITY.CHECK`

### URL Params

| Parameter |  Type   |  Required |
|-----------|---------|-----------|
| team_id   |  String |  yes      |


## Create Team

> Success Response Example

```json
	{
	    "team_id": "VasiaTeam",
	    "revision": "353102072647780353"
	}
```

### URL

    `TEAM#CREATE`

### URL Params

| Parameter        |  Type                                |  Required |
|------------------|--------------------------------------|-----------|
| team_id          |  String                              |           |
| crypto_container |  [CryptoContainer](#cryptocontainer) |           |
| invitee_user_id  |  String                              |           |
| name             |  String                              |           |
| description      |  String                              |           |


## Get Team

> Success Response Example

```json
  {
      "created_at": "2017-04-03T12:02:26.548Z",
      "crypto_key_id": "ucm7mdETZdX3",
      "description": "",
      "direct": "bohd",
      "name": "",
      "revision": "347802063547138049",
      "team_id": "direct-347802061267533825",
      "unread_message_count": 0,
      "unread_notification_count": 2,
  }
```

### URL

    `TEAM#GET`

### URL Params

| Parameter |  Type   |  Required |
|-----------|---------|-----------|
| team_id   |  String |  yes      |


## Disable Team

> Success Response Example

```json
  {
      "revision": "347802063547138049",
  }
```

### URL

    `TEAM#DISABLE`

### URL Params

| Parameter |  Type   |  Required |
|-----------|---------|-----------|
| team_id   |  String |  yes      | 
