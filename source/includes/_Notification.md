# Notification

## Get Notification

> Success Response Example

```json
  {
    "notification_id": "349447612081897473",
    "payload_format": "team-crypto-key-request",
    "deleted": false,
    "created_at": "2017-04-12T13:42:26.000Z",
    "updated_at": "2017-04-12T13:42:26.000Z",
    "seen_by": [
      {
        "pupkin": "2017-04-12T13:42:26.000Z",
      },
    ]
  }
```

### URL

    `TEAM.NOTIFICATION#GET`

### URL Params

| Parameter       |  Type   |  Required |
|-----------------|---------|-----------|
| team_id         |  String |  yes      |
| notification_id |  String |  yes      |


## Notifications List

> Success Response Example

```json
  {
    "notifications": [
      {
        "notification_id": "349447612081897473",
        "payload_format": "team-crypto-key-request",
        "deleted": false,
        "created_at": "2017-04-12T13:42:26.000Z",
        "updated_at": "2017-04-12T13:42:26.000Z",
        "seen_by": [
          {
            "pupkin": "2017-04-12T13:42:26.000Z",
          },
        ]
      },
    ],
    "revision": "349451673657147393",
  }
```

### URL

    `TEAM.NOTIFICATION#LIST`

### URL Params

| Parameter             |  Type   |  Required |
|-----------------------|---------|-----------|
| team_id               |  String |  yes      |
| prior_notification_id |  String |           |
| after_notification_id |  String |           |
| limit_count           |  Int    |           |


## Mark Notification Received

> Success Response Example

```json
  {
    "revision": "349451673657147393"
  }
```

### URL

    `TEAM.NOTIFICATION#MARK.RECEIVED`

### URL Params

| Parameter       |  Type   |  Required |
|-----------------|---------|-----------|
| team_id         |  String |  yes      |
| notification_id |  String |  yes      | 
