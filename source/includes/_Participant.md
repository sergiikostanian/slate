# Participant

## Get Participant

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
    "revision": "763h387348g638g76",
  }
```

### URL

    `TEAM.WORKSPACE.PARTICIPANT#GET`

### URL Params

| Parameter    |  Type   |  Required |
|--------------|---------|-----------|
| team_id      |  String |  yes      |
| workspace_id |  String |  yes      |
| user_id      |  String |  yes      |


## Participants List

> Success Response Example

```json
  {
    "participants": [
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

    `TEAM.WORKSPACE.PARTICIPANT#LIST`

### URL Params

| Parameter    |  Type   |  Required |
|--------------|---------|-----------|
| team_id      |  String |  yes      |
| workspace_id |  String |  yes      |


## Add Participant

> Success Response Example

```json
  {
    "revision": "763h387348g638g76"
  }
```

### URL

    `TEAM.WORKSPACE.PARTICIPANT#ADD`

### URL Params

| Parameter    |  Type                  |  Required |
|--------------|------------------------|-----------|
| team_id      |  String                |  yes      |
| workspace_id |  String                |  yes      |
| user_id      |  String                |  yes      |
| role         |  [RoleItem](#roleitem) |  yes      |
